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