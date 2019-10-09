# Aula 2 - HARDWARE, SOFTWARE E CONCEITOS

## Hardware e seus componentes

![Hardware](/media/hardware.png)

1. **Unidade Central de Processamento (UCP ou CPU)**: É o dispositivo central de um computador. Processador.
    * **Unidade de Controle**: Responsável pelo gerenciamento de todo o fluxo de informações entre as unidades que fazem parte do hardware, bem como a execução das instruções.
    * **Unidade Lógica e Aritmética**: Responsável pelos cálculos e decisões a serem efetuadas de acordo com as instruções recebidas.
2. **Memória**: Responsável pelo armazenamento das instruções e dados a serem executados ou manipulados pela CPU e seus componentes, bem como armazenamento de informações recebidas pelas Unidades de Entrada e Saída.
3. **Dispositivos de Entrada**: Todos os periféricos que são utilizados e interligados ao computador para envio de informações para o processamento.
4. **Dispositivos de Saída**: Todos os periféricos utilizados para enviar alguma informação para o usuário.

#### Dispositivos Internos x Dispositivos Externos

![Dispositivos](/media/dispositivos.png)

## Software

Todos programas responsáveis por administrar a execução de funções pelo hardware e automatizar as tarefas que o computador irá desempenhar.

**Software Básico**: Utilizado para produzir ou gerenciar a operação do computador e a relação dentre softwares aplicativos com o hardware.

**Software Aplicativo**: Seu foco é o usuário final. Normalmente, os erros ou falhas percebidas pelo usuário são identificados nos softwares que se encaixam nesta categoria.

**Software Livre**: sua cópia ou redistribuição não caracteriza pirataria.

**Software Proprietário**: Não é de livre utilização, cópia ou distribuição. Seu uso somente é possível e permitido mediante a compra de licenças de uso, que podem ser por usuário, por máquina ou por empresa.

**Sistema**: Conjunto de partes coordenadas que colaboram para a realização de um determinado objetivo.

## Algoritmo X Linguagem de Programação X Programa

**Algoritmo** é o conjunto de etapas (instruções) finitas, ordenadamente definidas, com o propósito de obter solução para um determinado problema.

Um algoritmo ou um conjunto de algoritmos podem formar um programa.

Esse conjunto de instruções é transformado em uma linguagem própria (linguagem binária ou linguagem de máquina) que será executada em uma máquina.

**Linguagem de alto nível**: mais próximas do entendimento do programador. Ex: Pascal; Java; C; C++; Cobol; Delphi; Python.

**Linguagem de baixo nível**: mais complexas para o ser humano, em que é mais difícil a compreensão por parte do programador e são necessárias mais ações na programação. Ex: assembly.

Esses conversores são identificados como programas compiladores e ligadores (link editor ou linker).

## Tradução

Consiste na tradução de um programa escrito em linguagem de Alto Nível para a linguagem binária da máquina correspondente.

É feito o processo de **Compilação**, onde o programa escrito na linguagem fonte é traduzido para linguagem máquina e depois ligado e carregado para ser executado.

![Tradução](/media/traducao.png)

## Interpretação

O programa fonte é traduzido e executado, instrução a instrução, de modo interativo.

O interpretador traduz cada instrução para uma representação interna e interpreta-a simulando o funcionamento do processador.

**Vantagens** - O ciclo escrita, execução, modificação e atualização é mais rápido.

**Desvantagens** - A execução é mais lenta.

## Palavra (word)

Unidade natural de informação usada por cada tipo de computador em particular. É uma sequência de bits de tamanho fixo processada em conjunto em uma máquina.

Os computadores modernos possuem tamanho de palavra de 16, 32 e 64 bits, o que indica a unidade básica de transferência de dados entre a CPU e a memória principal.

## Tempo de acesso (latência)

Tempo para recuperação/escrever de uma informação na memória. Depende da tecnologia da memória utilizada.

## Tempo de resposta

Mede o desempenho global do sistema. Baseia-se no tempo gasto entre o início da solicitação e a apresentação da resposta. Engloba o tempo de acesso ou latência.

## Bits e bytes

**Bits**: Esses códigos binários são conhecidos como bits (Binary Digit) e podem assumir somente dois valores: 0 ou 1.

**Bytes**: formada por um conjunto de bits. 1 byte = 8 bits

![](/media/bit_e_bytes.png)

## K (Kilo), M (Mega), G (Giga), T (Tera) e P (Peta)

São potências de 2 (afinal, estamos falando de uma base binária) e não de 10.

**Kilo (= K)**: Representa 1024 unidades (210), e não 1000.

**Mega (= M)**: Representa 1.048.576 unidades (220) ou 1024.K (Afinal, 220 = 210.210).

![](/media/tabela_byte.png)

![](/media/tabela_byte2.png)

## Capacidade de armazenamento x Capacidade de transferência

**Armazenamento**: utilizamos representação em Bytes (B maiúsculo).
* Exemplos:
    * 1 Kbyte ou 1 KB = 1024 Bytes
    * 1 Mbyte ou 1 MB = 1024 Kbytes

**Capacidade de transferência**: usamos bits (b minúsculo), normalmente indicado em bits por segundo (bps).
* Exemplos:
    * 1 Kbit ou 1 Kb = 1024 bits
    * 1 Mbits ou 1 Mb = 1024 Kbits

![](/media/KB_Kb.png)
