# Aula 10 - DISPOSITIVOS DE E/S

## O que são dispositivos de entrada e saída?

São considerados dispositivos de entrada e saída todos aqueles equipamentos de computação que, sendo interligados ao sistema de computação, possam inserir e extrair informação do mesmo.  

## Dispositivos de Entrada

![Dispositivos de Entrada]("/media/dispositivos_entrada.png")

## Dispositivos de Saída

![Dispositivos de Saída]("/media/dispositivos_saida.png")

Independente da finalidade, a função de dispositivos de E/S sempre será receber ou enviar informações ao meio exterior de um sistema de computação, convertendo as informações obtidas (de entrada ou de saída) em uma forma inteligível para a máquina (se estiver recebendo dados) ou para o usuário (se estiver enviando).

Para E/S, também são necessários barramentos de comunicação, pois é através deles que se pode interligar todos os componentes do sistema de computação.

## Tipos de transmissão

**Transmissão serial:** Na transmissão serial, o periférico é conectado ao dispositivo controlador (veremos posteriormente) ou interface de E/S por uma única linha de transmissão de dados. Nesse tipo de transmissão, a informação é transmitida/recebida bit a bit e, por não haver necessidade de controle e gerenciamento como o paralelo, é de fácil controle e implementação. Por essa facilidade, o uso deste tipo de transmissão, bem como tecnologias disponíveis, têm crescido consideravelmente. Por exemplo, a porta USB (Universal SERIAL Bus, ou barramento SATA - SERIAL ATA), são tecnologias padronizadas no uso de equipamentos.

![Transmissão serial]("/media/transmissao_serial.png")

**Transmissão paralela:** Na transmissão em paralelo, um grupo de bits é transmitido de cada vez, cada um sendo enviado por uma linha separada de transmissão. A informação é transmitida/recebida em grupos de bits de cada vez, simultaneamente. Por ser feita dessa forma, os sinais de cada linha de barramento precisam chegar simultaneamente. Sendo assim, é difícil de controlar, pois os mecanismos de verificação desse “paralelismo” têm de custo elevado.

![Transmissão paralela]("/media/transmissao_paralela.png")

## Controladora de E/S

A CPU e Memória Principal não se comunicam diretamente com o periférico, necessitando de uma interface de comunicação entre CPU/MP e o periférico, conhecidos normalmente como controladoras de E/S.

![Controladora de E/S]("/media/controladora_e-s.png")

Esses dispositivos ficam interligados através de barramento ou “bus” e normalmente possuem unidades de memória (registradores) para comunicação com a CPU, que se comunica com sua controladora, responsável por converter o fluxo de bits em um bloco de bytes, executando também as correções de erros necessárias e tornando os dados disponíveis para serem copiados para a MP.

As controladoras de E/S são um hardware que controla uma porta, barramento ou dispositivo e sua comunicação com a CPU.

### Controladora de E/S - Processo de comunicação

1. Inicialmente, a CPU interroga o dispositivo, enviando o endereço do dispositivo e um sinal dizendo se quer mandar ou receber dados através da controladora;
2. A controladora, reconhecendo seu endereço, responde quando está pronta para receber (ou enviar) os dados;
3. A CPU então irá transferir (ou receber) os dados através da controladora;
4. A controladora responderá à CPU confirmando que:
- Recebeu (ou transferiu) os dados (“Acknowledge” ou ACK); ou
- Não recebeu os dados, neste caso solicitando retransmissão (“Not-acknowledge” ou NAK).

### Device Drivers

Software que permite que o sistema operacional e este dispositivo específico possam se comunicar dentro do processamento da CPU.

Formas de comunicação entre CPU/MP e interface de E/S

Para qualquer tipo de comunicação, sempre há o armazenamento de conteúdo de dados em memória, a fim de que este conteúdo possa ser trafegado durante o processamento.

**Memória compartilhada:** memória principal é compartilhada tanto por instruções e dados comuns de um programa quanto por instruções/dados de operações de E/S. Necessário somente lançar no barramento de controle o comando de leitura/escrita que deve ser executado, pois a memória principal é justamente a memória utilizada neste tipo de operação.
Vantagem: Não necessita de instruções especiais para processamento.
Desvantagem: Ocupa parte do espaço da memória principal para seu processamento.

![Memória compartilhada]("/media/memoria_compartilhada.png")

**Memória isolada:** Consiste em criar um espaço de memória próprio de E/S para aquela operação, não utilizando assim uma parcela da memória principal. Necessário um sinal de identificação a fim de saber se a instrução a ser processada é de E/S ou não, pois o local de armazenamento do conteúdo a ser processado estará em local diferente.
- Vantagem: Não utiliza espaço da memória principal.
- Desvantagem: Necessita de instruções especiais.

![Memória isolada]("/media/memoria_isolada.png")

### Formas de realização de entrada/saída

**E/S programada:** Nesse tipo, a CPU lê constantemente o status do controlador de E/S e verifica se já acabou o processamento (Polling ou Busy-waiting), espera até o fim da operação para dar continuidade aos demais. Há um intenso uso da  CPU, bem como uma ociosidade de tempo, uma vez que o polling faz com que existam momentos de espera no processamento.

**E/S com emprego de interrupção:** Muito utilizada na arquitetura atual, como o próprio nome diz, nesse tipo, a CPU solicita a transferência de um processamento à controladora e desvia-se para outra atividade, sem aguardar que o processamento seja finalizado. Dessa forma, ela pode se preocupar com outros processamentos até que o mesmo seja finalizado pelo dispositivo de E/S, que, ao finalizar, avisa à CPU, por meio de um sinal de interrupção, que faz com que a CPU “desvie” sua atenção para o resultado do processamento requisitado.
**Tipos de interrupção:**
- **Internas:** Geradas pela execução de uma instrução. Exemplo: Divisão por Zero, etc.
- **Externas:** Geradas por um sinal externo à CPU. Utilizadas na comunicação com periféricos.

**Acesso direto à memória (DMA - direct memory access):** Controlador de DMA: Permite a transferência de dados entre uma interface e a MP praticamente sem intervenção da CPU. CPU solicita transferência. Controlador sinaliza final através de interrupção.

### Tratamento de interrupção (Interrupt Handler)

É importante reforçar que cada tipo de interrupção tem um tratamento específico a ser feito.

Se estivermos falando de um click do mouse, o “mecanismo de tratamento” vai verificar que o botão foi pressionado e, dependendo do botão (vamos considerar um mouse de 2 botões), uma operação diferente será executada.

Geralmente, a CPU utiliza o código identificador do botão pressionado para um endereço específico de memória e cada programa irá tomar sua decisão do que será feito quando este “click” for efetuado, seja ele um navegador de internet, um jogo, entre outros aplicativos.

Quando esse processo de interrupção pelo mouse é encerrado, o tratamento também é encerrado, e a CPU volta à execução do programa que havia sido interrompido para tratar o “click” do mouse, restaurando todos os valores, salvos antes da interrupção, e retomando exatamente do ponto em que parou.

#### Tipos de interrupções

- **Maskable interrupt (IRQ):** É uma interrupção de hardware que pode ser ignorada por configurar um bit em um registro da máscara de interrupção (IMR) bit-mask.
- **Non-maskable interrupt (NMI):** É uma interrupção de hardware que carece um bit-mask associado. Então, isso nunca pode ser ignorado. NMIs são frequentemente usados por timers, especialmente por watchdog timers.
- **Inter-processor Interrupt (IPI):** Caso especial gerado por um processador para interromper outro processador em um sistema de multiprocessadores.
- **Software Interrupt:** É uma interrupção gerada dentro de um processador pela execução de uma instrução. Interrupções de software são frequentemente usadas para implementar chamadas de sistema porque elas implementam uma chamada de sub-rotina com a mudança de nível da CPU.

As características dos dispositivos E/S são: Taxa de transmissão, Complexidade de Controle, Representação de dados, Aplicação, Unidade de transferência e Condições de erro. As interrupções podem ser divididas em três classes: relógio, E/S e falha de Hardware.