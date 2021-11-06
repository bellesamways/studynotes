# Aula 4 - Linguagem SQL - Select - Parte 2

Vamos continuar usando o Banco de Dados da Empresa para os exemplos de modelo lógico.

![Banco de Dados da Empresa](/media/Implementação-de-Banco-de-Dados/aula4/Image1.png)

As tabelas possuem os seguintes dados:

Região:

![Tabela Região](/media/Implementação-de-Banco-de-Dados/aula4/Image2.jpeg)

Departamento:

![Tabela Departamento](/media/Implementação-de-Banco-de-Dados/aula4/Image3.jpeg)

Empregado:

![Tabela Empregado](/media/Implementação-de-Banco-de-Dados/aula4/Image4.jpeg)

Cliente:

![Tabela Cliente](/media/Implementação-de-Banco-de-Dados/aula4/Image5.jpeg)

## Gerando restrições às consultas

Até agora, todos os comandos que demos retornaram todas as linhas da tabela. Mas e se você desejar filtrar as tabelas e retornar apenas as linhas que atendam a uma condição?

Nesse caso, você deve acrescentar a cláusula Where ao comando de Select.

A cláusula Where estabelece uma condição que a linha deverá obedecer para que faça parte do conjunto resposta da consulta. No caso, apenas retornam as linhas cujo teste da condição dê como resposta verdadeiro.

Ao selecionar os dados para visualização ou outra necessidade, podemos, além de ordená-los, restringir o espectro de visualização utilizando a cláusula Where.

![Estabelecendo uma condição com a cláusula Where](/media/Implementação-de-Banco-de-Dados/aula4/Image6.png)

Repare que, das seis linhas que a tabela possui “empregado com ID de 1 até 6”, somente retornam as três que possuem ID maior que 3 (4,5 e 6).

Na construção das condições, você pode utilizar os seguintes operadores relacionais:

- Igual =

- Diferente <>

- Menor que <

- Maior que >

- Maior ou igual a >=

- Menor ou igual a <=

Um cuidado que você deve tomar é com o tipo de dado que está utilizando para filtrar. No caso anterior, era um dado numérico (ID) e bastava escrevê-lo. Mas e se fosse um texto?

Veja os dados da tabela CLIENTE.

![Dados da tabela Cliente](/media/Implementação-de-Banco-de-Dados/aula4/Image7.jpeg)

Você deseja o ID do cliente Ponto Quente, cujo valor é 110. O Comando seria então:

- SELECT ID

- FROM CLIENTE

- WHERE NOME = 'PONTO QUENTE'

Veja o retorno.

![Retorno do comando anterior](/media/Implementação-de-Banco-de-Dados/aula4/Image8.jpeg)

Por que não voltou o ID do cliente, já que existe esse nome na tabela? Veja o mesmo comando no Oracle e no SqlServer.

![Comando no Oracle e no Sql Server](/media/Implementação-de-Banco-de-Dados/aula4/Image9.jpeg)

Repare que, no SqlServer, retornou o valor 110 e no Oracle, não. O que está acontecendo?

Alguns SGBD são case sensitive para os dados, ou seja, fazem diferenciação entre letra maiúscula e letra minúscula. Dessa forma, temos que respeitar isso, ou a consulta poderá não retornar as linhas.

No caso do nosso banco de dados, o nome do Cliente está com a primeira letra de cada palavra em maiúsculo, portanto, temos que escrever dessa forma no comando.

- SELECT ID

- FROM CLIENTE

- WHERE NOME = 'Ponto Quente'

![Consulta respeitando a diferenciação entre letra maiúscula e letra minúscula](/media/Implementação-de-Banco-de-Dados/aula4/Image10.jpeg)

Você pode estar pensando:

Significa, então, que eu tenho que saber como está escrito no Banco de Dados? E se eu não souber? E se em uma linha estiver tudo maiúsculo e na outra, tudo minúsculo? E se o banco não tiver um padrão?

Neste caso, você deve padronizar a consulta utilizando uma função que leve o valor existente no banco de dados para maiúsculo ou para minúsculo antes de fazer a comparação.

Veja os exemplos a seguir.

![Padronizando a consulta com a função UPPER](/media/Implementação-de-Banco-de-Dados/aula4/Image11.jpeg)

Repare que:

- Nos comandos PONTO QUENTE, está em maiúsculo e foi utilizada a função UPPER para levar o conteúdo da coluna NOME para maiúsculo antes da comparação;

- UPPER atua apenas na comparação, não altera o valor do existente no banco de dados.

Veja o exemplo abaixo, onde, ao pedirmos para retornar também o nome, ele vem como está no banco de dados.

![A função UPPER não altera o valor do banco de dados](/media/Implementação-de-Banco-de-Dados/aula4/Image12.png)

Dois cuidados que você deve tomar ao trabalhar com string:

- A string deve vir entre apóstrofes ‘PONTO QUENTE‘;

- Se o SGBD for case sensitive, você deve escrever o comando como os dados que estão no banco ou utilizar uma função para padronizar a forma de comparação.

## Trabalhando com datas

Ao trabalhar com datas, devemos colocá-las entre aspas simples, no formato dd/mm/aaaa, onde “dd” é o dia em dois dígitos, “mm” o mês em dois dígitos e “aaaa” é o ano em quatro digitos.

Mostrar sobrenome e senha dos empregados admitidos em 3/3/2009.

- SELECT ULT_NOME, DT_ADMISSAO

- FROM EMPREGADO

- WHERE DT_ADMISSAO = '3/3/2009';

![Trabalhando com datas no PostGreSql, SqlServer e Oracle](/media/Implementação-de-Banco-de-Dados/aula4/Image13.jpeg)

Teste também os seguintes comandos:

```sql
SELECT ULT_NOME, DT_ADMISSAO
FROM EMPREGADO
WHERE DT_ADMISSAO = '3/MAR/2009'
```

Ou

```sql
SELECT ULT_NOME, DT_ADMISSAO
FROM EMPREGADO
WHERE DT_ADMISSAO = '3/MARÇO/2009'
```

Ou

```sql
SELECT ULT_NOME, DT_ADMISSAO
FROM EMPREGADO
WHERE DT_ADMISSAO = '3/MAR/09'
```

Estes formatos também são aceitos, mas, no PostgreSql, deve-se ter um cuidado: o nome/abreviatura dos meses devem ser em inglês: Março - March / Abr – Apr. Já o Oracle e o SqlServer dão suporte aos nomes em português.

## Consultando dados com várias condições

Você pode especificar critérios complexos combinando várias condições de pesquisa.

A utilização dos operadores lógicos AND e OR permite montar expressões lógicas para filtrar as linhas. Como toda expressão lógica, o operador AND somente retorna Verdadeiro (TRUE) se ambas as condições forem verdadeiras, enquanto o operador OR somente retorna FALSO (FALSE) se as duas condições forem falsas.

Veja a tabela EMPREGADO.

![Tabela EMPREGADO](/media/Implementação-de-Banco-de-Dados/aula4/Image14.png)

Vamos supor que você deseja mostrar os empregados que tenham sido contratados após primeiro de janeiro de 2010 e que tenham salário maior que R$10.000.

O comando e o resultado estão na figura a seguir.

![Comando Select utilizando AND](/media/Implementação-de-Banco-de-Dados/aula4/Image15.png)

Repare que a utilização do AND obriga que as duas condições sejam verdadeiras para que a linha retorne. Se tivéssemos utilizado OR, bastaria uma ser verdadeira para que a linha retornasse.

![Comando Select utilizando OR](/media/Implementação-de-Banco-de-Dados/aula4/Image16.png)

## Operadores da linguagem SQL

A linguagem SQL possui um conjunto próprio de operadores para testar condições.

Esses operadores são:

- IN: CONTIDO EM (LISTA)

- BETWEEN: ENTRE VALORES

- LIKE: STRING SEMELHANTE

- IS NULL: Testa valores nulos

### Operador IN

O operador **IN** permite comparar o valor da coluna com uma lista de valores e retorna verdadeiro se, em uma determinada linha, o valor da coluna for igual a um dos valores da lista.

Desejamos listar os empregados que trabalham no departamento 10 ou no departamento 30. Como ficaria o comando?

```sql
SELECT *
FROM EMPREGADO
WHERE ID_DEPTO IN (10,30)
```

Agora, para ver os empregados que NÃO trabalham nestes departamentos, basta acrescentar NOT ao comando:

```sql
SELECT *
FROM EMPREGADO
WHERE ID_DEPTO NOT IN (10,30)
```

### Operador Between

O operador Between And permite verificar se o valor de um campo está contido em uma faixa de valores. Por exemplo, desejamos retornar o id ult_nome e cargo dos empregados com salários entre R$8.000 e R$19.500 inclusive.

O comando seria:

```sql
SELECT *
FROM EMPREGADO
WHERE SALARIO BETWEEN 8000 AND 19500
```

![Resultado do comando Select com o operador Between](/media/Implementação-de-Banco-de-Dados/aula4/Image17.jpeg)

Repare que retornam os empregados com salários de R$8.000 e de R$19.500. Isso mostra que o Between cria um intervalo fechado, ou seja, os limites fazem parte dos valores aceitáveis. Para fazer a condição inversa, basta utilizarmos Not Between.

```sql
SELECT *
FROM EMPREGADO
WHERE SALARIO BETWEEN 8000 AND 19500
```

![Resultado do comando Select com o operador Not Between](/media/Implementação-de-Banco-de-Dados/aula4/Image18.png)

Podemos utilizar Between com Datas. Por exemplo, desejamos os empregados contratados em 2009. O comando seria:

```sql
SELECT *
FROM EMPREGADO
WHERE DT_ADMISSAO BETWEEN '1/1/2009' AND '31/12/2009'
```

![Usando o operador Between com datas](/media/Implementação-de-Banco-de-Dados/aula4/Image19.png)

### Operador Like

O operador Like é utilizado para fazer casamento de padrão, ou seja, procurar um conjunto de caracteres que existe em uma string.

Esta operação de comparação, para poder ser eficiente, necessita do uso de caracteres coringa, que no caso do SQL são dois:

- % - Curinga para representar uma quantidade arbitrária de caracteres (inclusive nenhum);

- \_ - Curinga para indicar a existência obrigatória de um caracter naquela posição.

**Exemplo**: Desejamos saber os dados dos empregados com o ult_nome começado com N. O comando seria:

```sql
SELECT *
FROM EMPREGADO
WHERE UPPER(ULT_NOME) LIKE 'N%'
```

![Resultado da consulta dos empregados com o ult_nome começado com N](/media/Implementação-de-Banco-de-Dados/aula4/Image20.jpeg)

Observações

- Repare o uso da função UPPER. Esta função leva a string para maiúsculo antes de fazer a comparação, sendo muito útil para contornar a limitação do Oracle e do Postgresql, por serem Case Sensitive. Uma outra função possível de ser utilizada é lower, que leva o texto todo para minúsculo.

- No SqlServer, você deve eliminar UPPER, já que ele não é Case Sensitive.

- Note o % depois do N informando que, após essa letra, pode existir uma quantidade arbitrária de caracteres.

**Exemplo**: Desejamos saber os dados dos empregados com o ult_nome terminado com S. O comando seria:

```sql
SELECT *
FROM EMPREGADO
WHERE UPPER(ULT_NOME) LIKE '%S'
```

![Resultado da consulta dos empregados com o ult_nome terminado com S](/media/Implementação-de-Banco-de-Dados/aula4/Image21.png)

E se você quiser retornar os PRIMEIROS NOMES dos empregados que possuem E em qualquer lugar do nome? Como seria o comando?

![Consultando o prim_nome dos empregados com E em qualquer lugar do nome](/media/Implementação-de-Banco-de-Dados/aula4/Image22.png)

Repare no retorno. Temos Carmen com E no meio, mas temos também Ernane que possui E no início e no final, pois o % autoriza a ter uma quantidade arbitrária de caracteres, inclusive nenhum.

Se você desejasse retornar os sobrenomes que possuem E como segunda letra, não adiantaria utilizar %. Para isso temos que informar que OBRIGATORIAMENTE deve existir uma letra antes do E, utilizando nosso outro curinga, o ‘\_’. O comando seria então:

```sql
SELECT ULT_NOME
FROM EMPREGADO
WHERE UPPER(ULT_NOME) LIKE '_E%'
```

![Resultado da consulta dos sobrenomes que possuem E como segunda letra](/media/Implementação-de-Banco-de-Dados/aula4/Image23.png)

Note que temos que ter um \_ antes do E para informar que o E é a segunda letra e que, após ela, podemos ter uma quantidade qualquer de caracteres.

Alguns cuidados:

- O ‘\_’ deve estar colado no ‘E’. Não pode haver espaço entre eles;

- Você deve colocar um ‘\_’ para cada caractere. Por exemplo, para L na terceira, o comando seria:

![Consultado os sobrenomes que possuem L como terceira letra](/media/Implementação-de-Banco-de-Dados/aula4/Image24.png)

Agora, quando você deseja quem não tem R no nome, deve acrescentar o NOT antes do LIKE.

![Consultando os sobrenomes que não possuem R no nome](/media/Implementação-de-Banco-de-Dados/aula4/Image25.png)

### ILIKE

Devido ao fato do PostgreSql ser Case Sensitive, nos comandos utilizamos o UPPER, porém este SGBD possui um operador de LIKE proprietário que permite que façamos o teste sem o uso da função UPPER. É o ILIKE, ou seja, Insensitive-LIKE.

Quando o utilizamos, não precisamos nos preocupar com maiúsculas ou minúsculas. Veja a figura.

![Utilizando o Ilike para consultar os sobrenomes que possuem a letra E](/media/Implementação-de-Banco-de-Dados/aula4/Image26.png)

### Operador IS NULL

O operador Is Null visa determinar se, no campo, existe valor ou não (o campo é nulo).

Um valor nulo é um valor que está indisponível, não foi atribuído, é desconhecido ou inaplicável, tornando inviável usar ‘=’ no teste. Como nulo não é valor, mas sim ausência de valor, ele não pode ser igual ou diferente de qualquer outro valor. Considere a tabela CLIENTE.

![Tabela CLIENTE](/media/Implementação-de-Banco-de-Dados/aula4/Image27.png)

Se você desejasse retornar todos os dados dos CLIENTES que não são atendidos por um vendedor, o comando seria:

```sql
SELECT *
FROM CLIENTE
WHERE VENDEDOR IS NULL
```

![Retornando todos os dados dos clientes que não são atendidos por um vendedor](/media/Implementação-de-Banco-de-Dados/aula4/Image28.png)

Caso contrário, se você quisesse os que são atendidos por vendedor, utilizaria IS NOT NULL.

![Retornar todos os dados dos clientes que são atendidos por um vendedor](/media/Implementação-de-Banco-de-Dados/aula4/Image29.png)
