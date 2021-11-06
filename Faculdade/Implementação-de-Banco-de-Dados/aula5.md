# Aula 5 - LINGUAGEM SQL – Funções de Grupo

Vamos continuar utilizando o modelo abaixo como exemplo:

![Tabelas do banco de dados "Empresa"](/media/Implementação-de-Banco-de-Dados/aula5/Image1.png)

As tabelas possuem os seguintes dados:

Região:

![Tabela Região](/media/Implementação-de-Banco-de-Dados/aula5/Image2.png)

Departamento:

![Tabela Departamento](/media/Implementação-de-Banco-de-Dados/aula5/Image3.png)

Empregado:

![Tabela Empregado](/media/Implementação-de-Banco-de-Dados/aula5/Image4.png)

Cliente:

![Tabela Cliente](/media/Implementação-de-Banco-de-Dados/aula5/Image5.png)

## Eliminando valores duplicados (DISTINCT)

Observe que na tabela Empregados, RODRIGUES e UGARTE possuem o mesmo cargo. E se desejássemos ver os diferentes cargos? Se comandássemos SELECT CARGO FROM EMPREGADO, teríamos o resultado desejado?

![Resultado do comando SELECT CARGO FROM EMPREGADO](/media/Implementação-de-Banco-de-Dados/aula5/Image6.png)

Em termos de dados, até poderíamos dizer que sim, que todos os cargos aparecem no resultado. Mas, em termos de facilidade para o usuário, isso é suficiente?

Imagine que a tabela tivesse milhares de linhas com dezenas de cargos diferentes.

O usuário ficaria confuso, pois teria muita dificuldade de isolar todos os cargos existentes ali. Para resolver esse tipo de caso, podemos, no comando, eliminar os valores duplicados, retornando apenas uma vez cada cargo.

Para tal, devemos acrescentar a cláusula distinct ao comando de Select. Dessa forma o comando seria:

```sql
SELECT DISTINCT CARGO
FROM EMPREGADO
```

![Retornando cargos únicos com Select Distinct](/media/Implementação-de-Banco-de-Dados/aula5/Image7.png)

Agora conseguimos o resultado que queríamos. Observe agora o seguinte comando:

```sql
SELECT DISTINCT CARGO, ULT_NOME
FROM EMPREGADO
```

![Utilizando o Distinct para filtrar linhas diferentes](/media/Implementação-de-Banco-de-Dados/aula5/Image8.png)

Note que voltaram os dois vendedores. Por que isso ocorreu se o DISTINCT continua antes do cargo? **O Distinct, na realidade, filtra as linhas diferentes, não os valores da coluna.** Como os dois vendedores possuem nomes diferentes, as linhas são distintas, portanto as duas retornam.

## Agregando dados

Até agora todos os comandos que demos retornavam uma linha para cada linha da tabela ou uma linha para cada linha da tabela que atendesse a condição da cláusula Where. Veja os exemplos abaixo.

![Retornando todas as linhas da tabela e retornando as linhas que atendem a condição da cláusula Where](/media/Implementação-de-Banco-de-Dados/aula5/Image9.jpeg)

No primeiro comando, retornaram três linhas, o total de linhas da tabela. No segundo comando, duas linhas, o total de linhas que atendem a condição da cláusula Where.

Observe agora os próximos dois comandos.

![Retornando o valor total de linhas da tabela e retornando aquantidade de linhas que atendem a condição da cláusula Where](/media/Implementação-de-Banco-de-Dados/aula5/Image10.jpeg)

Note que, com os dois comandos, retornou apenas uma linha. No primeiro, com valor três (total de linhas da tabela) e no segundo, com valor dois (quantidade de linhas que atendem a cláusula Where).

O que mudou? Foi acrescentado COUNT na claúsula Select que, como você já deve ter percebido, **contou as linhas que a consulta retornaria e exibiu esse valor**. O que fizemos foi agregar dados, ou seja, **derivamos um dado sumarizado a partir dos dados da tabela**.

## Funções de grupo

Uma função de grupo atua em uma instância da tabela, ou seja, no conjunto de suas linhas.

As funções agregam os dados a partir de todas a linhas da tabela ou de grupos em que as linhas possam ser enquadradas.

A princípio, a tabela forma um único grupo, e a consulta com função de grupo retornará uma única linha.

Ao utilizarmos a cláusula GROUP BY, podemos dividir a tabela em grupo, sendo que a consulta, então, retornará uma linha para cada grupo. Na linguagem SQL, possuímos as seguintes funções de grupo:

### AVG (coluna)

- Retorna a MÉDIA aritmética dos valores da coluna solicitada;

- Exemplo: AVG (valor_segurado);

- Se na coluna existirem nulos, ela os desconsidera no cálculo,

- Os valores na coluna devem ser numéricos.

### MAX (coluna)

- Retorna o MAIOR valor existente na coluna solicitada;

- Exemplo: MAX (CPF);

- Se na coluna existirem nulos, ela os desconsidera.

- Os valores na coluna podem ser numéricos, alfanuméricos ou datas

### MIN (coluna)

- Retorna o MENOR valor existente na coluna solicitada;

- Exemplo: MIN (CPF);

- Se na coluna existirem nulos, ela os desconsidera;

- Os valores na coluna podem ser numéricos, alfanuméricos ou datas

### SUM (coluna)

- Retorna a soma aritmética dos valores da coluna solicitada;

- Exemplo: SUM (valor_segurado);

- Se na coluna existirem nulos, ela os desconsidera no cálculo;

- Os valores na coluna devem ser numéricos.

### COUNT (coluna)

- Retorna o número de valores não nulos da coluna solicitada;

- Exemplo: COUNT (CPF);

- Os valores na coluna podem ser numéricos, alfanuméricos ou datas

### COUNT (\*)

- Retorna o número de linhas que a consulta retornaria;

- Exemplo: COUNT (\*);

- Considera os valores nulos.

Vejamos alguns exemplos.

Acesse o PostgreSQL e digite o seguinte comando: `SELECT * FROM EMPREGADO`.

![Selecionando os dados de todos os empregados](/media/Implementação-de-Banco-de-Dados/aula5/Image11.png)

Esse comando seleciona dados de todos os empregados.

Vamos supor que você deseja recuperar apenas o valor médio dos salários e a soma dos salários. Para essa consulta, você comandaria:

```sql
SELECT AVG(SALARIO), SUM(SALARIO)
FROM EMPREGADO
```

![Consultando o valor médio dos salários e a soma dos salários](/media/Implementação-de-Banco-de-Dados/aula5/Image12.png)

Apesar de já ter sido dito, lembre-se sempre de que as funções AVG e SUM são numéricas, ou seja, exigem que os seus argumentos (colunas que passamos a função; no exemplo, a coluna SALÁRIO) sejam números.

Agora você deseja listar o maior e o menor valor de salário de um empregado, os sobrenomes que aparecem como último e como primeiro na ordem alfabética crescente e as datas do empregado contratado há mais tempo e há menos tempo. Para isso basta comandar:

![Resultado da consulta anterior](/media/Implementação-de-Banco-de-Dados/aula5/Image13.png)

Observe que:

- Podem ser utilizadas várias funções de grupo em paralelo, na mesma coluna ou em colunas distintas;

- Quando o argumento da função é alfanumérico (como a coluna ult_nome), o valor que aparece por último na ordem alfabética crescente é o maior e o que aperece primeiro é o menor;

- Quando o argumento da função é numérico (como a coluna salário), menor e maior se referem à posição dos números no sistema de numeração, respeitado o fato de serem positivos ou negativos;

- Quando o argumento da função é data (como a coluna dt_admissao), menor e maior se referem à posição da data na linha do tempo, ou seja, a menor aparece primeiro na linha do tempo e a maior aparece por último.

Mais um exemplo:

Acesse o PostgreSql e digite o seguinte comando: `SELECT * FROM EMPREGADO`.

![Resultado do comando SELECT * FROM EMPREGADO](/media/Implementação-de-Banco-de-Dados/aula5/Image14.png)

Agora você deseja saber a quantidade de empregados e a quantidade de empregados que possuem gerentes. Como seria o comando?

O comando seria:

```sql
SELECT  COUNT(*), COUNT(ID), COUNT(ID_GERENTE)
FROM EMPREGADO
```

E obteríamos um retorno similar ao da figura abaixo.

![Retornando a quantidade de empregados e a quantidade de empregados que possuem gerentes](/media/Implementação-de-Banco-de-Dados/aula5/Image15.png)

Observe que:

- Count(\*) conta a quantidade de linhas retornadas, independentemente de seu conteúdo;

- Count(coluna) conta a quantidade de linhas não nulas naquela coluna;

- Se compararmos o resultado de count(id) com count(id_gerente), podemos notar que a primeira expressão retornou o valor 6, total de linhas da tabela já que ID é chave primária, não podendo possuir valor nulo. Já a segunda retornou 5, pois o empregado de ID 1 não possui gerente, de forma que somente cinco linhas possuem valor não nulo nesta coluna.

Se acrescentar a função de grupo DISTINCT, essa passará a ignorar os valores duplicados, computando cada um deles apenas uma vez.

Observe a figura abaixo que nos mostra o conteúdo das colunas CARGO e ID_DEPTO na tabela EMPREGADO.

![Conteúdo das colunas CARGO e ID_DEPTO na tabela EMPREGADO](/media/Implementação-de-Banco-de-Dados/aula5/Image16.png)

Podemos observar que, na coluna cargo, dentre seis linhas há duas com o valor vendedor, e na coluna id_depto, dentre seis linhas há quatro com o valor 20.

Se desejássemos listar a quantidade de cargo e quantidade de cargos diferentes a quantidade de departamentos e a quantidade de departamentos diferentes, qual seria o comando?

O comando seria:

```sql
SELECT COUNT(CARGO), COUNT(DISTINCT CARGO),
COUNT(ID_DEPTO), COUNT( DISTINCT ID_DEPTO)
FROM EMPREGADO
```

Obteríamos um retorno similar ao da figura abaixo.

![Resultado do comando anterior](/media/Implementação-de-Banco-de-Dados/aula5/Image17.png)

Observe o seguinte:

- Quando executamos o comando sem o distinct, (count(cargo) ou count(id_depto), são contadas todas as linhas não nulas;

- Quando executamos o comando com o distinct, (count(distinct cargo) ou count(distinct id_depto), cada valor discreto existente na coluna é computado apenas uma vez.

## Criando grupos nas tabelas

Podemos agrupar os dados de nossa tabela utilizando a cláusula GROUP BY. Sintaxe:

```sql
SELECT nome da coluna [ , nome da coluna]
        FROM  nome da tabela
        WHERE condição
        GROUP BY expressão
```

“Expressão” determina a(s) coluna(s) cujo(s) valor(es) vai servir de parâmetro para o agrupamento das linhas. Sobre os grupos criados serão aplicadas as funções de grupo, para gerar a sumarização desejada.

Por exemplo: se você desejasse saber a quantidade de empregados, a média salarial e o valor da folha salarial de cada departamento da empresa, o comando seria:

```sql
SELECT  COUNT(*), AVG(SALARIO), SUM(SALARIO), ID_DEPTO
FROM EMPREGADO
GROUP BY ID_DEPTO
```

Obteríamos um retorno similar ao da figura abaixo.

![Consultando  quantidade de empregados, a média salarial e o valor da folha salarial de cada departamento](/media/Implementação-de-Banco-de-Dados/aula5/Image18.png)

Observe o seguinte:

- Na cláusula Group By, você deve colocar a coluna cujos valores serão utilizados para criar os grupos, sendo que pertencem ao mesmo grupo todas as linhas que possuem valores iguais na coluna;

- Você também deve colocar na cláusula Select a coluna ou colunas utilizadas para criar os grupos, permitindo dessa forma que se saiba a qual grupo pertence o valor gerado pela função de grupo.

No SELECT, só é permitido colocar COLUNAS que foram utilizadas no GROUP BY ou nas FUNÇÕES DE GRUPO.

Observe o exemplo da figura abaixo, similar ao comando anterior, com a diferença de que não temos a cláusula GROUP BY, gerando um erro com a presença da coluna id_depto no select.

![Erro com a presença da coluna id_depto no select](/media/Implementação-de-Banco-de-Dados/aula5/Image19.png)

A cláusula GROUP BY permite que você crie grupos definidos por mais de uma coluna, ou seja, a agregação não será por uma coluna, mas por um conjunto de colunas.

Para recuperar a quantidade de empregados que temos em cada cargo em cada departamento, poderíamos dar o comando mostrado na figura a seguir.

![Consultando a quantidade de empregados em cada cargo e em cada departamento](/media/Implementação-de-Banco-de-Dados/aula5/Image20.png)

## Filtrando dados agrupados

Ao utilizar a cláusula GROUP BY, pode-se filtrar a seleção de dados antes deles serem agrupados OU/E após o agrupamento. O momento de realizar essa restrição depende do desejo de eliminar linhas da tabela antes de aplicar as funções de grupo, criando uma condição na cláusula WHERE, ou se o seu intuito é eliminar GRUPOS que não atendam a uma determinada condição, utilizando nesse caso a cláusula HAVING.

Vejamos alguns exemplos:

Você deseja filtrar a consulta por dados que existem na tabela. Por exemplo, quer contar a quantidade de empregados, o salário médio e a soma dos salários dos empregados do departamento 20. Nesse caso devemos filtrar os dados antes de agrupá-los utilizando WHERE, já que a filtragem será realizada por um dado que existe na tabela, o ID_DEPTO.

```sql
SELECT  COUNT(*), AVG(SALARIO), SUM(SALARIO)
FROM EMPREGADO
WHERE ID_DEPTO = 20
```

E obteríamos um retorno similar ao da figura.

![Filtrando os dados dos empregados do departamento 20](/media/Implementação-de-Banco-de-Dados/aula5/Image21.png)

Em resumo, temos que:

- Quando se deseja filtrar antes do agrupamento, utiliza-se a cláusula WHERE para eliminar as linhas da tabela que não nos interessa agrupar, de forma similar ao que fazemos no comando select, quando não desejamos que as linhas retornem no resultado da consulta;

- A condição estabelecida no WHERE, as linhas que não a atendem, no caso do exemplo as linhas que não são do ID_DEPTO 20, não retornam. Dessa forma somente as linhas do departamento 20 estarão no conjunto a ser feito com a agregação de dados;

- Após a filtragem das linhas da tabela é que os dados são agrupados e as funções aplicadas, retornando, portanto, apenas os valores referentes ao departamento desejado.

A cláusula HAVING tem função semelhante à cláusula WHERE, mas é aplicada aos resultados das funções de grupo geradas para cada grupo, não nas linhas das tabelas. Em outras palavras, após gerarmos os resultados dos grupos, podemos filtrá-los retornando apenas aqueles que atendam às condições da Cláusula HAVING.

Considere agora o seguinte comando:

```sql
SELECT ID_DEPTO, COUNT(*), AVG(SALARIO), SUM(SALARIO)
FROM EMPREGADO
GROUP BY ID_DEPTO
```

![Retorno do comando anterior](/media/Implementação-de-Banco-de-Dados/aula5/Image22.png)

Note que os departamentos 20 e 30 possuem mais de um empregado. Se desejássemos listar os departamentos que possuem mais de um empregado, como seria o comando?

A primeira ideia que poderíamos ter seria utilizar a cláusula WHERE como no seguinte comando:

```sql
SELECT  COUNT(*), AVG(SALARIO), SUM(SALARIO), ID_DEPTO
FROM EMPREGADO
WHERE COUNT(*) > 1
GROUP BY ID_DEPTO
```

Esse comando gera um erro, conforme podemos ver na figura abaixo:

![Erro ao utilizar a função Count na clásula Where](/media/Implementação-de-Banco-de-Dados/aula5/Image23.png)

Não podemos utilizar funções de grupo desta forma na cláusula WHERE, somente em subconsulta, como veremos mais à frente no curso. Além disso, devemos lembrar que, na tabela original, não existe a contagem de linhas e a cláusula WHERE trabalha nos dados existentes na tabela.

Qual seria o comando então? Veja na figura abaixo.

![Utilizando corretamente a função Count com a clásula Having](/media/Implementação-de-Banco-de-Dados/aula5/Image24.png)

Note o uso da cláusula HAVING para criar condições às quais os grupos devem obedecer para poderem retornar. Podemos dizer que a cláusula HAVING é similar à cláusula WHERE somente se aplicada aos dados gerados pelas funções de grupo.

Observe que você pode apenas usar WHERE para restringir linhas individuais. Para restringir grupos, usa-se a cláusula HAVING.

Um comando com cláusulas WHERE e HAVING funciona obedecendo aos seguintes passos:

- Primeiro são selecionadas as linhas da tabela que satisfazem a condição da cláusula WHERE (se não houver, todas a linhas são selecionadas);

- As linhas são agrupadas;

- A função de grupo é aplicada ao Grupo;

- Os grupos que satisfazem a condição do HAVING são exibidos (se não houver, todos os grupos serão exibidos).

## Ordenando consultas

Até agora, em todos os comandos que você viu, as linhas retornaram na ordem em que foram produzidas. Porém, muitas vezes, pode ser necessário que elas sejam ordenadas. Para permitir isso, o SQL possui a cláusula ORDER BY.

O resultado de uma consulta pode ser ordenado pelo valor de uma ou mais colunas, de forma crescente ou decrescente.

A sintaxe básica do ORDER By é:

```sql
SELECT { * | nome da coluna [, nome da coluna ...]}
        FROM nome da tabela
        WHERE condição {AND | OR} condição
        ORDER BY  nome da coluna  [ ASC  |  DESC ]  [, nome da coluna   [ ASC | DESC] . ]
```

Onde:

- ASC ordena as linhas de forma ascendente; é a ordenação default.

- DESC ordena as linhas de forma descendente.

A cláusula ORDER BY será sempre a última de um comando SQL.

Vejamos um exemplo: desejamos listar o ID, o sobrenome, a data de admissão, o cargo e o salário de todos os empregados em ordem crescente de salário.

![Ondenando a consulta com Order By](/media/Implementação-de-Banco-de-Dados/aula5/Image25.png)

Note que:

- O resultado da consulta voltou ordenado na forma solicitada. No exemplo, a ordenação definida na cláusula ORDER BY fez com que as linhas retornadas da tabela EMPREGADO sejam ordenadas por SALÁRIO e só então exibidas;

- O padrão default de ordenação da cláusula ORDER BY é crescente. Dessa forma, o uso de ASC para indicar a ordem crescente (ascendente) é opcional. Se for omitida, a ordenação ascendente será realizada, como foi o caso do exemplo.

### Ordenação decrescente

Para a ordenação decrescente, basta utilizarmos a opção DESC (descendente) no lugar de ASC.

![Ordenação decrescente com Desc](/media/Implementação-de-Banco-de-Dados/aula5/Image26.png)

### Ordenação múltipla

Podemos realizar a ordenação por várias colunas na mesma consulta. Podemos ordenar o resultado por cargo e, a partir da primeira ordenação, dentro de cada cargo por salário. Veja o exemplo abaixo.

![Ordenação múltipla](/media/Implementação-de-Banco-de-Dados/aula5/Image27.png)

Observe que o resultado é inicialmente ordenado pela CARGO de forma DESCENDENTE (VENDEDOR, PRESIDENTE, ETC.) e ao termos uma CARGO repetido (observe o VENDEDOR) as linhas de mesma CARGO são ordenadas entre si por SALARIO de forma ascendente.

No comando, usamos o argumento ASC, mas como é forma padrão de ordenação, poderíamos omiti-lo.

Outra forma de comandarmos a ordenação é pela posição da coluna no resultado. Com isso o comando anterior poderia ser escrito da seguinte forma:

```sql
SELECT *
FROM VEICULO
ORDER BY 2 ASC, 5 DESC
```

Onde os números 4 e 5 referenciam a quarta coluna (CARGO) e a quinta (SALÁRIO), produzindo, dessa forma, o mesmo resultado na consulta.

![Outra forma de realizar a ordenação](/media/Implementação-de-Banco-de-Dados/aula5/Image28.png)
