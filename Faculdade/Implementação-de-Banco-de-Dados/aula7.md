# Aula 07 - Linguagem SQL – Subconsulta e Operadores de Conjunto

Continuaremos usando o banco de dados da empresa para os exemplos.

## Junção exterior (outer join)

Este tipo de junção retorna as linhas que estão relacionadas, como no INNER JOIN, e as não relacionadas de uma ou mais tabelas.

Exemplo: Queremos retornar todos os empregados e os clientes que eles atendem. Este comando seria um comando de junção interior normal, no qual a coluna Vendedor deve ser igualada à coluna ID de empregado. Observe que somente os empregados de ID 5 e 6 atendem algum cliente, portanto apenas eles podem retornar na consulta.

EMPREGADO

![Tabela Empregado](/media/Implementação-de-Banco-de-Dados/aula7/Image1.jpeg)

VENDEDOR = ID

CLIENTE

![Tabela Cliente](/media/Implementação-de-Banco-de-Dados/aula7/Image2.jpeg)

O comando seria então:

```sql
SELECT C.ID, C.NOME, E.ID, E.ULT_NOME, E. CARGO
FROM EMPREGADO E INNER JOIN CLIENTE C ON C.
VENDEDOR = E. ID
```

Que geraria o seguinte resultado:

![Retornando os empregados e os clientes que eles atendem](/media/Implementação-de-Banco-de-Dados/aula7/Image3.jpeg)

Note que no resultado voltam apenas os empregados de id 5 e 6, pois estão relacionados como clientes; os demais não aparecem no resultado (id 1, 2, 3 e 4).

E se desejássemos retornar todos os empregados e para os vendedores os dados dos clientes?

Comandaríamos então uma junção exterior. Neste caso, substituiríamos a expressão inner por left ou right caso a tabela que desejamos retornar esteja do lado esquerdo ou direito do comando.

No caso, como empregado está à esquerda, o comando seria:

```sql
SELECT C.ID, C.NOME, E.ID, E.ULT_NOME, E. CARGO
FROM EMPREGADO E LEFT JOIN CLIENTE C ON C. VENDEDOR = E. ID
```

![Retornando todos os empregados e para os vendedores os dados dos clientes](/media/Implementação-de-Banco-de-Dados/aula7/Image4.jpeg)

Note que as colunas de clientes ficam nulas nas linhas que correspondem aos empregados que não se relacionam com clientes.

E se o comando fosse de right join, o que aconteceria?

```sql
SELECT C. ID, C. NOME, E. ID, E. ULT_NOME, E. CARGO
FROM EMPREGADO E RIGHT JOIN CLIENTE C ON C.
VENDEDOR = E. ID
```

![Aplicando o comando anterior com right join](/media/Implementação-de-Banco-de-Dados/aula7/Image5.jpeg)

Retornaríamos todos os clientes e, para os que não se relacionam com vendedores (Casa Desconto), as colunas de empregado seriam nulas.

Uma terceira forma de fazer a junção exterior é com full join:

![Fazer a junção exterior com full join](/media/Implementação-de-Banco-de-Dados/aula7/Image6.jpeg)

O full join retorna todos os relacionados e os não relacionados das duas tabelas, preenchendo com nulo as colunas da outra tabela para as linhas não relacionadas. Ou seja, é um left e um right realizados em conjunto.

Você pode estar se perguntando: Para que serve isso? Por que eu desejaria retornar os relacionados e os não relacionados?

Normalmente isso ocorre:

1. Quando você deseja saber quais elementos de uma tabela não estão relacionados com os da outra tabela.

2. Quando você precisa fazer uma junção e necessita garantir que retornem todos os elementos de uma determinada tabela.

Vamos discutir cada um destes casos.

Determinar os elementos não relacionados:

Para exemplificar esta situação, vamos incluir mais uma linha na tabela de Região.

```sql
INSERT INTO REGIAO VALUES (3,'Centro')
```

A tabela então ficaria:

![Incluindo mais uma linha na tabela Região](/media/Implementação-de-Banco-de-Dados/aula7/Image7.jpeg)

Se olharmos na tabela de Departamentos, veremos que não existe departamento ligado à região Centro (id_regiao = 3).

![Tabela Departamentos](/media/Implementação-de-Banco-de-Dados/aula7/Image8.jpeg)

Vamos detalhar a primeira situação: quando você deseja saber quais elementos de uma tabela não estão relacionados com os da outra tabela. Portanto, se você desejasse retornar todos os dados das regiões que não têm departamentos, teria de comandar uma junção exterior.

Façamos passo a passo:

1. Fazer a junção exterior:

   Primeiro, temos que determinar como fazer a junção exterior. Para isso, escrevemos o comando retornando todas as colunas das duas tabelas.

![Retornando todas as colunas das duas tabelas](/media/Implementação-de-Banco-de-Dados/aula7/Image9.jpeg)

2. Isolar a região não ligada a departamentos:

   Analisando o retorno, podemos notar que a PK da tabela Departamento (coluna ID) ligada à região Centro é nula. Como vimos, isso acontece devido ao fato de a junção exterior acrescentar ao retorno uma linha toda nula nas colunas da tabela de departamento.

   Desta forma, basta filtrar o resultado por esta coluna para isolar a região Centro:

![Filtramdo o resultado pela coluna id da tabela Departamento para isolar a região Centro](/media/Implementação-de-Banco-de-Dados/aula7/Image10.jpeg)

3. Retornar apenas os dados da Região

   Se você observar vai notar que estão retornando as colunas de departamento (todas nulas). Para retornarem apenas as da Região, basta fazer a projeção:

![Retornando apenas as colunas da Região](/media/Implementação-de-Banco-de-Dados/aula7/Image11.jpeg)

Duas observações importantes:

Note o uso do alias com o \* no select (R.\*). É uma forma otimizada de pedir para retornar todas as colunas de uma das tabelas, sem ter que listá-las na cláusula.

O passo a passo mostrado é meramente didático; o comando da última figura funciona e gera o resultado esperado.

Vejamos agora um exemplo da segunda situação: Quando você precisa fazer uma junção e necessita garantir que retornem todos os elementos de uma determinada tabela. Você deseja retornar o nome da região e o do departamento que fica na região. Para regiões que não têm departamento, retornar o nome da região e o texto “não tem”.

Conforme vimos no caso anterior, a Região 3, Centro, não está ligada a nenhum departamento, portanto se fizéssemos um inner join, ela não retornaria.

![O comando com inner join não retorna a região Centro](/media/Implementação-de-Banco-de-Dados/aula7/Image12.jpeg)

Teremos então que fazer um outer join. Vamos novamente passo a passo:

1. Fazer a junção exterior:

   Primeiro, temos que determinar como fazer a junção exterior; para isto, escrevemos o comando retornando todas as colunas das duas tabelas:

![Retornando todas as colunas das duas tabelas](/media/Implementação-de-Banco-de-Dados/aula7/Image13.jpeg)

2. Projetar as colunas desejadas:

   Como desejamos apenas as colunas Nome da região e Nome do departamento, devemos fazer a sua especificação na cláusula select.

![Consultando as colunas Nome da região e Nome do departamento com a cláusula Select](/media/Implementação-de-Banco-de-Dados/aula7/Image14.jpeg)

3. Substituir o nulo no nome do Departamento pela mensagem “Não tem”:

   Para fazer esta substituição, vamos utilizar uma função chamada COALESCE. Se o primeiro valor nos parênteses for nulo, a função o substitui pelo segundo valor:

![Usando a função COALESCE para fazer a substituição](/media/Implementação-de-Banco-de-Dados/aula7/Image15.jpeg)

Duas observações importantes:

Este comando funciona exatamente da mesma forma no Oracle e no SQLServer.

O passo a passo mostrado é meramente didático; o comando da última figura funciona e gera o resultado esperado.

Finalmente, você pode estar se perguntando: onde está o outer no comando de junção exterior, já que em todos os comandos que demos ele não aparece, ao contrário da junção interior, na qual sempre escrevemos inner?

Na realidade, tanto inner como outer são opcionais. Na próxima figura, podemos ver o comando utilizando outer, e na seguinte, o de inner join somente com join.

![Comando com o outer join](/media/Implementação-de-Banco-de-Dados/aula7/Image16.jpeg)

![Comando de inner join somente com join](/media/Implementação-de-Banco-de-Dados/aula7/Image17.jpeg)

Qual seria o comando para mostrarmos uma lista de todos os gerentes, cada um com seus subordinados?

### Junção exterior – sintaxe tradicional do Oracle

Ao contrário da sintaxe tradicional de inner join, que é igual em todos os SGBDs, existe no Oracle uma sintaxe de outer join proprietária cuja sintaxe tradicional é:

```sql
SELECT nome da tabela1.nome da coluna, nome da tabela2.nome da coluna ....
FROM nome da tabela1, nome da tabela2
WHERE nome da tabela1.nome da coluna (+) = nome da tabela2.nome da coluna
```

Onde: (+) é o símbolo do outer join, que pode ser colocado em quaisquer dos lados da cláusula where, mas não em ambos os lados. Este símbolo deve ser colocado seguindo o nome da coluna, que pode não ter correspondente.

No caso do nosso exemplo, envolvendo clientes e vendedores, no qual desejamos retornar todos os empregados e para os vendedores os dados dos clientes, o comando na sintaxe tradicional seria:

```sql
SELECT C.ID, C.NOME, E.ID, E.ULT_NOME, E. CARGO
FROM CLIENTE C, EMPREGADO E
WHERE C. VENDEDOR (+) = E.ID
```

O resultado pode ser visto na figura e é o equivalente a um right join na sintaxe ANSI.

![Resultado do comando na sintaxe tradicional](/media/Implementação-de-Banco-de-Dados/aula7/Image18.jpeg)

O operador de outer join (+) não tem ligação com o lado da tabela na cláusula from.

Observe na figura o comando invertendo a ordem das tabelas na from e veja que o resultado é o mesmo, equivalendo agora a um left join.

![Resultado após inverter a ordem das tabelas na from](/media/Implementação-de-Banco-de-Dados/aula7/Image19.jpeg)

Na sintaxe tradicional do Oracle, não é possível fazer um full join; o comando gera erro:

![Erro ao dar o comando com full join](/media/Implementação-de-Banco-de-Dados/aula7/Image20.jpeg)

## Autojunção

Uma autojunção [self join] é uma junção da tabela com ela mesma. Na tabela Empregado, por exemplo, cada empregado está subordinado a outro. A coluna 'id_gerente' indica o código do gerente do empregado.

![Tabela Empregado](/media/Implementação-de-Banco-de-Dados/aula7/Image21.jpeg)

Para mostrarmos uma lista de todos os gerentes, cada um com seus subordinados, podemos comandar na sintaxe tradicional:

```sql
SELECT G.ID, G.ULT_NOME, G.CARGO, S.ID, S.ULT_NOME, S. CARGO
FROM EMPREGADO G, EMPREGADO S
WHERE S.ID_GERENTE = G.ID
```

Nesse caso, é obrigatório usar um apelido de tabela para distinguir as duas "cópias" da tabela que estão sendo relacionadas: 'G', no , representa uma linha da tabela Empregado, enquanto Gerente e 'S' representam outra linha, de um subordinado, que estão sendo comparadas entre si.

Podemos ver o resultado dessa consulta:

![Mostrando uma lista de todos os gerentes, cada um com seus subordinados](/media/Implementação-de-Banco-de-Dados/aula7/Image22.jpeg)

Na sintaxe ANSI, o mesmo comando seria:

```sql
SELECT G.ID, G._ULT_NOME, G.CARGO, S.ID, S.ULT_NOME, S. CARGO
FROM EMPREGADO G INNER JOIN EMPREGADOS ON S.ID_GERENTE = G.ID
```

Obteríamos o mesmo resultado da consulta anterior.

![Comando anterior aplicado com a sintaxe ANSI](/media/Implementação-de-Banco-de-Dados/aula7/Image23.jpeg)

Note que na realidade a autojunção não é um tipo de comando de junção; o comando é de inner join; é uma forma de raciocinar para fazer a junção de uma tabela com ela mesma.

## Junção using

Existe uma outra terceira forma de se escrever um comando de junção interior, a junção using, mas o que vem a ser isso?

Repare que, tanto na tabela Departamento quanto na Região, temos uma coluna chamada id_regiao, FK em Departamento e PK em Região, que seria utilizada na cláusula de junção no comando.

![Tabela Departamento e tabela Região](/media/Implementação-de-Banco-de-Dados/aula7/Image24.jpeg)

O comando de junção normal seria:

![Comando de junção normal](/media/Implementação-de-Banco-de-Dados/aula7/Image25.jpeg)

Quando esta situação ocorre, em vez de comandarmos inner join on, podemos comandar inner join using, pondo entre parênteses a coluna comum às duas tabelas. Veja o comando e seu retorno:

![Comando com inner join using](/media/Implementação-de-Banco-de-Dados/aula7/Image26.jpeg)

Compare agora os dois retornos: as linhas que voltam são as mesmas, mas a coluna ID_REGIAO retorna apenas uma vez no using.

Você pode utilizar using para comandos de outer join.

![Comando Right join com using](/media/Implementação-de-Banco-de-Dados/aula7/Image27.jpeg)

A junção using, além do PostgreSQL, funciona no Oracle, mas no SQLServer dá erro.

![Comparação de uso da junção using no Oracle e mensagem de erro no SQLServer](/media/Implementação-de-Banco-de-Dados/aula7/Image28.jpeg)

## Natural join

A junção natural é um tipo de junção que você realiza pelas colunas de mesmo nome de duas tabelas. Embora pareça similar ao using, temos que tomar alguns cuidados. Vamos repetir a junção de Departamento e Região usando natural join:

![Comando com Natural Join](/media/Implementação-de-Banco-de-Dados/aula7/Image29.jpeg)

Note que o comando não deu erro, mas não retornaram linhas. O que aconteceu?

Existem duas colunas de mesmo nome das tabelas (ID_REGIAO e NOME), mas isso não atrapalhou no using, pois especificamos a coluna a ser usada.

![Tabela Departamento e Tabela Região com duas colunas de mesmo nome](/media/Implementação-de-Banco-de-Dados/aula7/Image30.jpeg)

Para podermos fazer a junção natural aqui, somente ID_REGIAO poderia ser comum. Vamos então criar uma nova tabela, cópia de Região, mas chamando a coluna nome com NOMEREG:

![Criando uma tabela cópia de Região e nomeando a coluna como NOMEREG](/media/Implementação-de-Banco-de-Dados/aula7/Image31.jpeg)

Para a criação da tabela, utilizamos o comando select into from, que tem a seguinte sintaxe:

```sql
Select <colunas a serem copiadas>
Into <tabela a ser criada>
From <tabela de origem dos dados>
```

No caso, copiamos as colunas (SELECT) ID_REGIAO e NOME, alterando o nome desta para NOMEREG para dentro (INTO) da tabela CREG a partir (FROM) da tabela Região. Se olharmos agora a estrutura das tabelas Departamento e Região, poderemos notar que existe apenas uma coluna com o mesmo nome entre elas (ID_REGIAO).

![Tabelas Departamento e Região](/media/Implementação-de-Banco-de-Dados/aula7/Image32.jpeg)

Agora o comando de natural join poderá ser executado.

![Executando o comando Natural Join](/media/Implementação-de-Banco-de-Dados/aula7/Image33.jpeg)

Note que, como aconteceu na junção USING ID_REGIAO, retornou uma única vez.

Este comando funciona no Oracle e no SQLServer? Vamos ver; primeiro criaremos a tabela CREG nos dois SGBDs.

O Comando no SQLServer é o mesmo do PostgreSQL, mas no Oracle é diferente: é o comando `create table <nome da tabela> as Select` o que você deseja copiar.

![Criando a tabela CREG no SQLServer e no Oracle](/media/Implementação-de-Banco-de-Dados/aula7/Image34.jpeg)

Vamos comandar agora o natural join nos dois:

![Comando Natural Join no SQLServer e Oracle](/media/Implementação-de-Banco-de-Dados/aula7/Image35.jpeg)

No Oracle, o comando funciona, mas no SQLServer dá erro, como acontece com o using.

## Neoquijoin

Todos os comandos de junção que demos até agora foram feitos com a utilização do sinal de igual (=) na cláusula de junção. Este tipo de junção é chamado de equijoin, ou seja, junção baseada em igualdade. Mas nós podemos dar comando utilizando outros tipos de comparação. Para podemos exemplificar, vamos criar uma tabela chamada Tipo_Salario, com o seguinte comando:

```sql
CREATE TABLE TIPO_SALARIO
(TIPO VARCHAR(20) PRIMARY KEY,
LIMITE_INFERIOR INTEGER,
LIMITE_SUPERIOR INTEGER);
```

A seguir, vamos inserir três linhas:

```sql
INSERT INTO TIPO_SALARIO VALUES ('BAIXO',1000,10000);
INSERT INTO TIPO_SALARIO VALUES ('MEDIO',10001,20000);
INSERT INTO TIPO_SALARIO VALUES ('ALTO',20001,50000);
```

Ao término dos comandos, a tabela ficará com os seguintes dados:

![Tabela Tipo_Salario](/media/Implementação-de-Banco-de-Dados/aula7/Image36.jpeg)

Agora imagine que você deseja recuperar o ID, o sobrenome e o salário do empregado e o seu tipo salarial. Os três primeiros dados estão na tabela de empregados, mas o tipo está na tabela Tipo_Salario.

Temos então que fazer uma junção, mas como, se não temos uma chave que ligue as tabelas?

Queiroz, o empregado de ID 4, ganha 8000. Se você comparar este valor com os limites de cada tipo da tabela Tipo_Salario (figura 34), notará que ele tem um salário do tipo baixo, pois está entre o limite inferior e o superior deste tipo.

![Dados da tabela Empregado](/media/Implementação-de-Banco-de-Dados/aula7/Image37.jpeg)

A forma de fazer a junção, então, é estabelecer uma cláusula de junção que verifique em qual faixa o salário do empregado se encaixa:

![Junção verificando em qual faixa o salário do empregado se encaixa](/media/Implementação-de-Banco-de-Dados/aula7/Image38.jpeg)

Comentário: Este comando funciona exatamente da mesma forma no Oracle e no SQLServer.

![Comando aplicado no SQLServer e no Oracle](/media/Implementação-de-Banco-de-Dados/aula7/Image39.jpeg)

Para podermos visualizar melhor estes comandos, vamos inserir mais uma linha na tabela de Veículos que não terá um proprietário.

![Inserindo mais uma linha na tabela de Veículos](/media/Implementação-de-Banco-de-Dados/aula7/Image40.jpeg)

Observe que o veículo inserido tem Proprietário nulo, ou seja, não está associado a nenhum proprietário.

![Veículo inserido com Proprietário nulo](/media/Implementação-de-Banco-de-Dados/aula7/Image41.jpeg)

Conforme já tínhamos visto, também temos o proprietário MARIANA ROSA, que não está associado a nenhum veículo. Desta forma, ao fazer a junção interior, não retornará nem a Mariana nem o veículo de placa TTZ0156.

![Associando o Propietário Mariana Rosa ao veículo de placa TTZ0156 com Inner Join](/media/Implementação-de-Banco-de-Dados/aula7/Image42.jpeg)

Vamos ver agora como fazer a junção exterior. Neste tipo de junção, temos o conceito de lado. Repare no comando: a tabela Proprietário está à esquerda na cláusula from, e a tabela Veículo à direita.

![Comando aplicado anteriormente](/media/Implementação-de-Banco-de-Dados/aula7/Image43.jpeg)

Se você quiser retornar todos os proprietários, quando apenas os veículos associados como Proprietário estiverem à esquerda, você deverá comandar um left join.

![Retorno do comando com Left Join](/media/Implementação-de-Banco-de-Dados/aula7/Image44.jpeg)

Note que:

- Retornou uma linha com a Mariana Rosa.

- Como não existe um veículo para se associar a Mariana, as colunas de Veículo na linha ficam nulas; isto sempre acontece na junção anterior.

Agora, para voltarem todos os veículos e apenas os proprietários associados, basta trocar left por right.

![Retorno do comando com o Right Join](/media/Implementação-de-Banco-de-Dados/aula7/Image45.jpeg)

Agora retornou o veículo TTZ0156, e as colunas de Proprietário na linha são nulas. Para você voltar todas as linhas associadas e as não associadas das duas tabelas, basta escrever full join.

![Retorno do comando com Full Join](/media/Implementação-de-Banco-de-Dados/aula7/Image46.jpeg)

As utilidades disso são basicamente duas:

1. Suponha que você tenha uma tabela de alunos e uma de fotos, e na de fotos exista uma FK para aluno. Se você deseja retornar todos os alunos para os que têm foto, a única forma é comandar uma junção exterior, pois, na interior, retornariam apenas os alunos que têm foto.

2. Selecionar, por exemplo, o proprietário que não possui veículos. Para obter este resultado, você deve comandar o outer join apropriado (left ou right) e, a seguir, filtrar as linhas cuja chave primária da outra tabela seja nula.

Veja o comando:

![Selecionando o proprietário que não possui veículos](/media/Implementação-de-Banco-de-Dados/aula7/Image47.jpeg)

O comando funciona devido ao fato de uma chave primária nunca poder ser nula, e o nulo, no caso, aparece devido à junção exterior.
