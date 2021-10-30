# Aula 06 - Linguagem SQL – junção

Continuaremos usando o banco de dados da empresa para os exemplos.

## Junções de tabelas

O banco de dados da EMPRESA possui, na tabela DEPARTAMENTO, os dados dos departamentos e, na tabela REGIÃO, os dados regiões.

Se você reparar no esquema da tabela DEPARTAMENTO, vai notar a existência de uma chave estrangeira (ID_REGIAO) para a tabela REGIÃO que nos permite saber a região a que o departamento pertence.

Se você deseja pegar dados dos departamentos e de sua região, por exemplo, vai utilizar a FK ID_REGIAO para ligar as linhas das duas tabelas, fazendo uma junção.

Lembre-se que, na modelagem lógica, os relacionamentos são mapeados em chaves estrangeiras. Desta forma, fazer junção nada mais é que recuperar os dados das entidades que estão relacionadas nas duas tabelas.

Tipos de junção:

- Junção cruzada: retorna o produto cartesiano das duas tabelas, ou seja, a combinação de todas as linhas de uma tabela com todas as linhas de outra tabela.

- Junção interior: neste tipo, retornam as linhas que estão relacionadas nas duas tabelas.

- Junção exterior: neste tipo, retornam as linhas relacionadas e as não relacionadas em uma ou duas tabelas.

Sintaxe da junção: os comandos de junção interior e junção cruzada podem ser escritos de duas formas diferentes, ou seja, em duas sintaxes diferentes. Uma delas é a tradicional, mais antiga e a segunda é a sintaxe ANSI.

- Tradicional: Na cláusula from, listamos as tabelas com seus nomes separados por vírgula e, no caso da junção interior, na cláusula where deve ser escrita a condição de junção [join condition], que as linhas devem atender para participarem da resposta.

- ANSI: Na cláusula from, deve ser especificado o tipo de junção que estamos realizando com a condição de junção sem ser estabelecida na subcláusula on.

Os comandos de junção exterior, na maioria dos SGBDs, serão escritos na sintaxe ANSI.

## Junção cruzada (cross join)

Este tipo de junção gera a combinação de todas as linhas de uma tabela com todas as linhas da outra tabela; é o chamado **produto cartesiano**.

Como a junção cruzada, combinadas todas as linhas das duas tabelas, não existe uma condição de junção.

Observe o conteúdo das tabelas Departamento e Região:

![Tabelas Departamento e Região](/media/Implementação-de-Banco-de-Dados/aula6/Image1.png)

Se você comandar a junção cruzada das duas tabelas, o que irá acontecer?

A tabela Veículo possui 10 linhas e modelo 5. O resultado final terá então 50 linhas, já que cada uma das linhas da tabela será combinada com todas as linhas de Modelo.

Na sintaxe tradicional, o comando será:

```sql
SELECT *
FROM DEPARTAMENTO, REGIÃO
```

![Retornando os dados das tabelas Departamento e Região](/media/Implementação-de-Banco-de-Dados/aula6/Image2.png)

Note que:

1. Retornam seis linhas.

2. Se você olhar a última coluna (nome da região primeiro), temos a região Norte, associada a todos os três departamentos, e depois Sul associada a todos os departamentos.

3. Se existissem mais regiões, o descrito no item 2 se repetiria para todas.

4. As linhas 1 e 4 são do mesmo departamento, já que é o início de um novo conjunto de linhas ligadas à mesma região.

5. Não existe condição de junção.

6. O esquema do retorno, ou seja a ordem das colunas, é a justaposição das colunas da primeira tabela da cláusula from com as da segunda. Se você inverter a ordem na cláusula from, o retorno também será invertido, como mostra a figura a seguir.

![Invertendo a ordem das colunas na cláusula from](/media/Implementação-de-Banco-de-Dados/aula6/Image3.jpeg)

Já na sintaxe ANSI, devemos escrever na cláusula from o tipo de junção comandado.

```sql
SELECT *
FROM DEPARTAMENTO CROSS JOIN REGIAO
```

![Usando o Cross Join na cláusula From](/media/Implementação-de-Banco-de-Dados/aula6/Image4.jpeg)

Observe agora o seguinte comando:

```sql
SELECT *
FROM EMPREGADO
CROSS JOIN DEPARTAMENTO
CROSS JOIN REGIAO
```

![Retorno do comando anterior com o produto cartesiano das três tabelas](/media/Implementação-de-Banco-de-Dados/aula6/Image5.jpeg)

Ele faz o produto cartesiano das três tabelas, gerando 36 linhas (6 empregados X 3 departamentos X 2 regiões).

Em qualquer comando de junção, independentemente da sintaxe, podemos determinar as colunas que desejamos, basta listá-las no Select.

Se você desejasse retornar apenas o nome do departamento e o nome da região, poderia comandar:

```sql
SELECT NOME, NOME
FROM DEPARTAMENTO CROSS JOIN REGIAO
```

Correto? Não; veja o erro do comando:

![Erro ao tentar retornar apenas o nome do departamento e o nome da região](/media/Implementação-de-Banco-de-Dados/aula6/Image6.jpeg)

Analise a mensagem de erro. Ela diz que a coluna nome é ambígua. Como assim, ambígua?

Acontece que tanto a tabela Departamento como a tabela Região têm uma coluna com o título Nome, e o SGBD não sabe qual delas utilizar no comando. A solução é qualificar a coluna, ou seja, colocar o nome da tabela seguido do nome da coluna ligados por um ponto, da seguinte forma:

![Qualificando a coluna no comando](/media/Implementação-de-Banco-de-Dados/aula6/Image7.jpeg)

Esta solução, a qualificação como o nome da tabela, pode ser trabalhosa, já que os nomes de tabela podem ter até 40 caracteres. Uma forma para resolvermos isso é apelidarmos as tabelas e usarmos este apelido para qualificarmos as colunas.

Um apelido (também chamado de alias) de tabela nada mais é que uma ou mais letras colocadas logo depois do nome da tabela na cláusula FROM.

Observe este comando e reflita:

![Utilizando um apelido de tabela](/media/Implementação-de-Banco-de-Dados/aula6/Image8.jpeg)

Atenção: Depois que você cria o apelido, não pode mais utilizar o nome da tabela para qualificar as colunas.

## Junção interior (inner join)

Este tipo de junção recupera as linhas relacionadas nas tabelas envolvidas na junção.

Se você desejasse retornar os dados do departamento e os da região a que o departamento pertence, seria este tipo de junção que deveria comandar. O fato de retornarem as linhas relacionadas apenas acarreta que, se existem departamentos sem região ou região que não tem departamentos, estes não aparecem no resultado.

O Inner join é também chamado de Equijoin quando a condição de junção utiliza a igualdade, ou seja, quando o valor da coluna de uma tabela (normalmente a chave estrangeira) é igual ao valor da coluna na outra tabela (normalmente a chave primária).

Essa junção pode ser comandada tanto na sintaxe tradicional como na ANSI.

### Junção interior – sintaxe tradicional

```sql
select <colunas>
from tabela1, tabela2
where <condição de junção>;
```

Condição de junção é uma expressão de comparação entre as colunas das duas tabelas envolvidas, normalmente a chave de primária de uma com a chave estrangeira da outra.

Na realidade, a sintaxe tradicional pode ser entendida como o produto cartesiano das duas tabelas seguido de uma seleção utilizando a cláusula where.

Vamos comandar a junção de Departamento e Região. A coluna ID_REGIAO em departamento é uma FK para a tabela Região, que tem como PK a coluna ID_REGIAO. Desta forma, o comando seria:

```sql
SELECT *
FROM DEPARTAMENTO D, REGIAO R
WHERE D.ID_REGIAO = R.ID_REGIAO
```

![Comando de junção das tabelas Departamento e Região com a sintaxe tradicional](/media/Implementação-de-Banco-de-Dados/aula6/Image9.png)

### Junção interior – sintaxe ANSI

Na sintaxe ANSI, junções interiores são indicadas com inner join:

```sql
select <colunas>
from tabela1 INNER JOIN tabela2 ON <condição de junção;>
```

No caso anterior, o comando seria:

```sql
SELECT *
FROM DEPARTAMENTO D
INNER JOIN REGIAO R ON D.ID_REGIAO = R.ID_REGIAO
```

![Realizando junção interior com a sintaxe ANSI](/media/Implementação-de-Banco-de-Dados/aula6/Image10.jpeg)

### Junção interior de mais de duas tabelas

Podemos fazer a junção de mais de duas tabelas. Para isto, basta acrescentarmos uma nova tabela com uma nova cláusula de junção.

Vejamos um exemplo inicialmente na sintaxe ANSI. A primeira coisa a fazer é identificar quais tabelas podem se juntar. Analise o modelo do banco:

![Modelo do banco de dados da empresa](/media/Implementação-de-Banco-de-Dados/aula6/Image11.jpeg)

Temos uma FK de Empregado para Departamento e uma FK de Departamento para Região. Desta forma, temos que comandar a junção de Empregado com Departamento, que gera uma tabela intermediária em memória, e juntar este resultado com Região.

![Unindo o resultado da junção de Empregado com Departamento com a tabela Região](/media/Implementação-de-Banco-de-Dados/aula6/Image12.jpeg)

O mesmo comando na sintaxe tradicional seria:

![Comando de junção na sintaxe tradicional](/media/Implementação-de-Banco-de-Dados/aula6/Image13.jpeg)

Neste caso, colocamos as tabelas na cláusula from e as condições de junção no where, ligadas por and.
