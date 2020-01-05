# Aula 1 - EVOLUÇÃO HISTÓRICA DA COMPUTAÇÃO


## Primeira Geração (Válvula)

A primeira geração dos computadores foi marcada pela utilização de válvulas. A válvula é um tubo de vidro, muito similar a uma lâmpada, com eletrodos que possuem a finalidade de controlar o fluxo de elétrons.

## Segunda Geração (Transistor)

A segunda geração de computadores iniciou com a chegada de um substituto para a válvula, o transistor. Além de menores, os transistores consumiam menos energia, sofriam menos aquecimento e eram mais rápidos, o que permitiu que fossem incorporados ao desenvolvimento de computadores, durante o período de 1955 a 1964.

## Terceira Geração (Circuitos Integrados)

A terceira geração veio com a invenção do circuito integrado de silício por Robert Noyce, físico e um dos fundadores da Intel. Com o circuito integrado, dezenas de transistores poderiam estar em um único chip, o que possibilitava a construção de computadores menores e ainda mais rápidos e baratos, pois permitia também a produção em escala maior.

## Quarta Geração (VLSI)

Traduzido como Very Large Scale Integration, ou Integração de Circuitos em Larga Escala, essa geração veio mais como uma evolução dos circuitos integrados, onde a tecnologia permite hoje a inclusão de milhões de transistores em um chip.
Para compreender isso, é necessário entender o processo de litografia. Contudo, neste momento, podemos nos ater à informação de que os fabricantes usam tecnologia de nanômetros distância na construção de microchips, ou seja, a distância entre um transistor e outro dentro do chip.
Para termos uma ideia dessa distância, um nanômetro equivale a um bilionésimo de milímetro.

## Lei de Moore

A lei de Moore surgiu em 1965 através de um conceito estabelecido por Gordon Earl Moore, cofundador da Intel. Essa lei dizia que a capacidade de processamento dos processadores dobraria a cada 18 meses. Moore não tinha essa certeza em 1965, mas imaginava que isso seria possível.

![Lei de Moore](/media/lei_de_moore.png)

Como podemos ver no gráfico, isso realmente tem acontecido. Nos últimos anos, chegando a menos que do isso, de forma que já se discute se esta lei irá se perpetuar mesmo.
Isso tudo se deve ao desenvolvimento acelerado de toda tecnologia de computação.

**São funções básicas de um computador**: processamento de dados, armazenamento de dados, transferência de dados e controle.

**São componentes estruturais de um computador**: Unidade central de processamento, memória principal, dispositivos de entrada e saída e sistemas de interconexão.

Os componentes básicos de um computador são o processador, responsável por executar cálculos lógicos e aritméticos; a memória, que armazena os dados e programas a serem executados; os dispositivos de entrada, que tem a função de fornecer meios de introduzir informações no sistema e os dispositivos de saida, que mostram as informações processadas ao usuário.

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

# Aula 3 - SISTEMAS DE NUMERAÇÃO

## Simbologia para representar quantidades

Os sistemas de numeração têm o objetivo de fornecer uma simbologia com regras para representar certas quantidades, de forma que, com essas regras e normas, a informação quantitativa possa ser identificada por quem a conheça.

Atualmente, essa representação é feita através de números. Em alguns casos, também letras.

### Sistema de Numeração Não Posicional

Já foi muito usado na antiguidade. Não era um sistema de numeração fácil para, por exemplo, fazer operações aritméticas.

Sistema de numeração romano: mais conhecido e estudado nas escolas até hoje, onde letras representam certas quantidades.

A única regra diferenciada na numeração romana é que se um algarismo menor for colocado à esquerda de um maior, o mesmo deverá ser subtraído do maior.

## Sistema de Numeração Posicional

O valor representado pelo algarismo no número depende da posição em que ele aparece na representação. Seu valor absoluto é modificado por um fator (ou peso), que varia conforme a posição do algarismo, sendo **crescente da direita para a esquerda**.

![Sistema de Numeração Posicional](/media/sistema_numeracao_posicional.png)

Dependendo da posição onde o algarismo se localiza, seu resultado final e seu peso serão diferentes.

**Dois conceitos fundamentais:**
1. **A base que representa este número.**
2. **A posição em que o algarismo está.**

## Bases Numéricas

**Sistema Binário:** Usado na computação, sabemos que todos números são formados pelo **0 e 1, ou seja, 2 algarismos.**
**Sistema Decimal:** Usado em nosso cotidiano, sabemos que todos os números são formados pelos números que variam de **0 a 9, ou seja, 10 algarismos.**
**Sistemas Octal e Hexadecimal:** Não é diferente, teremos a representação de todos os números com **8 e 16 algarismos**, respectivamente.

![Bases Numéricas](/media/bases_numericas.png)
![Exemplos de Números em Diferentes Bases Numéricas](/media/bases_numericas_exemplos.png)


## Conversão de Decimal para outra Base

**1º Passo:**
- Realizar divisões sucessivas pelo valor que identifica a base
- Deverão ser feitas tantas divisões quanto necessário para o quociente se tornar zero ou ser menor do que a base, não sendo mais possível efetuar divisões.
**2º Passo:**
- Não sendo possível efetuar mais divisões, deve-se transcrever o último quociente juntamente com os restos das divisões, em ordem inversa ao cálculo efetuado.

![Conversão de Decimal para Binário](/media/conversao_decimal_binario.png)
![Conversão de Decimal para Octal](/media/conversao_decimal_octal.png)
![Conversão de Decimal para Hexadecimal](/media/conversao_decimal_hexadecimal.png)

## Conversão de uma Base para Decimal

Multiplicação de cada algarismo do número pela base, elevada à potência de sua posição do algarismo.

1. multiplicação dos números pelo resultado das suas bases e potências.
2. somando-se os resultados de tudo o que foi obtido.
3. temos o número Decimal convertido.

### 6578 para a base 10

![Conversão de Octal para Decimal](/media/conversao_octal_decimal.png)

### 1AC216 para a base 10

![Conversão de Hexadecimal para Decimal](/media/conversao_hexadecimal_decimal.png)

### 110111102 para a base 10

![Conversão de Binário para Decimal](/media/conversao_binario_decimal.png)

## Bases Octal e Hexadecimal para a base Binária

1. Cada algarismo do número deve ser convertido individualmente para a Base Binária;
2. Ao ser convertido, cada algarismo convertido deve ser formado por um grupo de:
- 3 algarismos binários (se o original for Octal);
- 4 algarismos binários (se o original for Hexadecimal).

Caso na conversão de cada algarismo, o binário não possua o total de três ou quatro binários necessários, deve-se completar com zeros à esquerda a fim de que os grupos sejam formados.

![Conversão de Octal para Binária](/media/conversao_octal_binario.jpg)
![Conversão de Hexadecimal para Binária](/media/conversao_hexadecimal_binario.jpg)

## Conversão da base Binária para Octal e Hexadecimal

1. Com o número binário a ser convertido, dividimos o mesmo, da direita para a esquerda, em grupos de:
- 3 algarismos binários (se o número a ser convertido for Octal);
- 4 algarismos binários (se o número a ser convertido for Hexadecimal);
2. Uma vez efetuada essa divisão, cada grupo deve ser convertido para Decimal, que será o seu número representativo. No caso do Hexadecimal, se o número corresponder entre 10 e 15, o mesmo deverá ser substituído pela letra correspondente, de A até F.

![Conversão de Binária para Octal](/media/conversao_binario_octal.jpg)
![Conversão de Binária para Hexadecimal](/media/conversao_binario_hexadecimal.jpg)

# Aula 4 - ARITMÉTICA E REPRESENTAÇÃO DE SINAIS

Toda operação aritmética ou lógica com mais é feita sem efetuar nenhuma conversão, mas, sim, em binário, para, dessa forma, ser convertido e visualizado pelo ser humano na base pretendida.

## Soma no Sistema Binário

**O transporte para outra coluna, “vai um”.**

![Soma no Sistema Binário](/media/soma_binario.png)

## Subtração no Sistema Binário

![Subtração no Sistema Binário](/media/subtracao_binario.png)

## Soma no Sistema Hexadecimal

![Tabela de Correspondência Decimal-Hexadecimal](/media/tabela_decimal_hexadecimal.png)

O “vai 1” será utilizado sempre que a soma de dois algarismos **exceder o valor de 15 (ou seja, F)**, que é o maior algarismo da base hexadecimal, e irá com o valor 1 para o vizinho, e não como 15 ou F.

![Soma no Sistema Hexadecimal](/media/soma_hexadecimal.png)

## Subtração no Sistema Hexadecimal

Ao emprestar 1 unidade do vizinho, estará emprestando o equivalente a 16.

![Subtração no Sistema Hexadecimal](/media/subtracao_hexadecimal.png)

## Representação de números positivos e negativos em binário

O uso de sinal + (positivo) ou – (negativo) em números binários.

### Sinal e magnitude

Caso tenhamos um número com n algarismos binários (n bits), seu sinal é obtido inserindo-se um bit adicional mais à esquerda, para indicar o valor do sinal, e sua magnitude, ou seja, o seu valor, continua mantendo os bits restantes deste número.

**0 indica POSITIVO e 1 indica NEGATIVO**

![Positivo e negativo em binário](/media/positivo_negativo_binario_magnitude.png)
![Positivo e negativo em binário, exemplo](/media/positivo_negativo_binario_exemplo.png)

### Complemento de 1

Um pouco mais complexo, porém mais confiável do que o método de sinal e magnitude.

1. Com o número binário a ser inserido o sinal, acrescenta-se um bit significativo 0 (zero) mais à esquerda do número, identificando o sinal POSITIVO do mesmo. Procedimento já executado anteriormente em sinal e magnitude;
2. Para identificação do número como negativo, é feita também a inclusão de um bit significativo à esquerda, porém agora invertido, ou seja, ao invés de 0 (zero), 1 (um), assim como a regra de sinal e magnitude. Porém, também são invertidos todos os Bits relativos à magnitude (ou identificação do valor) do número.

![Positivo e negativo em binário, por complemento de 1](/media/positivo_negativo_binario_complemento_1.png)

### Complemento de 2

Método muito utilizado em computação, por não dar ambiguidade no valor e significado do zero em seu significado. Este método é tido como o mais confiável da atualidade.

Todos os procedimentos do complemento de 1 +

3. Realizada a inversão dos Bits, é adicionado 1 ao binário resultante;
4. Feito isso, é encontrado o Complemento de 2, relativo ao negativo de um número em binário.

![Positivo e negativo em binário, por complemento de 2](/media/positivo_negativo_binario_complemento_2.png)

# Aula 5 - CIRCUITOS LÓGICOS

## Portas Lógicas

Componente de hardware que recebe um ou mais sinais de entrada e produz um sinal de saída, de acordo com a lógica estabelecida para a construção do referido circuito definido.

Símbolos: Para que sejam montados os circuitos.
Expressões: Muito similares às expressões matemáticas.

### Porta E ou AND

É aquela que executa a multiplicação de duas ou mais variáveis.

Com a porta E ou AND, temos na tabela verdade uma saída no um (1), ou seja, verdadeiro, SE E SOMENTE SE as suas entradas ou mais entradas forem todas iguais a um, ou seja, positivas.

![Porta](/media/porta_and.png)

| **A** | **B** | **A . B** |
|-------|-------|-----------|
| 0     | 0     | **0**     |
| 0     | 1     | **0**     |
| 1     | 0     | **0**     |
| 1     | 1     | **1**     |

### Porta OU ou OR

É aquela que executa a soma, em que se obtém o valor um (1) quando uma ou mais variáveis de entrada forem iguais a um (1) e assume valor zero (0) se e somente se todas as suas variáveis forem iguais a zero (0).

![Porta](/media/porta_or.png)

| **A** | **B** | **A + B** |
|-------|-------|-----------|
| 0     | 0     | **0**     |
| 0     | 1     | **1**     |
| 1     | 0     | **1**     |
| 1     | 1     | **1**     |

### Porta NÃO / NOT

A função NÃO (também conhecida como Complemento) é aquela que inverterá o estado ou valor da variável, ou seja, se a variável estiver com valor zero (0), vai para um (1), e, se a variável estiver com valor um (1), vai para zero (0).

![Porta](/media/porta_not.png)

| **A** | **S** |
|-------|-------|
| 0     | **1** |
| 1     | **0** |

### Porta NÃO E, NE ou NAND

Essa função é uma composição de duas portas lógicas já estudadas, ou seja, da função E com a função NÃO, de forma que o resultado será uma nova função E invertida.

![Porta](/media/porta_nand.png)

| **A** | **B** | **(A . B)**' |
|-------|-------|--------------|
| 0     | 0     | **1**        |
| 0     | 1     | **1**        |
| 1     | 0     | **1**        |
| 1     | 1     | **0**        |

### Porta NOU / NOR

Essa função é uma composição de duas portas lógicas já estudadas, ou seja, da função OU com a função NÃO, de forma que o resultado será uma nova função OU invertida.

![Porta](/media/porta_nor.png)

| **A** | **B** | **(A + B)**' |
|-------|-------|--------------|
| 0     | 0     | **1**        |
| 0     | 1     | **0**        |
| 1     | 0     | **0**        |
| 1     | 1     | **0**        |

### Porta “OU – EXCLUSIVO” (XOR)

Essa porta lógica, OU – EXCLUSIVO, apresenta como resultado lógico 1, se as variáveis de entrada forem diferentes entre si, ou seja, se houver EXCLUSIVIDADE de valor na variável.

![Porta](/media/porta_xor.png)

| **A** | **B** | **A (+) B** |
|-------|-------|-------------|
| 0     | 0     | **0**       |
| 0     | 1     | **1**       |
| 1     | 0     | **1**       |
| 1     | 1     | **0**       |

### Porta “NOU – EXCLUSIVO” (XNOR) / COINCIDÊNCIA

A função lógica XNOR, conhecida como COINCIDÊNCIA, ao contrário da OU-EXCLUSIVO, tem como resultado um (1), sempre que em suas variáveis de entrada houver uma igualdade.

![Porta](/media/porta_xnor.png)

| **A** | **B** | **A (.) B** |
|-------|-------|-------------|
| 0     | 0     | **1**       |
| 0     | 1     | **0**       |
| 1     | 0     | **0**       |
| 1     | 1     | **1**       |

    A chave de tudo é um circuito eletrônico chamado **chave automática**.
ligada -> 1
desligada -> 0

## Expressões Lógicas

A construção de expressões com base no circuito já informado.

1. Procure iniciar a formação das expressões da direita para a esquerda
2. Para facilitar a identificação das expressões, pode ser útil desmembrar os membros da porta lógica final. Conforme exemplo abaixo, desmembrando, teríamos a expressão lógica abaixo. De forma que, identificando X’ e X’’, simplesmente podemos substituir na expressão.
3. Pode-se verificar que ambos os desmembramentos, X’ e X’’, são formados pela mesma porta lógica, função OU, representada pelo símbolo +. Sendo assim, pode-se escrever as expressões que representam os mesmos.
4. Uma vez identificado, temos:

![Expressões Lógicas](/media/portas_expressoes_logicas.png)

## Tabela Verdade

Permite que possíveis saídas de um circuito sejam identificadas. Assim, é possível saber a probabilidade, por exemplo, de uma saída positiva em um circuito.

Considerando que o Sistema é Binário (Base 2), eleva-se a base 2 à quantidade de variáveis existentes.

Exemplo:
- 2 variáveis, 4 variações na Tabela Verdade (22);
- 3 variáveis, 8 variações na Tabela Verdade (23).

![Tabela Verdade](/media/tabela_verdade.png)

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

Aula 7 - PROCESSADOR E CONJUNTO DE INSTRUÇÕES

## Instrução de Máquinas

As operações da máquina podem ser:

- **Matemáticas:** Ex: Operações aritméticas, lógicas, de complemento.
- **Movimentação de dados:** Ex: Movimentação da memória para um registrador.
- **Entrada/saída**: Ex: Leitura e gravação de dados em dispositivos externos.
- **Controle**: Ex: Desvio condicional da sequência de execução (Se X>18 então ...).

## Formato das Instruções

| **CÓDIGO DE OPERAÇÃO** | OPERANDO 1 | OPERANDO 2 | OPERANDO 3 |

**Código de Operação:** Define a operação que será realizada pelo processador. É o campo da instrução onde o valor binário identifica a operação a ser realizada. Este código é a entrada no Decodificador de Instruções para a unidade de controle. Cada instrução possui um código único, que será seu identificador dentro da execução de instruções em um processador.

**Operando:** Define o valor binário da localização do dado ou mesmo o próprio conteúdo do dado a ser processado pela instrução definida em seu código de operação. Normalmente o operando define um endereço de memória que possui o dado armazenado ou onde será armazenado o resultado de uma operação. Operações aritméticas possuem em geral 2 ou 3 operandos.

**Aspectos dos Conjuntos de Instruções**

![Aspectos dos Conjuntos de Instruções](/media/conjuntos_instrucoes_1.png)

| ADD      | SALARIO      | TAXA         |
|----------|--------------|--------------|
| 11010011 | 110011001100 | 101010101010 |
| 8 BITS   | 12 BITS      | 12 BITS      |

![Aspectos dos Conjuntos de Instruções](/media/conjuntos_instrucoes_2.png)

A **Palavra desse processador seria de 32 Bits**, que é o tamanho da informação que trafega entre a CPU e a memória principal. Dessa forma, temos um exemplo de uma instrução definida por 1 operação e 2 operandos.

## Quantidade de Operados

Instruções de máquinas são constituídas por um conjunto de beta, que contém um subconjunto chamado código de operação, responsável por identificar a operação a ser realizada pelo hardware. Esse código é decodificado na UC na fase de instrução, gerando os pulsos de controle para acionar as portas lógicas necessárias à execução da operação. Possui ainda um ou mais grupos de bits denominados campo(s) do(s) operando(s) que tem por função identificar e localizar o dado a ser processado.

**Instruções com 3 operandos:** Dentro de uma instrução de 3 operandos, os campos 1 e 2 representam os endereços de cada dado que será utilizado na operação. O campo relativo ao Operando 3 contém o endereço onde será armazenado o resultado da operação em execução.

![Instruções com 3 operandos](/media/instrucoes_3_operandos.png)

O pensamento deve ser assim:
ADD    A, B, X        “Pegue A, some com B, e armazene em X”

**Instruções com 2 operandos:** Nas instruções com 2 operandos, novas operações aparecem, em virtude de algumas limitações. Quando há somente 2 operandos, o campo 1 sempre recebe o resultado da operação.

![Instruções com 2 operandos](/media/instrucoes_2_operandos.png)

Operação Move, como o próprio nome diz, MOVE o conteúdo de um endereço de memória, para outro endereço.

**Instruções com 1 operando:** Nas instruções com 1 operando, o uso do Acumulador (registrador utilizado para armazenamento temporário na CPU) é constante, pois é utilizado como um operando não expressamente declarado, mas utilizado em todas as operações.

![Instruções com 1 operando](/media/instrucoes_1_operando.png)

Nesse tipo de execução, tem-se 2 novas operações, sendo elas LDA (LOAD) e STA (STORAGE), onde:
- LDA se refere a carregar um conteúdo armazenado na memória;
- STA a armazenar um conteúdo na memória.

No exemplo ADD Op, entende-se: “Pegue o conteúdo do Acumulador, some ao Operando, e grave novamente no Acumulador”.

## Modos de Endereçamento de Instruções

- **Imediato:** utiliza um valor como operando e não um endereço na memória, ou seja, não é utilizado um endereço da memória, o operando é parte da instrução. Permite definir constante e valores de variáveis iniciais;
- **Direto:** indica o endereço de memória onde está o operando;
- **Indireto:** Indica um ponteiro de endereço para um operando, onde o conteúdo deste ponteiro não é um dado e sim outro endereço. Há um duplo endereçamento neste caso;
- Por registrador: O endereço se refere a um endereço de registrador e não da memória principal;
- **Base + Deslocamento:** Endereço obtido pela soma do operando com o conteúdo de um registrador-base.

## Paralelismo

Possibilidade de executar instruções em paralelo.

**Formas gerais de paralelismo:**

- Paralelismo no nível de instrução    
- Paralelismo no nível de processador

### Paralelismo no nível de instrução

O mais conhecido é o PIPELINE.

Pipeline foi uma técnica revolucionária que consistia em dividir a execução de uma instrução através do ciclo de instruções em diversas etapas, chamadas estágios, onde cada uma era manipulada por um agente distinto dentro do ciclo de instrução. Dessa forma, era possível identificar agentes “ociosos” dentro do processo, podendo agilizar e iniciar outra instrução, mesmo que a anterior não tivesse sido finalizada.

Trata-se de uma metodologia básica para melhorar a velocidade, reduzindo o número de ciclos de clock necessários para executar uma instrução, permitindo sobrepor a execução das instruções através dos pipelines, fazendo, assim, o uso uso mais adequado do hardware.

![Pipeline](/media/paralelismo_pipeline.png)

Não será sempre o caso, mas, em boa parte das vezes, o pipeline evitará a ociosidade e aumentará a eficiência do processador.

Logo, o paralelismo a nível de instrução, através do pipeline, aumenta o desempenho de uma CPU devido ao aumento da vazão das instruções, para que haja maior número de instruções executadas por unidade de tempo.

# Aula 8 - MEMÓRIA (PARTE 1)

## O que é memória?

Memória é o componente dentro da arquitetura e organização do computador com a função de armazenar os programas e os dados que serão manipulados pelo sistema operacional dentro dos ciclos de instrução.

A memória não pode ser considerada um componente único, mas sim um subsistema.

## Velocidade de processamento

Memória principal: Essa memória principal é a tão conhecida memória RAM, que leva aproximadamente 60 nanossegundos para processar um dado e transferir para a CPU.

Dentro da CPU, um dado é processado em aproximadamente 5 nanossegundos (isto significa 5 bilionésimos de segundo), ao contrário do processamento da memória principal

## Memória primária x secundária

Uma memória é volátil quando ela perde o conteúdo, quando não há alimentação de energia. Resumindo, **se o equipamento é desligado, seu conteúdo é perdido.**

**Memória primária:** São os componentes que fornecem dados e instruções para uso imediato, sendo voláteis. Basicamente, é formada pelos seguintes componentes: Registradores, Memória cache e Memória principal.

**Memória secundária:** São os componentes que provêm capacidade de armazenamento permanente (não voláteis). Exemplos de dispositivos de armazenamento secundário são: Discos Rígidos, Discos Óticos (CDs, DVDs, etc.) e Fitas.

![Memória primária x secundária]("/media/memoria_primaria_secundaria.png")

## Registradores

São dispositivos de armazenamento temporário, localizados na CPU, utilizados constantemente dentro do processo de execução das instruções. Por serem usados pela CPU, entende-se que são memórias muito rápidas. Na verdade, são consideradas as memórias mais rápidas existentes no sistema de computação. Porém, como seu objetivo é o armazenamento do conteúdo de memória a ser processado pela CPU, sua capacidade de armazenamento se limita à palavra daquele processador, normalmente variando de 8 a 64 Bits.

Mesmo sendo de baixa capacidade de armazenamento, os registradores são sempre construídos internamente no chip do processador.

## Memória cache

É uma memória criada justamente para diminuir os “estados de espera” entre CPU e memória principal, sendo muito mais rápida do que a memória RAM e com mais capacidade do que os registradores.

Ela tem a função de armazenar temporariamente conteúdos muito requisitados e fornecer as informações para a CPU de forma mais ágil, evitando que a memória principal tenha que ser consultada a todo momento, reduzindo a ociosidade da CPU.

O custo da memória cache é maior do que o da principal e menor do que o custo de registradores, o que justifica parte da solução encontrada.

**O custo de fabricação da memória cache é muito maior do que o da principal, não justificando a extinção da principal. Ou seja, não seria viável economicamente construir um computador somente com tecnologia de memória cache.**

## Princípio da localidade

Todo conteúdo consultado com mais frequência na memória principal é mantido de forma espelhada na memória cache, ou seja, este conteúdo não é apagado na memória principal, somente espelhado. Esse conteúdo consultado com frequência é verificado pelo princípio da localidade.

Princípio da localidade temporal: Baseia-se no fato de que um dado acessado recentemente tem mais chances de ser usado novamente do que um dado usado há mais tempo. Isso é uma realidade pois, quando um programa está em execução, uma variável pode ser consultada diversas vezes durante seu processamento, por exemplo, se houver uma rotina de loop ou sub-rotinas. **Sendo assim, o princípio da localidade temporal tende a manter os dados e instruções recentemente acessados.**

**Princípio da localidade espacial:** Baseia-se no fato de que há uma grande probabilidade de acesso para dados e instruções em endereços próximos àqueles acessados recentemente pela CPU (como no exemplo citado anteriormente). Durante a execução de um programa, normalmente as variáveis são criadas e armazenadas próximas umas às outras, dentro da memória principal.

**O conteúdo estará disponível na memória cache de imediato?**
Nem sempre.
- Se a CPU busca um determinado dado e o encontra na cache, dá-se o que chamamos de cache hit, ou seja, conteúdo é localizado na cache;
- Se o caso for negativo, ou seja, se o dado não estiver presente na cache, sendo necessário requisitar o conteúdo para a memória principal, dá-se o que chamamos de cache miss.

Independente de cache miss ou cache hit, dentro do processo de fabricação da memória cache e suas metodologias de gravação de dados, o índice de cache hit é geralmente acima de 90%.

## Níveis de cache

**Cache L1 (nível 1):** Pequena memória inserida internamente no processador, ou seja, encapsulada dentro do núcleo de processamento. Também conhecida como cache on-die (no núcleo), exatamente por estar dentro do processador.
Alguns fabricantes identificam as memórias cache L1 como formada por dois elementos:
- Memória de instrução – acionada quando o processador está buscando uma instrução;
- Memória para dados – acionada se o processador estiver buscando um dado.

**Cache L2 (nível 2):** Localizada fora do núcleo, mas muito próxima do mesmo, sendo construída normalmente dentro do processador.

**Cache L3 (nível 3):** Em algumas arquiteturas, encontramos ainda o nível 3 na placa-mãe. Em outras, dentro do processador. Porém, usada como cache compartilhada entre os núcleos de um processador. Foi criada originalmente pelo fabricante AMD.

Caches são geralmente inclusivas. Isso significa que o conteúdo total de uma cache L1 está na cache L2, que também está na cache L3.

## Mapeamento de cache

**Caches totalmente associativas:** Neste método todas as linhas de cache da memória principal podem ser gravadas em qualquer localização na memória cache. É uma forma ineficiente porque a recuperação dos dados pode levar à varredura completa da cache para localizar o conteúdo.

**Caches de mapeamento direto:** O método de mapeamento direto limita a gravação das linhas de cache em locais específicos na cache. Porém, este índice pré-definido dos locais permite que a pesquisa do conteúdo na cache seja mais ágil.

![Caches de mapeamento direto]("/media/cache_mapeamento_direto.png")

**Caches associativas de conjunto:** Este tipo de mapeamento é um esquema híbrido entre o mapeamento totalmente associativo e o mapeamento direto. Ele permite que os problemas do mapeamento totalmente associativo (em que a cache inteira precisa ser varrida à procura de um endereço) e do mapeamento direto (em que ocorrem colisões) sejam minimizados. Nele, um mesmo endereço na memória principal pode ser armazenado em mais de um local (por vez) da cache, através da criação de vias de cache, ou seja, cada linha pode possuir n vias de cache, onde normalmente são de 2 a 4 vias.

![Caches associativas de conjunto]("/media/cache_associativa_conjunto.png")

## Métodos de substituição de dados

No que se refere à memória cache, é importante lembrar que existe um momento em que sua capacidade está lotada e os dados precisam ser substituídos, como, por exemplo, os das vias de cache.

![Métodos de substituição de dados]("/media/metodos_substituicao_dados.png")

## Políticas de escrita em cache na memória principal

Logicamente, é necessário que, em algum momento, os dados atualizados na memória cache também sejam atualizados na memória principal. Afinal, uma deve ser o espelho da outra.

**Write Through:** Consiste em atualizar o valor em cache e na MP simultaneamente.
**Write Back:** Consiste em atualizar a cache, porém ao enviar atualizações em blocos para a memória principal.


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
