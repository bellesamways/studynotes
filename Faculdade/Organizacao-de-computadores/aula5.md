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