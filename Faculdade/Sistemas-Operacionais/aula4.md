# Aula 4 - Gerência de memória

A gerência de memória possui duas grandes abordagens:

Manter os processos na memória principal durante toda a sua execução;

Mover os processos entre a memória principal e secundária (tipicamente disco), utilizando técnicas de swapping (permuta) ou de paginação.

Hierarquia de memória:

cache: pequena memória e muito rápida que trabalha em conjunto com o processador pra aumentar o seu desempenho

memória ram: onde são armazenados os processos em execução

HDD/SSD: onde armazenamos arquivos para serem acessados posteriormente.

**Memória lógica** é a manipulada e invisível pelos programas, sempre que uma aplicação necessita de memória, esse recurso é utilizado.

**Memória física** são circuitos eletrônicos que irão realmente armazenar os dados.

![Alocação Contínua](/media/sistemas_operacionais/alocacao-continua.jpeg)

## Gerenciamento sem permuta

### Alocação Contígua

Os primeiros sistemas implementaram uma técnica muito simples onde a memória principal disponível é dividida entre o **Sistema Operacional e o programa em execução**. Como este esquema de gerenciamento é utilizado em sistemas **monoprogramáveis**, temos apenas um processo em execução por vez. Nesta técnica, o tamanho máximo dos programas é limitado à **memória principal disponível**. Para superar esta limitação foi desenvolvido o conceito de **overlay**.

### Overlay

A técnica de overlay utiliza o conceito de **sobreposição**, ou seja, a mesma região da memória será ocupada por módulos diferentes do processo.

A técnica de overlay foi o primeiro uso do conceito de mover partes do processo, entre o disco e a memória principal, que acabaria por gerar as modernas técnicas de gerenciamento de memória onde a divisão dos módulos é totalmente transparente para o usuário.

Esse gerenciamento é de responsabilidade do usuário e, geralmente, é oferecido como um **recurso da linguagem**.

_Em um programa com estrutura de overlay, um módulo fica sempre residente (Módulo Raiz) e os demais são estruturados como em uma árvore hierárquica de módulos mutuamente exclusivos, em relação a sua execução, colocados lado a lado, em um mesmo nível da árvore, de modo que o mesmo espaço possa ser alocado para mais de um módulo, os quais permanecem no disco e serão executados um de cada vez por meio de comandos de chamada (call). Um módulo residente faz chamadas a um módulo de overlay em disco e este é carregado no espaço de overlay sobre outro módulo do mesmo nível que lá estava (daí a necessidade de serem mutuamente exclusivos)._

</br>

![Processo Overlay](/media/sistemas_operacionais/processo-overlay.gif)

</br>

## Alocação Particionada Fixa

Com os sistemas multitarefas surgiu a necessidade de manter mais de um processo de usuário, na memória, ao **mesmo tempo**. A forma mais simples de se conseguir isso consiste em dividir a memória em _n_ partições (possivelmente diferentes) e _alocar_ os diferentes processos em cada uma delas.

Nos primeiros sistemas, estas partições eram estabelecidas na **configuração do sistema operacional** e seu **tamanho** e sua **localização** somente podiam ser alterados realizando um **novo boot**.

Quando um processo inicia, este deve ser alocado em uma partição com tamanho suficiente para acomodá-lo. Duas estratégias podem ser adotadas para alocar o processo:

uma única fila de entrada: Todos os processos ficam na mesma fila e vão sendo alocados na menor partição livre que os possa acomodar.

uma fila por partição: Os processos são divididos em várias filas de acordo com o seu tamanho e alocados quando a partição atendida pela fila está disponível.

</br>

![Alocacao Particionada Fixa](/media/sistemas_operacionais/alocacao-particionada-fixa.jpeg)

</br>

Este método de gerência de memória baseado em partições fixas, de uma forma ou de outra, gera um grande **desperdício de memória**, posto que, um processo ao ser carregado em uma partição, se ele não ocupa todo o seu espaço, o restante não poderá ser utilizado por nenhum outro processo.

</br>

## Alocação com Partições Variáveis

A memória principal não é particionada em blocos de tamanhos predeterminados. Inicialmente apenas uma partição existe e ocupa toda a memória disponível para usuários. À medida que os processos vão sendo alocados, essa partição vai diminuindo até que não caibam mais processos no espaço restante, resultando em um único fragmento.

Quando um processo termina e deixa a memória, o espaço ocupado por ele se torna uma partição livre que o gerente de memória utilizará para alocar outro processo da fila por memória. Uma lista de partições livres é mantida com ponteiros indicando os buracos disponíveis para alocação.

</br>

![Alocacao Particionada Variavel](/media/sistemas_operacionais/alocacao-particionada-variavel.jpeg)
A escolha da partição para o próximo job da fila deverá ser feita de acordo com uma das seguintes políticas:

![Politicas Partição Variavel](/media/sistemas_operacionais/politicas-particao-variavel.gif)

</br>

**First-fit**: Procura alocar o job na primeira partição onde ele couber(a busca termina assim que a primeira região é encontrada). É a mais rápida. Justificativa: **probabilisticamente agrupa os jobs pequenos separando-os dos grandes**.

**Best-fit**: Aloca o job na partição disponível de tamanho mais próximo ao seu (a lista de áreas livres de memória tem que ser totalmente pesquisada). Produz a menor região resto. Justificativa: **busca deixar fragmentos livres menores**.

**Worst-fit**: Procura alocar o job na maior partição disponível onde ele couber (a lista de áreas livres de memória tem que ser totalmente pesquisada). Produz a maior região resto, é a pior das três. Justificativa: **Intuitivamente sempre caberá mais um job pequeno no espaço resultante**.

</br>

## Realocação e Proteção

As políticas de alocação de partição introduzem dois problemas essenciais que devem ser resolvidos: **realocação e proteção**.

**Módulo está em Imagem de Memória ou está com Endereçamento Absoluto** é quando um módulo foi link-editado e seus endereços já estão associados às posições físicas do espaço de memória onde ele será alocado.

Ao conjunto de endereços que um processo faz referências, sejam eles de dados ou de instruções, chamamos de Espaço de Endereçamento. Assim, definimos por _Espaço Lógico de Endereçamento_ ao **conjunto de objetos ou endereços lógicos por ele referenciados** e por _Espaço Físico de Endereçamento_ ao **conjunto de endereços físicos correspondentes**.

Para que um processo possa ser alocado, em qualquer posição da memória, ele **não pode estar com endereçamento absoluto** e, nesse caso, um **mapeamento de endereços deverá ser feito** entre os endereços dos objetos referenciados pelo processo (endereços lógicos) e os endereços absolutos (físicos) no espaço que eles estarão ocupando na memória principal.

Supondo “N” o espaço de endereços lógicos e “M” o espaço de endereços físicos, então o mapeamento de endereços pode ser denotado por uma função do tipo: f: N → M

</br>

### Relocação de memória

É a função que mapeia os endereços lógicos em endereços físicos.

Quando ela é feita pelo link-editor, durante a resolução das referências em aberto, na geração do módulo de carga, os **endereços são resolvidos em relação a uma base inicial e o processo só poderá ser alocado a partir dessa base**, ou seja, _sempre rodará no mesmo lugar da memória_.

Alguns sistemas deixam essa tarefa de relocação para o carregador (loader) ou ligador-carregador (link-loader) que faz a resolução das referências externas e a relocação de endereços no instante de carregar o processo na memória para sua execução.

No primeiro caso (**link-editor**), a carga em imagem de memória sempre **roda no mesmo lugar da memória**, enquanto que, no segundo caso, **pode rodar em qualquer lugar**. Assim, a relocação poderá ser:

**Estática**: Quando o mapeamento de endereços é feito antes do carregamento do módulo, a relocação é dita **estática**.

</br>

**Dinâmica**: Para que a tradução dinâmica de endereços possa ser efetuada é preciso que toda referência seja lógica, isto é, nenhum endereço no programa poderá estar representando uma posição física, pois será mapeado pelo hardware. Esse processo é chamado de **Relocação dinâmica** de endereços.

![Relocação de Memoria](/media/sistemas_operacionais/relocacao-de-memoria.jpeg)

</br>

### Registradores Base e Limite

Quando um processo é carregado na memória, o endereço “inicial” é colocado em um registrador base e todos os endereços de programa são interpretados como sendo relativos ao endereço contido no registrador base. **O mecanismo de transformação, neste caso, consiste em adicionar ao endereço do programa o endereço base, o que produz a localização da palavra de memória correspondente.**

![Registradores Base e Limite](/media/sistemas_operacionais/registradores-base-limite.png)

Consegue-se relocação dinâmica facilmente: **basta mover o programa e corrigir o conteúdo do registrador base**. Proteção pode ser obtida com a _inclusão de um segundo registrador_ (registrador limite) contendo o endereço da última posição de memória que o processo pode acessar.

O mapeamento de endereço realizado pelo mecanismo (por “hardware”) de transformação é assim:

![Mapeamento](/media/sistemas_operacionais/mapeamento.png)

O espaço de endereço mapeado é linear, seu tamanho é a diferença entre o registrador limite e o base. Esse tamanho é necessariamente menor ou igual do que o espaço de memória disponível na configuração da maquina.

![Espaço de endereçamento linear](/media/sistemas_operacionais/enderecamento-linear.png)

Para reduzir o tempo de mapeamento, é conveniente que os registradores base e limite sejam de processo rápido. O custo dos registradores pode ser reduzido e a velocidade aumentada se os bits menos significativos desses registradores forem removidos. Se tal ocorrer, então o espaço de endereços deve ser múltiplo de **2n**, onde **n** é igual ao número de bits removidos.

</br>

## Gerenciamento com permuta

### Swap de memória

Denominamos **swapping** a política de remover um processo da memória toda vez que ele fica bloqueado. Assim que sua condição estiver satisfeita e ele retornar à fila de prontos ele é novamente carregado na memória.

Naturalmente que, para fazer swap, é necessário haver relocação dinâmica durante a carga dos jobs.

O swap de memória possui algumas vantagens e desvantagens. São elas:

VANTAGENS:

Maior compartilhamento da memória (maior throughput de tarefas);

Menor fragmentação de memória;

Boa técnica para ambientes com processos pequenos e poucos usuários.

DESVANTAGENS:

Custo alto para fazer o swap, por ser uma operação com memória auxiliar (disco)

### Memória virtual

O espaço de endereçamento lógico de um programa tem que ser mapeado em um espaço de endereçamento físico de memória.

Essa correspondência pode ser deixada totalmente a cargo do S.O., de forma que o programa não tenha nenhuma responsabilidade em se ater a um determinado tamanho de memória física disponível.

O conjunto de endereços que um programa pode endereçar, pode ser muito maior que a memória física disponível para o processo, em um determinado momento, ou mesmo que o total de memória fisicamente disponível na máquina. A esse conjunto de endereço chamamos de _espaço de endereçamento virtual_. Ao conjunto de **endereços reais de memória** chamamos _espaço de endereçamento real_.

Como os programas podem ser maiores que a memória física, somente uma parte de cada programa pode estar na memória durante a execução. As partes que não são necessárias em um determinado instante, ficam em disco e só são carregadas quando se tornarem necessárias. Todo o processo é transparente para o usuário e mesmo para os compiladores e link-editores, pois estes trabalham apenas com o espaço de endereçamento virtual. Apenas o S.O. se incube de carregar ou descarregar as partes necessárias e mapeá-las no espaço de endereçamento real durante a execução.

![Alocação com permuta](/media/sistemas_operacionais/permuta.png)

Como consequência desse mapeamento o programa não precisa estar nem mesmo em regiões contíguas de memória. O nível de fracionamento do programa deve ser escolhido de forma a **não comprometer o desempenho**, à medida que a tarefa de mapeamento é feita pelo S.O., juntamente com recursos de hardware. A memória (tanto virtual como real) é dividida em blocos e o S.O. mantém tabelas de mapeamento para cada processo, que relacionam os blocos da memória virtual do processo com os blocos da memória real da máquina.

</br>

### Paginação

O espaço de endereços é dividido em blocos de igual tamanho que chamamos de páginas. A memória principal também é dividida em blocos de mesmo tamanho (igual ao tamanho da página) denominados molduras.

Esses blocos de memória real são compartilhados pelos processos, de forma que a qualquer momento, um determinado processo terá algumas páginas residentes na memória principal (as páginas ativas), as restantes na memória secundária (as páginas inativas). O mecanismo da paginação possui duas atribuições:

Executar a operação de mapeamento, isto é, determinar qual página referenciada e em que bloco de memória (se for o caso) ela se encontra.

Transferir páginas da memória secundária para os blocos da memória principal (quando for requerido) e guardá-las de volta na memória secundária quando elas não estiverem em uso.

Com o objetivo de determinar qual a página referenciada por um endereço de programa, interpreta-se os bits mais significativos do endereço virtual como sendo o número da página dentro de uma tabela de páginas que é mantida pelo S.O. para cada processo ativo. Já os bits menos significativos indicam a localização da palavra na página selecionada:

![Paginação](/media/sistemas_operacionais/paginacao.png)

Se o tamanho da página é **2^n** palavras, então, os **n** bits menos significativos do endereço de programa representam o deslocamento, e os bits restantes indicam o número da página. O número total de bits do endereço de programa é suficiente para endereçar inteiramente a memória virtual.

A divisão de um endereço de programa no par (número de página, deslocamento) é feita pelo hardware e é completamente transparente ao programador.

![Mapeamento paginação](/media/sistemas_operacionais/mapeamento-paginacao.jpeg)

Se chamarmos de Z o tamanho da página, então: “p” é o quociente e “d” o resto da divisão de “a” por Z.

EXEMPLO:

Páginas com 16 endereços, logo, 4 bits de endereçamento;

Endereços virtuais de até 10 bits, logo, 1024 endereços;

Memória física de 256 endereços.

Então, se quiséssemos acessar o endereço binário 0010010111 a composição, pelo esquema acima, seria:

Os quatro últimos bits (0111) são o deslocamento d dentro da página;

Os seis primeiros bits (001001) são o número da página.

Como temos 1024 endereços e páginas de 16 endereços, então temos 1024/16= 64 páginas na tabela de páginas.

Como temos 256 endereços reais, então temos 256/16 = 16 blocos físicos de memória (blocos de 0 a 15).

![Exemplo mapeamento paginado](/media/sistemas_operacionais/exemplo-mapeamento-paginado.jpeg)

</br>

### Page fault

Normalmente, o número de blocos alocados a um processo é menor do que o número de páginas que ele usa. Por isso é possível que um endereço de programa referencie uma **página ausente**. Nesse caso, a entrada (da tabela) correspondente estará “vazia” e uma interrupção do tipo **falta de página (page fault)** é gerada sempre que uma página inativa é requerida.

_Uma interrupção é um evento externo que faz o processador parar a execução do programa corrente e desviar a execução para um bloco de código chamado rotina de interrupção. Ao terminar o tratamento de interrupção o controle retorna ao programa interrompido, exatamente, no mesmo estado em que estava quando ocorreu a interrupção._

![Page Fault](/media/sistemas_operacionais/page-fault.jpeg)

A interrupção faz com que o mecanismo da paginação inicie a transferência da página ausente da memória secundária para um dos blocos da memória principal e atualize a tabela de páginas.

O processo muda de estado, ficando bloqueado até que a transferência chegue ao fim.

As páginas são transferidas da memória secundária para a principal apenas quando são referenciadas, isso é chamado de **paginação por demanda**.

O sistema tenta prever quais páginas serão referenciadas pelo programa, trazendo-as para a memória antecipadamente, evitando assim a ocorrência do page fault, isso é **paginação antecipada**.

A posição ocupada por uma página na memória secundária é guardada em uma tabela separada ou na própria tabela de páginas. No último caso, é necessário um “bit de presença” para cada entrada da tabela de páginas, indicando se a página está ativa (está na memória física) ou não.

Se não houver nenhum bloco de memória disponível então é necessário desocupar um dos blocos para a página cuja presença está sendo solicitada. A escolha do bloco é função do **algoritmo de troca**. A transformação de endereços é função do hardware, enquanto que o algoritmo de troca é feito pelo software.

![Desoculpação de blocos](/media/sistemas_operacionais/desoculpacao-blocos.jpeg)

</br>

### Políticas de paginação

Para minimizar a ocorrência de page faults surgiu o conceito de working set.

Working set é o conjunto de páginas mais acessadas por um determinado processo.

Quando um programa começa a executar, a possibilidade de que ele requisite páginas que não estão na memória é muito grande. Entretanto, à medida que mais páginas vão sendo carregadas, a ocorrência de page faults vai diminuindo, devido ao princípio da localidade dos programas, já explicado quando falamos de memória cache.

**Capacidade**: quanto mais páginas no working set menos processos podem estar carregados ao mesmo tempo.

**Velocidade**: quanto mais páginas no working set menos page fault ocorrem, logo, melhor desempenho.

Definido o working set, resta definir qual deve ser a página a retirar da memória quando ocorre um page fault e uma página precisa ser carregada.

Antes de descartar qualquer página, o S.O. precisa saber se houve alguma alteração na página enquanto ela esteve na memória. Se houve, então ela precisa ser salva em disco antes de ser descartada, para que nenhum dado se perca. O S.O. mantém um bit na tabela de páginas chamado bit de modificação. Caso o bit indique que houve mudança, a página é salva em um arquivo de paginação, onde poderá ser futuramente resgatada.

As políticas de liberação de páginas são:

**Página aleatória**: escolhe-se simplesmente qualquer página. A desvantagem é que pode se escolher uma página que seja muito acessada.

**First-in-first-out**: retira-se a página carregada há mais tempo. A desvantagem é que pode retirar páginas que são acessas periodicamente.

**Least-recently-used**: retira-se a página utilizada pela última vez há mais tempo. A desvantagem é o overhead causado pela necessidade a cada acesso de atualização do momento em que a página foi acessada.

**Not-recently-used**: a página não utilizada nos últimos **k** acessos é substituída. A desvantagem também é o overhead causado pela necessidade, a cada acesso, de atualizar um contador de acessos à página.

**Least-frequently-used**: escolhe-se a página que tenha o menor número de acessos descritos em um contador de acessos. A ideia é manter, na memória, as páginas que são muito acessadas, entretanto, o problema é que páginas recém-carregadas no working set terão baixo número de acessos e serão indesejavelmente cotadas para serem retiradas.

VANTAGENS:

aumenta o espaço de endereçamento do processo;

admite código reentrante e compartilhamento de código pelos processos.

DESVANTAGENS:

overhead devido ao excesso de page faults tratados pelo sistema;

ocupa um arquivo só pra E/S de páginas;

ocupa muita memória do SO para as tabelas de páginas dos processos.

</br>

## Administração de Memória por Segmentação

A segmentação surgiu como uma alternativa de gerência de memória onde o programa agora não mais é dividido em blocos de comprimentos fixos (as páginas), mais sim, em segmentos de comprimentos variados, mas com um sentido lógico, isto é, **a paginação procedia a uma divisão física do programa e, às vezes, isso leva a um número muito grande de page faults por não observar suas características lógicas**.

A segmentação busca aproveitar exatamente essas características, agrupando em um segmento partes do programa que se referenciam mutuamente e que quando trazidas à memória estarão todas juntas não causando, o que nesse caso é chamado de **segment faults**, com tanta frequência.

O espaço de endereços torna-se bidimensional: endereços de programa são denotados pelo par (nome do segmento, endereço dentro do segmento). Para facilitar a implementação do mecanismo de transformação de endereços, o S.O. troca o nome do segmento por um nº, quando o segmento é referenciado pela primeira vez.

Considerando o par (s,d) como sendo um endereço de programa generalizado, onde s = número do segmento e d = endereço dentro do segmento, então o esquema de geração seria:

![Administração de Memória por Segmentação](/media/sistemas_operacionais/segmentacao.png)

A transformação de endereço é realizada por intermédio de uma **tabela de segmentos (uma tabela para cada processo)**. A s-ésima entrada da tabela contém o tamanho (l) e a posição inicial (a) da memória, onde o s-ésimo segmento foi carregado. As entradas da tabela são chamadas de “descritores de segmento”. O algoritmo de mapeamento é:

`extrair endereço de programa (s,d);`

`usar “s” para indexar tabela de segmentos;`

`retirar o endereço inicial do segmento (a);`

`se d < 0 ou d > l então “violação de memória”;`

`a + d é o endereço requerido.`

A busca de espaços para um segmento a ser trazido à memória nos leva novamente aos problemas de gerência por partições variáveis. A diferença aqui é que o espaço contíguo só é necessário para o segmento e não para todo o processo.

VANTAGENS:

reduz o número de page faults dentro de um segmento;

aproveita as características lógicas do processo;

dispensa uso de arquivo de paginação (ou segmentação)

DESVANTAGENS:

a soma de s + d, na tradução de endereços é mais lenta que a concatenação **p** e **d** na paginação;

a administração das áreas livres de memória é mais complicada (partições variáveis) e, portanto mais lenta;

as page faults (tratadas mais rapidamente, pois as páginas eram menores) são substituídas por segment faults que são maiores em comprimento.

</br>

### DIFERENÇA ENTRE SEGMENTAÇÃO E PAGINAÇÃO

A diferença principal entre a segmentação e a paginação é que a primeira busca uma divisão lógica do espaço de endereçamento do processo enquanto que a segunda busca uma divisão física desse espaço, ambas para implementação de uma política de memória virtual de um único nível.

Páginas têm seu tamanho determinado pelo tamanho da palavra, enquanto que segmentos têm seu tamanho determinado pelo tamanho da memória disponível.

</br>

## Administração por Segmentação com Paginação

Nem sempre é possível manter todos os segmentos na memória principal. Segmentos muito grandes poderiam, eventualmente, ultrapassar a memória disponível da máquina.

![Administração por Segmentação com Paginação](/media/sistemas_operacionais/administracao-por-pagina.png)

Em tempo de execução, alguns trechos de um segmento estariam na memória principal e outros não. A entrada da tabela de segmentos, isto é, o descritor de um segmento, apontaria para uma tabela de páginas (do segmento) ou então estaria vazia.

Vantagens do uso de paginação de implementação da segmentação:

não é necessário manter todas as páginas de um segmento na memória - apenas aquelas usadas correntemente.

as páginas de um segmento não precisam ser carregadas em áreas contíguas, isto é, podem ser dispersadas pela memória.
