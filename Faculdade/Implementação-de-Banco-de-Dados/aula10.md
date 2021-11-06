# Aula 10 - Linguagem SQL – Outros objetos de banco de dados

Continuaremos utilizando o banco de dados da empresa para os exemplos.

## Visões (views)

A utilização de visões nos permite materializar o esquema externo de um banco de dados.

Uma visão (view) é uma consulta previamente definida que fica armazenada no dicionário de dados, podendo ser acessada de forma similar a uma tabela. Quando a visão é referenciada em um comando de select, suas linhas e colunas são determinadas dinamicamente, ou seja, a consulta é executada, e o resultado apresentado para o usuário, atuando como um verdadeira tabela virtual.

Uma visão pode permitir, com restrições, que os dados da tabela sejam manipulados em comandos de insert, update e delete; porém, não armazena estes dados.

Vejamos a sintaxe do comando de criação de visões:

```sql
CREATE VIEW nome_view
AS subquery
```

Onde:

| Cláusula  | Descrição                                |
| --------- | ---------------------------------------- |
| Nome_view | É o nome da view.                        |
| subquery  | É o comando select que originará a view. |

Vejamos a sintaxe do comando de criação de visões:

```sql
CREATE VIEW EMP_RESUMO AS
SELECT ID, ULT_NOME, CARGO
FROM EMPREGADO
```

POSTGRESQL

![criação de visões no PostgreSQL](/media/Implementação-de-Banco-de-Dados/aula10/Image1.jpeg)

ORACLE

![criação de visões no Oracle](/media/Implementação-de-Banco-de-Dados/aula10/Image2.jpeg)

SQLSERVER

![criação de visões no SQLServer](/media/Implementação-de-Banco-de-Dados/aula10/Image3.jpeg)

Agora, podemos utilizar EMP_RESUMO como se fosse uma tabela. A diferença é que ela obtém os dados dinamicamente através da query especificada na própria definição da view.

### Consultando Visões

Para recuperarmos dados através da visão, basta executarmos um comando de select no qual o nome da visão fica na cláusula from. Por exemplo: para recuperarmos todas as linhas e colunas da visão EMP_RESUMO, basta darmos o seguintes comandos:

```sql
SELECT *
FROM      EMP_RESUMO
```

![Consultando Visões](/media/Implementação-de-Banco-de-Dados/aula10/Image4.jpeg)

- Ao fazer uma consulta em uma view, podemos usar todos as cláusulas do select, como: where, group by, having order by;

- Podemos também utilizar os operadores relacionais (in, between, like, is null), os operadores lógicos (and, or not) e as funções de grupo;

- Podemos fazer junções de uma tabela com uma visão;

- Podemos fazer subconsultas e utilizar operadores de conjunto;

- Em resumo, podemos utilizar todos os recursos que podem ser utilizados em comandos a partir de tabelas.

### Eliminando Visões

Para eliminar uma visão, basta dar o comando drop view.

![Eliminando Visões](/media/Implementação-de-Banco-de-Dados/aula10/Image5.jpeg)

### Tipos de views

Existem basicamente dois tipos de views: simples e complexos. O tipo simples é composto por apenas um select e utiliza apenas uma tabela; suas colunas são formadas por colunas da tabela original, sem cálculos ou funções. Já a view complexa é aquela em que há um join entre tabelas na subquery.

- Com uma view simples, será possível executarmos os comandos insert, update e delete (além do select);

- A manipulação dos dados através de uma view não desabilita as constraints das tabelas às quais os mesmos se referem;

- Cada coluna definida para views deve ter um nome de coluna válido;

- Caso seja uma fórmula, deve possuir um alias.

Veja um exemplo:

Crie a visão CLI_RESUMO com as colunas ID e nome da tabela cliente.

![Criando a visão CLI_RESUMO](/media/Implementação-de-Banco-de-Dados/aula10/Image6.jpeg)

Agora consulte a visão.

![Consulte a visão](/media/Implementação-de-Banco-de-Dados/aula10/Image7.jpeg)

Note que a nossa visão é simples, então podemos fazer comandos de insert, update e delete através dela. Podemos então inserir um cliente. Veja o comando:

```sql
INSERT INTO CLI_RESUMO VALUES (200,'PINGO DE LEITE')
```

![Utilizando o comando Insert na visão CLI_RESUMO](/media/Implementação-de-Banco-de-Dados/aula10/Image8.jpeg)

Se consultarmos a visão, o novo cliente vai aparecer.

![Consultando a visão](/media/Implementação-de-Banco-de-Dados/aula10/Image9.jpeg)

E, claro, se consultarmos diretamente a tabela, também aparecerá.

![Consultarmos a tabela Cliente](/media/Implementação-de-Banco-de-Dados/aula10/Image10.jpeg)

Note que a coluna Vendedor do novo cliente é nula; isto ocorre devido ao fato de na visão esta coluna não existir.

Um cuidado que você tem de tomar é que, se for inserir através de uma visão, todas as colunas obrigatórias têm que existir na visão, senão ocorrerá um erro, pois a visão não desabilita as restrições da tabela.

## Indexando tabelas

Um índice tem o propósito de acelerar o acesso aos dados de tabelas muito extensas, ou que são frequentemente acessadas via join.

No Oracle, ao criarmos uma primary key ou unique key, automaticamente é definido um índice único de acesso àquelas chaves. Porém, outras colunas que acessamos constantemente poderão ser indexadas, e para isso, temos que conhecer os comandos de criação e eliminação de índices.

### Tipos de índices

1. Único: Garante a unicidade do valor. O índice criado na primary key ou unique key é único; porém, podemos criar restrições de unicidade em outras colunas da tabela;

2. Não único: Índices criados apenas com o propósito de acelerar a pesquisa, como em chaves estrangeiras (foreign key), nas quais a unicidade não é requerida;

3. Uma coluna: Apenas uma coluna será indexada;

4. Colunas compostas ou concatenadas: Até 255 colunas podem ser concatenadas para formar apenas um índice, e não necessitam ser adjacentes.

### Utilizando índices

Devemos utilizar índices sempre que:

1. O meio de acesso tradicional mostrar-se ineficiente, provavelmente pelo tamanho da tabela e um número alto de consultas feitas a ela;

2. A coluna tiver limites extensos de valores;

3. A coluna tiver muitos valores nulos;

4. Duas ou mais colunas são frequentemente acessadas em conjunto numa cláusula where ou condição;

5. A tabela for muito grande e, na maior parte das queries, for esperada a recuperação de até 4% das linhas.

Não devemos utilizar índices sempre que:

1. A tabela for pequena (pode ser armazenada em poucos blocos Oracle);

2. As colunas não são frequentemente usadas em condições;

3. A maior parte das queries recupera mais que 4% das linhas da tabela;

4. A tabela sofre alta taxa de atualização.

Cuidados com índices: É importante observar que os índices são objetos atualizados pelo SGBD, em todas as operações de insert, update e delete na tabela indexada; Portanto, se por um lado aceleram a pesquisa aos dados através do comando select, por outro lado, quanto mais índice tiver a tabela, maior é o seu tempo de atualização.

### Criando um índice

Vejamos a sintaxe do comando a seguir:

```sql
CREATE INDEX [schema.]nome_indice ON tabela (coluna1 [, coluna2 [,...] ] )
```

Onde:

|             |                                                                                                     |
| ----------- | --------------------------------------------------------------------------------------------------- |
| schema      | É o schema no qual será gerado o índice. O default é o schema do usuário que está criando o índice. |
| nome_índice | Nome dado ao objeto índice que será criado.                                                         |
| tabela      | Nome da tabela que será indexada.                                                                   |
| coluna n    | A(s) coluna(s) que irão compor o índice.                                                            |

Veja um exemplo:

Para criar um índice na coluna Vendedor da tabela Cliente, o comando seria:

```sql
CREATE INDEX IND_VEND ON CLIENTE(VENDEDOR)
```

POSTGRESQL

![Criar um índice na coluna Vendedor da tabela Cliente no PostgreSQL](/media/Implementação-de-Banco-de-Dados/aula10/Image11.jpeg)

ORACLE

![criar um índice na coluna Vendedor da tabela Cliente no Oracle](/media/Implementação-de-Banco-de-Dados/aula10/Image12.jpeg)

SQLSERVER

![criar um índice na coluna Vendedor da tabela Cliente no SQLServer](/media/Implementação-de-Banco-de-Dados/aula10/Image13.jpeg)

### Eliminando um índice

Os índices podem ser eliminados, mas nunca alterados. Para alterá-los, devemos efetuar a remoção e depois recriá-los. O comando de eliminação de um índice é simples e exige apenas o privilégio drop index.

Vejamos a sintaxe do comando a seguir:

```sql
DROP INDEX [schema.]nome_índice
```

Onde:

|             |                                                                                                   |
| ----------- | ------------------------------------------------------------------------------------------------- |
| Cláusula    | Descrição                                                                                         |
| schema      | É o schema a quem pertence o índice. O default é o schema do usuário que está removendo o índice. |
| nome_índice | Nome do índice que será removido.                                                                 |

Não podemos eliminar os índices criados automaticamente pelas constraints primary key e unique key. Estes são automaticamente removidos quando eliminamos ou desabilitamos as constraints.

Por exemplo: para eliminar o índice criado na coluna Vendedor, o comando seria:

```sql
DROP INDEX IND_VEND
```

![Eliminando o índice IND_VEND](/media/Implementação-de-Banco-de-Dados/aula10/Image14.jpeg)

## Um gerador de sequências (sequences)

Os SGBDs possuem internamente uma máquina geradora de números sequenciais que pode perfeitamente ser usado para produzir números únicos, consecutivos e incrementados conforme determinado.

A esses números chamamos de sequences, que podem ser utilizados para gerar valores para chaves primárias em tabelas nas quais não existe uma coluna mais apropriada, ou qualquer outra aplicação em que haja a necessidade de números únicos.

A sintaxe do comando de criação de uma sequence é:

```sql
CREATE SEQUENCE   sequence_name
        [INCREMENT BY n ]
        [START WITH n]
        [MAXVALUE n I NOMAXVALUE]
        [MINVALUE n I NOMINVALUE]
        [CYCLE I NOCYCLE]
        [CACHE l NOCACHE]
```

Onde:

| Cláusula     | Descrição                                                                                                                                |
| ------------ | ---------------------------------------------------------------------------------------------------------------------------------------- |
| INCREMENT BY | Especifica o intervalo entre os números sequenciais. Pode ser positivo ou negativo, e a omissão significa incremento positivo de 1 em 1. |
| START WITH   | É o primeiro número da sequência.                                                                                                        |
| MAXVALUE     | Especifica o valor máximo que a sequence pode alcançar.                                                                                  |
| NOMAXVALUE   | É o default. Especifica um valor com precisão de 27 dígitos positivos ou negativos.                                                      |
| MINVALUE     | Especifica um valor mínimo para a sequence.                                                                                              |
| NOMINVALUE   | É o default. Especifica o valor mínimo de 1 para uma sequence ascendente e precisão negativa de 26 dígitos para sequences descendentes.  |
| CYCLE        | Especifica que, após atingido o valor limite, a sequence recomeçará no minvalue ou maxvalue.                                             |
| NOCYCLE      | É o default. Especifica que a sequence não pode gerar mais números após atingir o limite.                                                |
| CACHE        | Especifica quantos números a sequence pré-aloca e mantém em memória para acesso mais rápido.                                             |
| NOCACHE      | Valores não são pré-alocados em memória.                                                                                                 |

Vamos criar uma sequence chamada Números, que terá um valor inicial de 40, será incrementada de 3 em 3 e um valor máximo de 60.

O comando seria:

```sql
CREATE SEQUENCE NUMEROS
       INCREMENT BY 3
       START WITH 40
       MAXVALUE 60;
```

POSTGRESQL

![Criar uma sequence no PostgreSQL](/media/Implementação-de-Banco-de-Dados/aula10/Image15.jpeg)

ORACLE

![Criar uma sequence no Oracle](/media/Implementação-de-Banco-de-Dados/aula10/Image16.jpeg)

SQLSERVER

![Criar uma sequence no SQLServer](/media/Implementação-de-Banco-de-Dados/aula10/Image17.jpeg)

### Obtendo valores da sequence

Cada um dos SGBDs que estudamos recupera os valores da sequence de forma diferente. Vejamos cada um.

**POSTGRESQL**

Este SGBD utiliza uma função chamada Nextval() , cujo retorno é o valor recuperado da sequence.

Veja primeiro no comando de Select:

![Comando de Select com a função Nextval](/media/Implementação-de-Banco-de-Dados/aula10/Image18.jpeg)

Note que o nome da sequence está entre apóstrofes e que o valor retornado é 40, que é o valor inicial que definimos. Agora vamos utilizar em um insert na tabela departamento.

![Comando insert na tabela departamento](/media/Implementação-de-Banco-de-Dados/aula10/Image19.jpeg)

Consultando a tabela, obtemos:

![Consultando a tabela departamento](/media/Implementação-de-Banco-de-Dados/aula10/Image20.jpeg)

Observe que foi inserido o valor 43, já que a sequence incrementa de 3 em 3.

Particularidades de sequences:

1. Quando um número sequencial é gerado pela sequence, este é incrementado independentemente de a transação ter sido efetivada (commit) ou não (rollback);

2. Logo, valores podem ser perdidos para o sistema, ou seja, existirá sempre a garantia de unicidade (caso seja nocycle), porém poderá haver intervalos na aplicação;

3. Temos que ter cuidados com aplicações que manipulam dados fiscais como emissão de notas fiscais. Não devemos numerá-las com sequences;

4. Da mesma forma que usuários acessam a mesma sequence, estes podem receber valores intercalados, visto que num dado momento a sequence poderá estar atendendo um número para cada um;

5. Dois usuários jamais conseguirão gerar o mesmo número sobre uma mesma sequence;

6. Os valores que estão no cache (memória) são perdidos caso o banco de dados sofra uma interrupção anormal.

### Alterando uma sequence

Sequences podem ser submetidas a alteração e eliminação tal qual uma tabela, através dos comandos alter sequence e drop sequence.

Veja a sintaxe do comando:

```sql
ALTER SEQUENCE [schema.]sequence_name
       [INCREMENT BY n ]
       [MAXVALUE n I NOMAXVALUE]
       [MINVALUE n I NOMINVALUE]
```

Controles sobre sequences alteradas:

- Serão afetados apenas os números a serem gerados;

- Algumas validações serão feitas como um novo valor maxvalue; não poderá ser definido se menor que o último número gerado;

- A cláusula start with não poderá ser alterada; neste caso, a sequence deverá ser eliminada e recriada.

### Eliminando uma sequence

Para apagarmos uma sequence, utilizamos o comando drop sequence.

A sintaxe para eliminação de uma sequence:

```sql
DROP SEQUENCE [schema.]sequence_name;
```

Exemplo:

Drop sequence números.

![Eliminando a sequence números](/media/Implementação-de-Banco-de-Dados/aula10/Image21.jpeg)

### Colunas autonumeradas

Conforme já vimos, as sequences podem ser utilizadas para gerar valores para chaves primárias autonumeradas. No Oracle, este é o único, já que este SGBD não possui o tipo de autonumeração. A seguir, vamos verificá-los no SQLServer e PostgreSQL.

**POSTGRESQL**

O tipo autonumerado do PostgreSQL é o serial que deve ser utilizado na PK da tabela.

Veja o comando de criação de tabela:

![Criando a tabela PK_AUTONUMERADA](/media/Implementação-de-Banco-de-Dados/aula10/Image22.jpeg)

Nossa tabela possui duas colunas: a primeira autonumerada e a segunda caracter.

Veja a inserção de duas linhas:

![Inserindo duas linhas na tabela](/media/Implementação-de-Banco-de-Dados/aula10/Image23.jpeg)

Note que na lista de colunas só foi colocada a coluna C2. A C1 terá seu valor preenchido automaticamente, conforme podemos ver na seguinte consulta:

![Consultando os dados da tabela com o Select](/media/Implementação-de-Banco-de-Dados/aula10/Image24.jpeg)
