# Aula 7 – Armazenamento de massa

## Estrutura de armazenamento de massa

![Armazenamento de massa](/media/sistemas_operacionais/armazenamento-de-massa.png)

## Discos Magnéticos

Discos magnéticos são dispositivos para armazenamento não volátil de dados.

Os atuais discos magnéticos ou discos rígidos incorporam eletrônica de controle, motor para girar o disco, cabeças de leitura / gravação e o mecanismo para o posicionamento das cabeças.

\*Armazenamento não volátil: Tipo de armazenamento que independe de alimentação de energia para manter seu conteúdo e, portanto permanece gravado mesmo após ser desligado o computador, mas que pode, a critério do usuário, ser apagado ou alterado.

![Disco magnetico](/media/sistemas_operacionais/disco-magnetico.png)

Os discos possuem um formato circular. Suas duas superfícies são cobertas com um material magnético.

![Formato disco magnetico](/media/sistemas_operacionais/formato-disco-magnetico.png)

Durante a formatação, cada superfície é dividida em trilhas e cada trilha é dividida em setores (também chamados de bloco do disco), onde são armazenadas as informações.

\*Formatação: O processo de marcação magnética das trilhas e dos setores, em um disco, faz parte da "formatação" do disco. Esta formatação é dependente do sistema operacional que usará o disco.

![Trilha disco magnetico](/media/sistemas_operacionais/trilha-disco-magnetico.png)

As informações são lidas ou escritas através de uma cabeça de leitura/gravação.

## Tempo de acesso ao disco

É definido como o período decorrido entre a ordem de acesso e o final da transferência dos dados. Ele não é constante e varia em função da localização dos bancos no disco. O tempo de acesso pode ser definido com a seguinte fórmula:

![Formula tempo de acesso](/media/sistemas_operacionais/formula-tempo-de-acesso.png)

Os discos rígidos atuais são construídos com muitas superfícies de gravação, montadas em torno de um eixo comum. Os braços atuadores responsáveis pelo posicionamento das cabeças de leitura/gravação são montados em uma única estrutura, de forma que eles se movam solidariamente.

![Formula tempo de acesso](/media/sistemas_operacionais/funcionamento-disco-magnetico.png)

Observe que quando uma determinada cabeça é posicionada sobre uma trilha, as demais cabeças estarão também posicionadas sobre as trilhas das outras superfícies localizadas à mesma distância do eixo central e, portanto, todas as trilhas (localizadas a uma mesma distância do eixo central do disco) poderão ser acessadas simultaneamente por todas as cabeças.

Surge, neste caso, o conceito de cilindro: O conjunto de trilhas localizado a uma mesma distância do eixo central. Desta forma, em um disco de quatro cabeças (quatro faces) o cilindro 10 seria composto por todos os setores localizados na trilha 10 da face 1, na trilha 10 da face 2, na trilha 10 da face 3 e na trilha 10 da face 4.

Os dados gravados no mesmo cilindro (na mesma trilha, porém em superfícies diferentes) podem ser acessados (lidos ou gravados) sem que o braço atuador das cabeças de leitura/gravação tenha que ser movido.

</br>

## Gerenciamento de espaço livre em disco

### Mapa de bits

Cada bloco é representado por 1 bit, se o bloco está livre o bit é 0, se não é 1.

### Lista de blocos livres

Mantém todos os blocos livres ligados por uma lista, e guardar a cabeça (endereço inicial da lista) da lista. Aproveita os próprios blocos livres para armazenar os endereços da lista. Não é possível ter uma visão geral sobre a situação de um conjunto de setores, deve-se ler um a um, para saber se o setor está disponível ou não.

![Lista de blocos livres](/media/sistemas_operacionais/lista-de-blocos-livres.png)

### Bloco de Endereços

Utiliza-se o primeiro bloco livre, como bloco de endereços, para armazenar o endereço dos próximos "n" blocos livres, sendo que o bloco número "n", é outro bloco de endereços.

Guarda-se o endereço do primeiro bloco de endereços. Este método também permite, em uma única leitura (do bloco de endereços), saber sobre a situação de vários blocos, incluindo os endereços.

![Lista de blocos endereços livres](/media/sistemas_operacionais/bloco-de-enderecos.png)

</br>

### Lista de Blocos Livres contíguos

Aproveita a ideia de que sempre existem vários blocos livres contíguos. Mantém uma tabela de blocos livres, onde cada entrada, na tabela, contém o endereço do 1º bloco de um grupo de blocos contíguos e o tamanho do grupo.

![Lista de Blocos Livres contíguos](/media/sistemas_operacionais/bloco-de-enderecos.png)

## Alocação de espaço em disco

Uma das preocupações do sistema de arquivos é como alocar os espaços livres do disco para os arquivos, de forma que o disco seja mais bem utilizado e os arquivos possam ser acessados mais rapidamente.

Os três principais métodos de alocação de espaço do disco são:

### 1º alocação contígua

Este método procura identificar uma sequência contínua de blocos que apresente um tamanho suficiente para armazenar todas as informações relativas ao arquivo, ou seja, caso um arquivo precise de N blocos para o seu armazenamento, o sistema operacional procurará identificar uma sequência contínua de N blocos livres do disco.

Nesta técnica, o espaço só será alocado se for contíguo, caso contrário, o arquivo não poderá ser armazenado ou estendido. Se, por acaso, existir mais de uma possibilidade, então poderá ser utilizada uma técnica para selecionar uma opção.

As técnicas que podem ser utilizadas são: Worst-Fit, Best-Fit e First-Fit.

A alocação contígua de um arquivo é definida pelo endereço do primeiro bloco e seu comprimento, e, dessa forma, é colocada no diretório.

![Alocação contígua de arquivos](/media/sistemas_operacionais/alocacao-continua-arquivo.png)

### 2ª alocação ligada

Nesta técnica, os blocos alocados para um arquivo são encadeados em uma lista, não importando a contiguidade. Assim, seria armazenado no diretório o nome do arquivo e duas variáveis, isto é, os identificadores do primeiro e do último bloco do arquivo.

Em cada um dos blocos utilizados pelo arquivo, seria reservado um espaço para conter o endereço do próximo bloco da lista.

![Segunda alocação ligada](/media/sistemas_operacionais/segunda-alocacao-ligada.png)

### 3ª alocação indexada

Neste método, cada arquivo possui seu próprio bloco de índice, que é um vetor de endereços. A i- ésima entrada no bloco de índice aponta para o i-ésimo bloco do arquivo.

![Terceira alocação ligada](/media/sistemas_operacionais/terceira-alocacao-ligada.png)

## RAID

É a sigla para Redundant Array of Independent Disks ou, em tradução livre, algo como "Matriz Redundante de Discos Independentes". Trata-se, basicamente, de uma solução computacional combinando vários discos rígidos (HDs) para formar uma única unidade lógica de armazenamento de dados.

![RAID](/media/sistemas_operacionais/raid.png)

### Níveis de RAID

Para que um sistema RAID seja criado, é necessário utilizar pelo menos dois HDs (ou SSDs). Mas não é só isso: é necessário também definir o nível de RAID do sistema. Cada nível possui características distintas justamente para atender às mais variadas necessidades.

**RAID 0 (zero)**

Também conhecido como _striping_ (fracionamento), é aquele onde os dados são divididos em pequenos segmentos e distribuídos entre os discos.

Trata-se de um nível que não oferece proteção contra falhas, já que nele não existe redundância. Isto significa que uma falha, em qualquer um dos discos, pode ocasionar perda de informações para o sistema todo, especialmente porque "pedaços" do mesmo arquivo podem ficar armazenados em discos diferentes.

O foco do RAID 0 acaba sendo o desempenho, uma vez que o sistema praticamente soma a velocidade de transmissão de dados de cada unidade. Assim, pelo menos teoricamente, quanto mais discos houver no sistema, maior é a sua taxa de transferência.

![RAID control](/media/sistemas_operacionais/raid-control.png)

</br>

**RAID 1**

O RAID 1 é, provavelmente, o modelo mais conhecido. Nele, uma unidade "duplica" a outra, isto é, faz uma "cópia" da primeira, razão pela qual o nível também é conhecido como _mirroring_ (espelhamento).

Com isso, se o disco principal falhar, os dados podem ser recuperados imediatamente porque existem cópias no outro.

Perceba que, por conta desta característica, sistemas RAID 1 devem funcionar em pares, de maneira que uma unidade sempre tenha um "clone".

O nível RAID 1 é claramente objetivado na proteção dos dados, ou seja, não torna o acesso mais rápido. Na verdade, pode até ocorrer uma ligeira perda de desempenho, uma vez que o processo de gravação acaba tendo que acontecer duas vezes, uma em cada unidade.

![RAID control por unidade](/media/sistemas_operacionais/raid-control-unidade.png)

**RAID 0+1 e RAID 10**

Tal como você já deve ter imaginado, o nível RAID 0+1 é um sistema "híbrido" (hybrid RAID), ou seja, que combina RAID 0 com RAID 1. Para isso, o sistema precisa ter pelo menos quatro unidades de armazenamento, duas para cada nível. Assim, tem-se uma solução RAID que considera tanto o aspecto do desempenho quanto o da redundância.

![RAID control hibrido](/media/sistemas_operacionais/raid-control-hybrid.gif)

Há uma variação chamada RAID 10 (ou RAID 1+0) de funcionamento semelhante. A diferença essencial é que, no RAID 0+1, o sistema se transforma em RAID 0 em caso de falha; no RAID 1+0, o sistema assume o nível RAID 1.

![RAID com variação](/media/sistemas_operacionais/variacao-raid.gif)

**RAID 5**

É outro nível bastante conhecido. Nele, o aspecto da redundância também é considerado, mas de maneira diferente: em vez de existir uma unidade de armazenamento inteira como réplica, os próprios discos servem de proteção. Deste modo, pode-se inclusive montar o sistema com quantidade ímpar de unidades. Mas, como isso é possível? Com o uso de um esquema de paridade.

Neste método de proteção, os dados são divididos em pequenos blocos. Cada um deles recebe um bit adicional — o bit de paridade — de acordo com a seguinte regra: se a quantidade de bits '1' do bloco for par, seu bit de paridade é '0'; se a quantidade de bits '1' for ímpar, o bit de paridade é '1'.

![Bloco de RAID](/media/sistemas_operacionais/blocos-de-raid.png)

As informações de paridade — assim como os próprios dados — são distribuídas entre todos os discos do sistema. Via de regra, o espaço destinado à paridade é equivalente ao tamanho de um dos discos.

A partir daí, se em uma tarefa de verificação o sistema constatar, por exemplo, que o bit de paridade de um bloco é '1', mas ali há uma quantidade par de bits, percebe que há um erro.

Se houver apenas um bit com problema e se o sistema conseguir identificá-lo, conseguirá substituí-lo imediatamente. A restauração dos dados poderá ser feita inclusive depois de o HD ter sido trocado.

![Troca de bit](/media/sistemas_operacionais/troca-de-bit.png)

Como exemplo, imagine um bloco de dados com os bits '110X' e paridade '1'. O X indica um bit perdido, mas será que ele é '0' ou '1'? Como a paridade é '1', significa que o bloco é composto por quantidade ímpar de bits '1'. Logo, se X fosse '0', a paridade também deveria ser '0', pois ali existiria quantidade par de bits '1'. Isso significa que o bit X só pode ser '1'.

![Raid Controller](/media/sistemas_operacionais/raid-controller.gif)

### Implementação de RAID

Antigamente, montar sistemas RAID não era uma tarefa das mais simples e seu uso normalmente se limitava a servidores. Hoje, no entanto, é possível implementá-los até mesmo em computadores pessoais, mesmo porque praticamente qualquer sistema operacional moderno (Windows, Linux, Mac OS X, entre outros) suporta este recurso.

A maneira mais fácil de fazer isso é adquirindo uma placa-mãe contando com uma controladora RAID. Em poucas palavras, este dispositivo, que pode funcionar com interfaces PATA, SATA ou SCSI, identifica as unidades de armazenamento conectadas e as fazem trabalhar como um sistema RAID. Sua configuração geralmente é feita a partir do setup do BIOS, embora algum software de controle possa ser fornecido para funcionar no sistema operacional.

Se a placa-mãe não possuir controladora RAID, é possível adicionar placas que acrescentam esta função. Estes dispositivos, normalmente, podem ser encontrados utilizando interface PCI ou PCI Express.
