# Aula 6 - MODELO DE VON NEUMANN

## Conceito de Von Neumann

Se baseava na criação de um modelo de computador em que a máquina possuiria o programa (e suas instruções) armazenado em memória, de forma que os programas em execução poderiam ser alterados durante a execução (uma variável poderia ser alterada em meio à execução) e todas as instruções seriam armazenadas e executadas sequencialmente em memória, de acordo com seu endereçamento.

![Conceito de Von Neumann](/media/conceito_von_neumann.png)

Basicamente, todo e qualquer computador possuiria os seguintes elementos:

- CPU (ou UCP);
- Unidade de memória;
- Unidade de entrada;
- Unidade de saída.

Dados e instruções são armazenadas em uma única memória, utilizada tanto para leitura quanto para escrita, e podem ser acessados através de endereços.

## Composição do Modelo de Von Neumann
Todos os componentes estão interligados através de barramentos que permitem a transmissão dos bits entre eles, facilitando o processamento e integrando melhor todos os componentes na arquitetura de computadores.

Como caraterísticas de funcionamento do Modelo de Von Neumann, temos:

- Programação sequencial;
- Valor de uma variável alterado durante a execução de um programa;
- Instruções e dados armazenados indistintamente na memória e acessíveis através de endereços.

## Diagrama Funcional da CPU

![Diagrama Funcional da CPU](/media/diagrama_funcional_cpu.png)

Considerada o cérebro do computador, responsável pela execução dos programas armazenados na memória através do ciclo de Busca-Decodificação-Execução.

**Unidade de Controle (UC):** Responsável por buscar instruções na memória principal, determinar seu tipo e encaminhar. **(Responsável por ler e interpretar as instruções lidas da memória de instruções. dar ordens à unidade de dados para executar operações, coordenar as leituras e escritas na memória de dados, coordenar a comunicação com o mundo exterior através dos periféricos.)**

**Unidade Lógica e Aritmética (ULA):** Responsável por executar as instruções, efetuando operações matemáticas e operações lógicas, como já estudado.

**Registradores:** Memórias de alta velocidade, responsáveis, principalmente, pelo armazenamento de resultados necessários na execução de instruções. Na verdade, são as mais rápidas existentes em um computador.

- RDM - Registrador de Dados de Memória - tem conteúdo que foi lido ou que será gravado em uma local da memória.
- REM - Registrador de Endereços de Memória - contém o endereço da Memória Principal onde a CPU deseja efetuar uma leitura ou gravação.
- RI - Registrador de Instruções - tem o conteúdo da instrução em execução no momento.
- CI - Contador de Instrução (PC Counter) - também chamado de Contador de Programa, contém o endereço da próxima instrução que será requisitada na memória. Toda vez que este conteúdo é lido, já é alterado para o endereço da próxima instrução a ser executada.
- ACC - Acumulador - armazena os dados temporários para as operações na ULA.

**Barramentos:** são elementos que efetuam a ligação entre componentes dos computadores.

![Barramentos](/media/barramentos.png)

- Barramento de dados: Canal de comunicação bidirecional que interliga o RDM à memória e outros dispositivos. Sua função é a transferência de conteúdo entre a CPU e a memória principal e os dispositivos de entrada e saída.
- Barramento de endereços: Canal unidirecional que faz a transferência de bits que representam um endereço de memória.
- Barramento de controle: Canal bidirecional que efetua o envio de sinais de controle utilizados para diversos elementos do computador, como se fossem ações a serem feitas por estes elementos.

**Decodificador de instruções (DI):** Este elemento não faz parte de barramentos nem registradores, mas tem uma função de grande importância no processo de execução das instruções. Ele é o responsável por **decodificar o conteúdo dos dados enviados pelas instruções armazenadas na memória, interpretando as operações a serem realizadas.** Feita a decodificação, a unidade de controle poderá enviar para o respectivo responsável a finalização da operação requisitada na instrução, seja ela um cálculo matemático, gravação em um arquivo ou uma impressão.

## Ciclo de Busca – Decodificação – Execução

Esse ciclo ocorre desde o momento em que a CPU busca uma instrução armazenada na memória até o momento em que ela foi executada, estando, assim, a CPU disponível para mais uma execução.

**Busca:**

- Copiar o endereço contido no CI para o registrador de endereços da memória (REM) através do barramento de endereços;
- Enviar um sinal de controle com comando de leitura, via barramento de controle, pela UC para a Memória Principal;
- Ler o conteúdo no endereço da memória, armazenando o mesmo no RDM, através do barramento de dados de memória;
- Copiar o registrador de dados da memória (RDM) para o (RI);
- Atualizar o CI com o próximo endereço a ser executado.

**Decodificação:**

Nessa fase, é determinada qual instrução deve ser executada, enviando o conteúdo do RI para decodificação pelo DI.

**Execução:**

- Encaminhamento da operação para finalização pela UC;
- Fim da execução da operação.

**CLOCK:** um gerador de pulsos regulares de curta duração. Esse sinal é enviado pela CPU, como referência de tempo para todas as atividades dentro de um computador, de forma a garantir o sincronismo de todas as operações, independente do dispositivo, uma vez que alguns periféricos possuem clocks diferentes do clock interno da CPU. O clock é medido em quantidade de vezes por segundo, ou Hertz (hz).

[PDF sobre Clock](/media/clock.pdf)