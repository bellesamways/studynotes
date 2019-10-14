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