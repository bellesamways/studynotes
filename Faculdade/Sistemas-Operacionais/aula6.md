# Aula 6 - Sistema de arquivos

## Gerência de arquivos

Um arquivo pode ser entendido como um conjunto de dados armazenados em um dispositivo físico não volátil, com um nome ou outra referência que permita sua localização posterior.

Do ponto de vista do usuário e das aplicações, o arquivo é a unidade básica de armazenamento de informação em um dispositivo não volátil, pois para eles não há forma mais simples de armazenamento persistente de dados.

Como um dispositivo de armazenamento pode conter milhões de arquivos, estes são organizados em estruturas hierárquicas denominadas diretórios.

![Gerência de arquivos](/media/sistemas_operacionais/diretorio-armazenamento.png)

O Sistema de Arquivos pode ser entendido então como a organização física e lógica dos dados armazenados de forma persistente em um dispositivo físico não volátil.

Existem vários sistemas de arquivos nos Ss.Os. dentre os quais podemos citar FAT e NTFS do Windows.

</br>

### Atributos

Como vimos, um arquivo é uma unidade de armazenamento de informações que podem ser dados, código executável etc. Cada arquivo é descrito por atributos, cujo conjunto varia de acordo com o sistema e arquivos utilizado. Os atributos mais usuais são:

**Nome**: String de caracteres que identifica o arquivo para o usuário, como “foto1.jpg”, “relatório.pdf”, “hello.c” etc.

**Tipo**: Indicação do formato dos dados contidos no arquivo, como áudio, vídeo, imagem, texto etc. Muitos sistemas operacionais usam parte do nome do arquivo para identificar o tipo de seu conteúdo, na forma de uma extensão:“.doc”,“.jpg”,“.mp3”, etc.

**Tamanho**: Indicação do tamanho do conteúdo do arquivo, em bytes ou registros.

**Datas**: Para fins de gerência, é importante manter as datas mais importantes relacionadas ao arquivo, como suas datas de criação, de último acesso e de última modificação do conteúdo.

**Proprietário**: Em sistemas multiusuários, cada arquivo tem um proprietário, que deve estar corretamente identificado.

**Permissões de acesso**: Indicam que usuários têm acesso àquele arquivo e que formas de acesso são permitidas (leitura, escrita, remoção etc.).

**Localização**: Indicação do dispositivo físico onde o arquivo se encontra e da posição do arquivo dentro do mesmo.

**Outros atributos**: Vários outros atributos podem ser associados a um arquivo, por exemplo, para indicar se é um arquivo de sistema, se está visível aos usuários, se tem conteúdo binário ou textual etc. Cada sistema de arquivos normalmente define seus próprios atributos específicos, além dos atributos usuais.

</br>

![Extensão de arquivos](/media/sistemas_operacionais/tipos-de-extensao.png)

## Operações

As aplicações e o sistema operacional utilizam um conjunto de operações para manipular arquivos.

As operações básicas, envolvendo arquivos, são:

**Criar**: a criação de um novo arquivo implica em alocar espaço para ele no dispositivo de armazenamento e definir seus atributos (nome, localização, proprietário, permissões de acesso, etc).

**Abrir**: antes que uma aplicação possa ler ou escrever dados em um arquivo, ela deve solicitar ao sistema operacional a "abertura" desse arquivo. O sistema irá então verificar se o arquivo existe, verificar se as permissões associadas ao arquivo permitem aquele acesso, localizar seu conteúdo no dispositivo de armazenamento e criar uma referência pra ele na memória da aplicação.

**Ler**: permite transferir dados presentes no arquivo para uma área de memória da aplicação.

**Escrever**: permite transferir dados na memória da aplicação para o arquivo no dispositivo físico, os novos dados podem ser adicionados no final do arquivo ou sobrescrever dados já existentes.

**Mudar atributos**: para modificar outras características do arquivo, como nome, localização, proprietário, permissões, etc.

**Fechar**: ao concluir o uso do arquivo, a aplicação deve informar ao sistema operacional que o mesmo não é mais necessário, a fim de liberar as estruturas de gerência do arquivo na memória do núcleo.

**Remover**: para eliminar o arquivo do dispositivo, descartando seus dados e liberando o espaço ocupado por ele.

</br>

### Organização Sequencial

Neste tipo de arquivo, os registros são acessados, quer para leitura quer para escrita, de forma sequencial, isto é, a escrita de um registro só é feita após o último registro escrito e a leitura de um registro só é possível após todos os registros anteriores terem sido lidos.

Existe um ponteiro “invisível” que assinala para o registro corrente e que é incrementado de forma automática após cada leitura ou escrita. Dizemos que o ponteiro é invisível porque **não é necessário lidar com ele no algoritmo**. O sistema de arquivos da linguagem que se utilizar (e que oferecer organização sequencial de arquivos) lida com o ponteiro automaticamente a cada operação de abertura, leitura ou escrita do arquivo. Quando abrimos um arquivo, devemos informar se desejamos ler ou escrever e, a partir de então, só podemos realizar esse tipo de operação (leitura ou escrita) até o fechamento do arquivo.

O esquema mostrado, a seguir, ilustra o funcionamento das operações de leitura em um arquivo sequencial chamado Agenda:

![Funcionamento das operações de leitura](/media/sistemas_operacionais/operacao-de-leitura-sequencial.png)

Na escrita, o ponteiro pode ser posto no início do arquivo (se for um arquivo novo) ou no final do arquivo (se quisermos acrescentar registros aos já existentes). A diferenciação é feita no comando de abertura. Veja:

![Funcionamento das operações de escrita](/media/sistemas_operacionais/operacao-de-escrita-sequencial.png)

Para lidar com arquivos sequenciais, existe uma função lógica (Verdadeiro/Falso) indicando se o ponteiro chegou ao fim do arquivo (na leitura). Chamamos essa função de EOF (_end of file_).

![Função de EOF (*end of file*)](/media/sistemas_operacionais/end-of-file.png)

Essa função é usada como critério de parada em repetições para testar se já atingimos o fim do arquivo sequencial.

### Organização Direta

Neste tipo de arquivo, podemos acessar um determinado registro no meio do arquivo pelo seu número (posição do registro dentro do arquivo). O arquivo, uma vez aberto, aceita tanto operações de leitura quanto de escrita.

### Organização Indexada

Neste tipo de arquivo, existe um local do registro chamado **campo chave** que permite o acesso a um registro determinado. Agora não temos mais um índice necessariamente numérico, como nos arquivos diretos.

Para podermos utilizar qualquer campo como índice (campo chave), o sistema de gerenciamento de arquivos da linguagem (que é transparente para o usuário) utiliza outro arquivo, chamado **arquivo de índice**, que é **ordenado** pelo campo chave. Esse arquivo de índice, possui um campo com a chave e outro com o número do registro correspondente àquela chave no arquivo principal.

Por exemplo, suponha que temos um arquivo com nome, endereço e telefone, e o campo chave é nome. Observe como seria a organização para os dados:

![Exemplo de organização de dados](/media/sistemas_operacionais/organizacao-indexada.png)

Note que o arquivo de índice é ordenado. Assim, quando precisa localizar um registro no arquivo principal, o sistema de arquivos percorre primeiro o de índice, procurando pelo nome chave. Após encontrar a chave, pega o índice (que representa a posição) do registro completo referente àquela chave no arquivo principal.

</br>

### Organização lógica

O sistema de arquivos é quebrado em **partições** conhecidas como _volumes_.

Existe pelo menos uma partição e é nessa estrutura de mais baixo nível que os arquivos efetivamente residem. Um mesmo dispositivo físico (uma unidade de disco magnético, por exemplo) pode conter mais de uma partição, cada uma delas tratada como um dispositivo virtual.

Informações sobre os arquivos são guardadas em entradas no **diretório** de dispositivos ou tabela de volumes. O diretório de dispositivos, também conhecido simplesmente como _diretório_, pode ser visto como uma estrutura de dados contendo informações sobre os arquivos tais como localização física, nome, atributos e demais informações que o sistema queira guardar sobre os arquivos. Veja um exemplo de disco com duas partições:

![Disco com duas partições](/media/sistemas_operacionais/disco-com-duas-particoes.png)

Nas organizações de diretórios mais antigas, todos os arquivos estavam contidos em um só diretório. Isso introduzia limitações no número de arquivos e, principalmente, na nomeação dos arquivos, já que o nome deve ser único dentro do diretório. Assim, os diretórios evoluíram para estruturas com diversos níveis.

Esses diretórios são, normalmente, implementados como estruturas de árvores. Na estrutura principal ou Master File Directory (MFD), existem ponteiros para os diretórios de cada usuário ou User File Directories (UFDs) que, por sua vez, possuem apontadores para os demais subdiretórios, que podem ser criados por cada usuário e assim por diante, em uma estrutura que culmina pela referenciação dos arquivos físicos propriamente ditos.

![Estrutura de árvore](/media/sistemas_operacionais/estrutura-de-arvore.png)

</br>

### Diretórios compartilhados

São estruturas que permitem que subdiretórios comuns sejam compartilhados. Um arquivo compartilhado existe no sistema em dois lugares, mas não como uma cópia, ou seja, só existe um arquivo físico. Assim, **mudanças realizadas por um usuário são visualizadas por outro**. Arquivos e subdiretórios compartilhados podem ser implementados de duas formas: **grupos de acesso ou listas de controle**.

Em ambos os mecanismos, é necessário estabelecer níveis de proteção diferentes para os diferentes usuários. Direitos de leitura, escrita, execução, criação e remoção de arquivos ou diretórios devem ser estabelecidos para cada usuário.

**Grupos de acesso**: no esquema de _listas de controle_, cada arquivo ou diretório a ser compartilhado possui uma lista associada, onde são relacionados os usuários e as operações que cada um desses usuários pode fazer. As desvantagens são o tamanho dessa estrutura que pode ser grande se o arquivo ou diretório for compartilhado por muitos usuários. Além disso, há o problema do acesso sequencial à lista de compartilhamento, que também é lento.

**Listas de controle**: no esquema de grupos de usuários, os usuários que queiram compartilhar arquivos devem pertencer a um mesmo grupo. Quando da criação do arquivo é adicionada uma estrutura que descreve quais os níveis de proteção para: o dono (_owner_), o grupo (_group_) e todos (_all_).

![Grupo de usuários](/media/sistemas_operacionais/grupo-de-usuarios.png)

</br>

### Organização Física

Os sistemas precisam manter o controle da localização física dos arquivos nos dispositivos. Os dispositivos físicos são, normalmente, divididos em blocos e a estrutura de gerência de arquivos deve mapear em quais blocos físicos se encontra um determinado arquivo. Para saber quais blocos estão livres, é preciso manter um registro de blocos livres. Esse registro pode ser feito de três formas. São elas:

**Mapa de bits**: uma forma de fazer esse registro é manter um mapa de bits, um bit para cada bloco, que indique em quais blocos estão livres. A desvantagem é a quantidade de memória empregada.

**Lista encadeada**: a segunda forma é manter uma lista encadeada de blocos livres no disco. A desvantagem é ser necessário guardar ponteiros nos próprios blocos, para o bloco seguinte, além de se percorrer sequencialmente a estrutura para encontrar os blocos.

**Tabela de blocos**: a terceira forma é, considerando-se que a maioria dos blocos são alocados em conjunto, manter uma tabela de blocos livres contíguos com localização e tamanho de cada conjunto de blocos.

![Tabela de Conjuntos Livres Contínuos](/media/sistemas_operacionais/tabela-conjuntos-livre.jpeg)

Para alocar espaço para um arquivo no disco, os primeiros sistemas procuravam por um espaço contíguo de blocos, de forma que só era necessário guardar o bloco inicial e o tamanho em blocos que o arquivo ocupava.

Naturalmente, isso é bastante ineficiente porque demanda escolher um bloco que tenha tamanho satisfatório para o arquivo (políticas de First-fit, Best-fit ou Worst-fit, como visto para partições de memória), além dos tradicionais problemas de fragmentação que ocorrem em longo prazo (depois de muitos arquivos terem sido criados e apagados). A solução foi criar esquemas de alocação não contígua.

Uma saída é a alocação encadeada, onde toda entrada de arquivo no diretório possui um apontador para um bloco inicial do disco que, por sua vez, aponta para o próximo bloco do arquivo e assim por diante. A desvantagem é, novamente, a obrigatoriedade do acesso sequencial.

Outra solução é o acesso indexado, em que um determinado bloco, chamado **bloco de índice**, contém os ponteiros para os demais blocos do arquivo no disco.

![bloco de índice](/media/sistemas_operacionais/bloco-de-indice.jpeg)

## Sistema de arquivos FAT e NTFS

FAT (File Allocation Table) é o principal sistema de arquivos de computadores para vários sistemas operacionais, na maior parte do DOS, incluindo o DR-DOS, OpenDOS, FreeDOS, MS-DOS, Microsoft Windows (até e incluindo o XP).

FAT é usado também para flash drives e cartões de memória removíveis.

Sistema de arquivos é o método para armazenar e organizar arquivos de computador e os dados que eles contêm para torná-los fácil de encontrar e acessá-los. A tabela a seguir mostra em que sistema de arquivo FAT um flash drive ou cartão de memória deve ser formatado:

![Sistema de arquivos](/media/sistemas_operacionais/sistemas-de-arquivo.png)

NTFS é o sistema de arquivos padrão do Windows Server 2008 e do Windows 10.

NTFS é destinado ao uso em unidades do sistema Windows (discos rígidos e drives de estado sólido).

NTFS tem várias melhorias em relação ao FAT, como suporte melhorado para metadados e o uso de estruturas de dados avançados de confiabilidade, e utilização de espaço em disco, além de extensões adicionais, tais como listas de segurança de controle de acesso e sistema de arquivos jornalístico.
