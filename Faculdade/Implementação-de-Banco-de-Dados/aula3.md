# Aula 3 - Linguagem SQL - Select - Parte 1

## Banco de dados de exemplo

Um banco de dados denominado ”Empresa” será utilizado para os exemplos desta aula e das próximas. O Banco da empresa possui o seguinte Modelo Lógico:

![Banco de dados "Empresa"](/media/Implementação-de-Banco-de-Dados/aula3/Image1.png)

As tabelas possuem os seguintes dados:

- Região

- Departamento

- Empregado

- Cliente

Comandos para criação de tabelas:

```sql
CREATE TABLE REGIAO
(ID_REGIAO NUMERIC(7) PRIMARY KEY,
NOME  VARCHAR(40));

CREATE TABLE DEPARTAMENTO
( ID NUMERIC(7) PRIMARY KEY,
NOME VARCHAR(40) NOT NULL,
ID_REGIAO NUMERIC(7)REFERENCES REGIAO(ID_REGIAO));

CREATE TABLE EMPREGADO
( ID NUMERIC(7) PRIMARY KEY,
ULT_NOME VARCHAR(20) NOT NULL,
PRIM_NOME  VARCHAR(20) NOT NULL,
CARGO VARCHAR(30),
SALARIO NUMERIC(7,2),
DT_ADMISSAO DATE,
CPF CHAR(11) UNIQUE,
ID_DEPTO NUMERIC(7) REFERENCES DEPARTAMENTO(ID),
ID_GERENTE NUMERIC(7) REFERENCES EMPREGADO(ID));

CREATE TABLE CLIENTE
( ID NUMERIC(7) PRIMARY KEY
NOME VARCHAR(40) NOT NULL,
VENDEDOR NUMERIC(7) REFERENCES EMPREGADO(ID));
```

INSERINDO LINHAS NA TABELAS

```sql
INSERT INTO REGIAO VALUES (1, 'Norte');
INSERT INTO REGIAO VALUES (2, 'Sul');

INSERT INTO DEPARTAMENTO VALUES (10, 'Administrativo',1);
INSERT INTO DEPARTAMENTO VALUES (20, 'Vendas',1);
INSERT INTO DEPARTAMENTO VALUES (30, 'Compras',2);

INSERT INTO EMPREGADO VALUES (1, 'Velasques', 'Carmen', 'Presidente',29500, '05/05/2009','34567890125',10, null);
INSERT INTO EMPREGADO VALUES (2, 'Neves', 'Lauro', 'Diretor de Compras',19500, '03/03/2009','23456789012',30,1);
INSERT INTO EMPREGADO VALUES (3, 'Nogueira', 'Ernane','Diretor de Vendas', 18000, '07/04/2010','34567890123',20,1);
INSERT INTO EMPREGADO VALUES (4, 'Queiroz', 'Mark','Gerente de Compras',8000, '11/11/2010','12345432123',30,2);
INSERT INTO EMPREGADO VALUES (5, 'Rodrigues', 'Alberto', 'Vendedor',4000, '10/10/2008', '87965432123', 20,3);
INSERT INTO EMPREGADO VALUES (6, 'Ugarte', 'Marlene', 'Vendedor', 3500,'03/03/2009', '87654345678',20,3);

INSERT INTO CLIENTE VALUES (110, 'Ponto Quente',5);
INSERT INTO CLIENTE VALUES (120, 'Casa Supimpa',6);
INSERT INTO CLIENTE VALUES (130, 'Coisas e Tralhas',5);
INSERT INTO CLIENTE VALUES (140, 'Casa Desconto',null);
```

Os comandos listados acima mostram como o script disponível funciona normalmente no postgreSql e no SqlServer. No ORACLE, deve ser comandado COMMIT após o último insert.

Tendo esse Banco em mente, é altamente recomendável que você execute os comandos de exemplo no PostGreSql.

Foi escolhido como base o PostgreSql, por ser um SGBD mais leve e fácil de instalar, porém, se você puder usar o SqlServer ou o Oracle quando houver diferença entre os SGBD’s, será avisado.

## Consultando dados de uma tabela

O comando SQL que permite recuperar dados de uma ou mais tabelas é o SELECT. Esse comando nos permite escolher as colunas que retornarão, bem como filtrá-las da tabela.

O comando de Select é uma implementação prática da teoria dos conjuntos, mais especificamente da Álgebra Relacional. Dessa forma, um único Select pode retornar zero ou várias linhas, de acordo com as restrições colocadas no comando.

Os componentes básicos do comando são:

Cláusula **SELECT**

- Lista as colunas que serão recuperadas;

- Se utilizarmos o artifício do \* (asterisco) na cláusula SELECT, estaremos definindo que todas as colunas serão recuperadas.

Cláusula **FROM**

- Define a tabela que será recuperada.

Veja a sintaxe abaixo:

```sql
SELECT nome-col1, nome_col2, nome coln
FROM    nome_da_ tabela;
```

**OU**

```sql
SELECT *
FROM    nome_da_tabela ;
```

**Em que:**

| Palavra-Chave  | Descrição                                               |
| -------------- | ------------------------------------------------------- |
| nome_da_tabela | Nome da tabela que contém os dados a serem recuperados. |
| nome_coln      | Nome de uma coluna a ser recuperada.                    |
| \* (asterisco) | Recupera todas as colunas da tabela.                    |

### Retornando uma tabela inteira

Acesse o SGBD e digite o seguinte comando: `SELECT * FROM EMPREGADO`.

No comando acima, selecionamos todas as colunas e todas as linhas da tabela EMPREGADO.

![Selecionando todas as colunas e todas as linhas da tabela Empregado](/media/Implementação-de-Banco-de-Dados/aula3/Image2.jpeg)

Observe que não há nenhuma ordem ou seleção de linhas ou colunas.

### Retornando colunas específicas

Na Álgebra Relacional, vimos que existe a operação de projeção que permite retornar apenas algumas colunas da tabela, mas todas as linhas. O mesmo pode ser obtido em SQL. Para isso basta que se liste as colunas desejadas na cláusula SELECT, separando-as por virgulas.

**Exemplos:**

Acesse o SGBD e digite o seguinte comando: `SELECT ID, PRIM_NOME, ULT_NOME FROM EMPREGADO`.

No comando acima, são selecionadas apenas três colunas e todas as linhas da tabela EMPREGADO.

![Selecionando as colunas Id, PRIM_NOME e ULT_NOME da tabela Empregado](/media/Implementação-de-Banco-de-Dados/aula3/Image3.jpeg)

Nesse segundo caso, não são exibidas as colunas CARGO, SALARIO, DT_ADMISSAO, CPF, ID_DEPTO e ID_GERENTE.

No primeiro comando analisado, um asterisco substitui a lista de colunas desejadas, indicando que todas as colunas devem ser informadas.

Como seria o comando para exibir todo o NOME e o ID de todos os clientes?

![Exibindo o NOME e o ID de todos os clientes](/media/Implementação-de-Banco-de-Dados/aula3/Image4.jpeg)

COMANDO:

![Comando para exibir o NOME e o ID da tabela Cliente](/media/Implementação-de-Banco-de-Dados/aula3/Image5.jpeg)

- Quando você utiliza \*, as colunas retornam na ordem em que foram criadas na tabela;

- Quando você lista as colunas no SELECT, elas retornam na ordem em que as listou;

- As colunas no SELECT devem estar separadas por vírgula;

- Não deve existir vírgula antes da cláusula FROM.

## Escrevendo expressões de concatenação

No PostGreSql, o operador de concatenação é o ||. Se desejássemos retornar o PRIM_NOME do empregado com o ULT_NOME, o comando seria:

```sql
SELECT PRIM_NOME || ULT_NOME
FROM EMPREGADO
```

![Concatenando o PRIM_NOME com o ULT_NOME da tabela empregado](/media/Implementação-de-Banco-de-Dados/aula3/Image6.jpeg)

Notou que os nomes estão colados?

Isso decorre do fato de que, depois do PRIM_NOME ou antes do ULT_NOME, não existe espaço em branco armazenado na coluna.

Como resolver isso? Basta concatenar as colunas com um espaço em branco entre elas.

![Concatenando as colunas com um espaço em branco entre elas](/media/Implementação-de-Banco-de-Dados/aula3/Image7.jpeg)

Como fica isso no Oracle e no Sql Server?

No Oracle, o operador é o mesmo.

![Concatenação no Oracle](/media/Implementação-de-Banco-de-Dados/aula3/Image8.jpeg)

Já no SqlServer, o operador de concatenação é o +.

![Concatenação no SqlServer](/media/Implementação-de-Banco-de-Dados/aula3/Image9.jpeg)

**Criando Alias**

Quando são utilizadas expressões, o cabeçalho da coluna, normalmente, fica sem significado.

Dependendo do SGBD, ele pode ser a própria expressão, como acontece no ORACLE, pode ser (No column name), como acontece no SQLSERVER, ou pode ser ?Column?

Como acontece no PostgreSQL.

Seja como for, seria mais interessante se fosse possível nomear as colunas de forma a manterem o seu significado. Para isso, existem os alias de coluna.

**PostGreSql**

![Cabeçalho da coluna no PostgreSQL](/media/Implementação-de-Banco-de-Dados/aula3/Image10.png)

**SqlServer**

![Cabeçalho da coluna no SqlServer](/media/Implementação-de-Banco-de-Dados/aula3/Image11.png)

**Oracle**

![Cabeçalho da coluna no Oracle](/media/Implementação-de-Banco-de-Dados/aula3/Image12.png)

Para você criar um alias após a coluna, você deve colocar ‘AS’ e em seguida a palavra - sem espaços em branco e sem caracteres em português - que usará para ser o cabeçalho da coluna.

Para chamar a concatenação do PRIM_NOME com o ULT_NOME como NOME_COMPLETO, você deve comandar:

```sql
SELECT PRIM_NOME ||' '|| ULT_NOME AS NOME_completo
FROM EMPREGADO
```

**PostGreSql**

![Coluna NOME_COMPLETO no PostgreSQL](/media/Implementação-de-Banco-de-Dados/aula3/Image13.png)

**SqlServer**

![Coluna NOME_COMPLETO no SqlServer](/media/Implementação-de-Banco-de-Dados/aula3/Image14.png)

**Oracle**

![Coluna NOME_COMPLETO no Oracle](/media/Implementação-de-Banco-de-Dados/aula3/Image15.png)

1. Repare que no comando o alias está com NOME em maiúsculo e completo em minúsculo. Analise agora o retorno e note que no PostGreSql o alias fica todo em minúsculo, no Oracle todo em maiúsculo e no SqlServer da forma que você digitou o alias.

2. O AS nos 3 SGBD é opcional. Se você escrever o comando sem o AS, ele funciona. Teste para ver.

## Utilizando SELECT sem FROM

A cláusula SELECT, além de permitir a realização da projeção das colunas da tabela, pode ser utilizada para exibir resultados de operações aritméticas, retorno de funções ou textos.

Vejamos um exemplo no PostGreSql:

![Comando Select sem FROM para exibir um texto, operação aritmética e retorno de função](/media/Implementação-de-Banco-de-Dados/aula3/Image16.jpeg)

Note que:

- O comando primeiro exibe um texto (ALO), em seguida o resultado de uma operação aritmética (9+5) e finalmente retorna o valor da data da data/hora do sistema (FUNÇÃO NOW());

- Não existe cláusula FROM, pois desejamos retornar apenas uma linha com os valores.

O que aconteceria se fosse acrescentada uma cláusula FROM com um nome de tabela?

![Acrescentando uma cláusula FROM ao comando anterior](/media/Implementação-de-Banco-de-Dados/aula3/Image17.jpeg)

Note na figura acima que retornaram 4 linhas todas iguais. Isso acontece porque tanto as expressões como a função NOW() são de linha, ou seja, retornam uma linha para cada linha da tabela da cláusula FROM. Como a tabela CLIENTE possui 4 linhas, o retorno tem essa quantidade de linhas.

Por isso é omitida a cláusula FROM, já que desejamos apenas uma linha de retorno.

E o SqlServer, como fica? Muito Similar. A única diferença é que a função que retorna a data/hora se chama GETDATE().

![Comando no SqlServer com a função GETDATE](/media/Implementação-de-Banco-de-Dados/aula3/Image18.jpeg)

Como no PostgreSql, se tiver FROM, retornará uma linha para cada linha da tabela.

![Comando Select com a cláusula FROM no SqlServer](/media/Implementação-de-Banco-de-Dados/aula3/Image19.jpeg)

Faltou o Oracle. A função de data do Oracle é SYSDATE. Veja na figura abaixo o retorno do comando

![Comando Select sem a cláusula FROM no Oracle](/media/Implementação-de-Banco-de-Dados/aula3/Image20.jpeg)

Note que deu o erro, pois a cláusula From não foi encontrada. Por que isso acontece? Ao contrário do PostGreSql e do SqlServer, no Oracle a cláusula FROM é obrigatória. Como fazemos então para conseguir listar os valores? Colocamos a Cláusula FROM com a tabela DUAL.

![Utilizando a cláusula FROM com a tabela DUAL no Oracle](/media/Implementação-de-Banco-de-Dados/aula3/Image21.jpeg)

Observações:

- Sysdate também pode retornar a hora mas temos que fazer algumas configurações que ultrapassam o nosso escopo aqui.

- Como vimos antes no SqlServer e no PostgreSql também podemos colocar a cláusula FROM com um nome de tabela, só que retornaram uma linha para cada linha da tabela, mas como a cláusula FROM não é obrigatória não é um problema.

- No Oracle se colocarmos uma tabela com 4 linhas na FROM retornaram 4 linhas, como a cláusula FROM é obrigatório isto poderia gerar um problema. Para eliminar esta dificuldade existe uma tabela de sistema chamada DUAl que possui uma única linha e que deverá ser colocada na cláusula FROM sempre que se desejar retornar uma única linha com expressões ou funções de linha.

Se por curiosidade você quiser saber o conteúdo de DUAL, basta comandar:

![Verificando o conteúdo de DUAL](/media/Implementação-de-Banco-de-Dados/aula3/Image22.jpeg)

Você verá que a tabela possui uma única coluna chamada DUMMY e uma Linha com o valor X.

**Importante**: DUAL é uma tabela de sistema em que nenhum usuário pode DROPAR ou INSERIR linhas, tampouco ALTERAR ou ELIMINAR sua única linha.
