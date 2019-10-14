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