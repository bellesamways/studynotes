# Aula 9 - MEMÓRIA (PARTE 2)

## Memória Principal

Normalmente é chamada de RAM (Random Access Memory, em português Memória de Acesso Aleatório).

### Estrutura Processador/Memória Principal

Leitura (sinal READ): Para recuperar um conteúdo armazenado. Esta ação não elimina o conteúdo da memória.
Escrita (sinal WRITE): Para armazenar informações na memória. Esta ação elimina o conteúdo da memória, gravando uma informação por cima.

Dentro do processo de gravação, são utilizados:
- Barramentos de Controle;
- Endereços e Dados;
- Unidade de Controle (UC);
- Registradores de Endereço de Memória (REM);
- Registrador de Dados de Memória (RDM).

![Estrutura Processador/Memória Principal](/media/processador_memoria_principal.png)

### Processo de leitura

1. A CPU armazena no REM o endereço da posição, onde a informação a ser lida está localizada;
2. A CPU comanda uma leitura (sinal de controle para memória - READ), pelo barramento de controle;
3. O conteúdo (Palavra) da posição identificada pelo endereço armazenado no REM, então, é transferido para o RDM e a partir dele enviado para a UCP, pelo barramento de dados.

### Processo de escrita

1. A CPU envia, para o REM, o endereço da memória onde a palavra será gravada e, para o RDM, a informação (Palavra) da posição a ser gravada;
2. A CPU comanda uma gravação (sinal write) pelo barramento de controle;
3. A palavra armazenada no RDM é, nesse momento, transferida para a posição de memória, cujo endereço está no REM.

### Células e Endereços

Quando se diz célula, queremos dizer a unidade de armazenamento do computador na Memória Principal, sendo a menor unidade da memória que pode ser endereçada, pois não é possível buscar uma parte da célula, e sim a célula no seu todo, que possui um tamanho fixo, de acordo com a máquina e sua construção.

Porém, na atualidade, se baseia em células de 8 bits, ou seja, 1 byte, que são identificadas por um Endereço único, onde a CPU se referencia  ao tentar acessar, seja para consulta ou para gravação pelo Sistema Operacional. As células são numeradas sequencialmente, de 0 a m-1. **Endereço é o localizador da célula, que permite identificar univocamente uma célula.**

![Células e Endereços](/media/celulas_endereços.png)

A Memória Principal é assim organizada em unidade de armazenamento, formada por este conjunto de células.

Em geral, para se representar o endereço, é utilizado o tamanho máximo da PALAVRA do computador. Normalmente, o tamanho máximo do Registrador, endereço este que irá trafegar no Barramento de Endereços, já estudado em aulas anteriores.

### Representação do endereço

É a quantidade de bits necessária para representar a quantidade de memória. Se analisarmos desta maneira, sabemos que 1 bit consegue representar 2 endereços de memória, ou seja, 0 e 1. Sendo assim, podemos considerar algumas fórmulas para facilitar a representação de endereços de células na Memória Principal.

Fórmulas: Quantidade células possíveis para de se endereçar com x bits.

![Representação do endereço](/media/representacao_endereco.png)

### Capacidade de memória

Deve-se calcular o número total de endereços (total de células) x tamanho de cada célula de memória.

Exemplo:
Total de Endereços: 1024 / Tamanho da célula: 8 bits (ou 1 byte).
Tamanho MP: 1024 bytes.

Sabendo que o processador é de 32 Bits e sua PALAVRA é de 32 bits, o registrador também poderá endereçar no máximo 32 bits em endereço de memória. Sendo assim, 2^32 = 4294967296 células de memória de 8 Bits, que equivalem a um total de 4 Gigabytes.

### Classificações da memória

**Quanto à forma de acesso:**

- **Aleatória (RAM):** Significa que o tempo de acesso será o mesmo, independentemente de onde se encontra a célula. O termo acesso aleatório se relaciona à capacidade de acesso em qualquer posição de memória e em qualquer momento para gravação e leitura de conteúdo.
- **Não aleatório (Memórias Secundárias):** O tempo de acesso dependerá de onde o dado se encontra e tem relação com o acesso sequencial, imposto por alguns dispositivos de armazenamento, como uma unidade de fita.

**Quanto ao acesso de leitura e escrita:**

- **R/W:** Read and Write ou memória de leitura e escrita. Este tipo de memória permite operações de escrita e leitura pelo usuário e pelos programas. É uma memória volátil, ou seja, perde seu conteúdo na falta de energia.
- **ROM:** Read Only Memory ou memória apenas de leitura. Esta memória permite apenas a leitura. Seu conteúdo, uma vez gravado, não pode mais ser alterado. Foi muito utilizado inicialmente por fabricantes de computadores para gravar programas que não deviam ser apagados (por exemplo a BIOS - Basic Input Output System de computadores). É um tipo de memória não volátil.
- **PROM:** Programmable Read Only Memory ou memória apenas de leitura, programável. Esta memória é uma ROM Programável. Diz-se programável pois ela poderia ser comprada “virgem”, sem conteúdo, e, uma vez gravado o conteúdo com os gravadores de PROM, não podiam mais ser alterados.
- **EPROM:** Erasable Programmable Read Only Memory ou memória apenas de leitura. Assim como a PROM, poderia ser gravado com os gravadores de PROM apropriados, mas poderiam também ter seu conteúdo apagado utilizando-se máquinas específicas, baseadas em raios ultravioleta. Não foi muito utilizado depois da chegada da EEPROM.
- **EEPROM (E2PROM):** Electrically Erasable Programmable Read Only Memory ou memória apenas de leitura, programável e eletronicamente alterável. Também chamada EAROM (Electrically Alterable ROM). Esta sim é uma memória EPROM, agora apagável por processo eletrônico, com equipamento e programas adequados. Apesar de mais cara, é geralmente utilizada em dispositivos em que se deseja permitir alteração, possibilitando a carga de novas versões de programas ou então para possibilitar a reprogramação dinâmica de funções específicas de um determinado programa ou equipamento. Atualmente, grande parte dos equipamentos, sejam eles notebooks ou desktops, possuem sua atualização de BIOS ou Firmware baseado em EEPROM, em que sua atualização não depende da troca de hardware, mas somente da execução de um programa que faz toda a sua alteração eletrônica.
- **FLASH:** Um tipo específico de EEPROM, que é escrita e apagada em blocos, ao contrário das EEPROMs convencionais, em que é possível apagar cada byte, ao invés de grandes blocos de dados. EEPROMs convencionais são bem mais caras. Poderiam ser utilizadas para substituir os discos rígidos, porém se desgastam após serem apagadas 100 mil vezes. Ao passo que discos duram muitos anos, não importando quantas vezes sejam reescritos. O custo do byte armazenado em uma memória flash também é bem maior do que o custo do byte em um disco rígido convencional, como pode ser visto hoje com os discos SSD.

**Quanto à tecnologia de construção:**

- **SRAM (Static RAM):** São memórias de conteúdo estático, que não dependem de atualizações periódicas de alimentação de energia para manterem os valores armazenados. Estes tipos de memória, por serem mais rápidas e de custo mais elevado, são utilizadas principalmente na construção de memórias cache.
- **DRAM (Dynamic RAM):** Essas memórias têm tempo de acesso maior, na faixa de 60ns e são as mais comuns hoje em dia. A Memória Principal normalmente emprega essa tecnologia. Como seu conteúdo é perdido em alguns instantes, elas precisam ser periodicamente atualizadas (ciclo de “refresh”) e com alimentação constante de energia, o que faz com que fiquem indisponíveis para novas transferências em intervalos regulares. São as memórias utilizadas na construção da memória RAM.

## Memória secundária

Memórias secundárias ou memórias auxiliares são dispositivos de armazenamento em massa, não deixando de ser importantes no subsistema de memória, principalmente na resolução de problemas de armazenamento de grande quantidade de informações, bem como pelo falo de serem memórias não voláteis, ou seja, a informação não é perdida quando a mesma perde a alimentação de energia elétrica.
Lembrando que uma das principais características dos dispositivos que constituem as memórias secundárias é sua NÃO VOLATILIDADE, isto é, não dependem de estar energizados para manter seu conteúdo gravado.

**Características importantes**

- **Tempo de acesso:** O acesso a um dado no disco rígido, por exemplo, depende do deslocamento do braço que contém a leitora e do movimento de rotação do disco. Dessa forma, todos os processos mecânicos a serem executados por esses dispositivos jamais se compararão em termos de velocidade a um acesso aleatório de uma célula da Memória Principal, que depende apenas de um sinal elétrico para localizar um conteúdo na memória.
- **Capacidade:** Um dos grandes atrativos dos dispositivos de Memória Secundária é sua alta capacidade de armazenamento, que chegam a dezenas e até centenas de GBytes.
- **Volatilidade:** Como esses dispositivos armazenam as informações de forma magnética ou ótica, elas não se perdem nem desaparecem quando não há alimentação de energia elétrica.

**Disco Rígido:** Em termos de Memória Secundária, ainda é muito utilizado o Disco Rígido, formado por uma estrutura eletromecânica de discos de platina, em que a leitura é feita por um cabeçote, que, através da indução, efetua a leitura dos dados, sem efetivamente ter o contato físico com o disco. Apesar de ainda ser o mais utilizado, oferece riscos maiores para falhas por ser um dispositivo eletromecânico. Por isso, a cada dia cresce o uso dos discos SSD (Solid State Disk), que são discos puramente eletrônicos, formados por células de memória flash e que não dependem de dispositivos eletromecânicos para seu funcionamento.

Basicamente, a função principal dos discos HDD (Hard Disk Drive) e SSD (Solid State Drive) são as mesmas, ou seja, o armazenamento de grande volume de dados não volátil.

A principal desvantagem do SSD em relação ao HD ainda hoje é o preço devido ao fato de que o SSD é uma tecnologia puramente eletrônica, em que discos magnéticos foram trocados por memórias flash, de forma que o custo por GB de armazenamento ainda é mais caro.

Porém, os SSDs se destacam quando o assunto é velocidade. Em uma pequena comparação com um HDD, o tempo de boot de um sistema operacional Windows em um mesmo equipamento cai para menos da metade em um disco SSD.