# Aula 1 - Álgebra relacional

Os Sistemas de Banco de Dados atuais são, majoritariamente, baseados no Modelo Relacional. Como o modelo relacional teve sua origem na matemática, essa mesma ciência nos fornece a ferramenta para manipulá-lo, a Álgebra Relacional.

Dado é o “princípio em que se assenta uma discussão” ou o “elemento ou base para a formação de um juízo”. Ainda, assumindo-se um ponto de vista mais filosófico, dado é “o que se apresenta à consciência como imediato, não construído ou não elaborado”, FERREIRA et al. (1999, p. 602).

Essas definições são úteis para exemplificar o termo "dado" e situar sua definição de um ponto de vista mais humanizado.

Computacionalmente falando, pode-se definir **dado** como um valor armazenado e que por si só não quer dizer muita coisa. Uma lista de números - por exemplo, 10, 12, 20, 21, 23, 38 - não nos fornece nenhum significado, mas, por assim dizer, são os dados obtidos e anotados de alguma forma.

A necessidade de armazenar os dados precede a criação do conceito de Sistemas de Banco de dados.

Antigamente, os dados eram armazenados em arquivos. Normalmente são associados a um único sistema de aplicação, trazendo, por consequência, redundância de dados quando os mesmos se faziam necessários em outros sistemas.

## Sistema baseado em arquivo

1. Cada aplicação possui seus próprios arquivos de dados;

2. Se uma aplicação compartilha dados com outras, esses têm que ser duplicados;

3. Qualquer alteração no modelo de dados implica em alteração do código da aplicação.

![Sistema baseado em arquivo](/media/Implementação-de-Banco-de-Dados/aula1/image.png)

Isso acaba acarretando em:

- **Redundância de dados**: Trata-se da **duplicação dos mesmos dados em dois ou mais arquivos**. O problema com a redundância é que as mudanças, ao serem feitas no arquivo de uma aplicação, não são automaticamente realizadas nos arquivos das outras aplicações, gerando a falta de integridade dos dados.

- **Dependência entre programas e dados**: Os aplicativos tradicionais de banco de dados de arquivos são **caracterizados pela dependência entre programas e dados**, isso é, programas e dados desenvolvidos e organizados para uma aplicação são incompatíveis com os programas e dados organizados diferentemente para um outro aplicativo.

- **Custo excessivo em software**: Resulta da criação, documentação e acompanhamento de muitos arquivos e aplicações diferentes.

A evolução da tecnologia associada ao aumento de volume de dados a ser armazenado levou à criação do Sistema de Banco de Dados. Um banco de dados é uma **coleção de dados organizados de forma que possam ser acessados e utilizados por muitas aplicações diferentes**. Em vez de armazenar dados em arquivos separados para utilização, os dados são armazenados e organizados em um só local, permitindo compartilhamento e inter-relacionamento por múltiplos usuários.

Um software adicional foi necessário para o gerenciamento dos dados, o SGBD (sistema de gerenciamento de banco de dados). Consiste em um grupo de programas que podem ser usados como uma interface entre o banco de dados e um usuário ou um banco de dados e um programa aplicativo.

![Sistema de gerenciamento de banco de dados](/media/Implementação-de-Banco-de-Dados/aula1/Image1.png)

## Modelo relacional

Nos maiores SGBD comerciais, o modelo de dados utilizado é o Modelo Relacional criado com base na Teoria Matemática dos Conjuntos e na Álgebra Relacional, O Modelo de Dados Relacional tem as seguintes vantagens:

- É independente das linguagens de programação;

- É independente dos sistemas de gestão de bases de dados;

- É independente dos Sistemas Operacionais.

> “O modelo relacional representa o banco de dados como uma coleção de relações.”
> ELMASRI, R.; NAVATHE, S., 2015.

Pode-se depreender uma relação como uma tabela de valores onde cada **linha representa uma coleção de dados ou valores relacionados**. **Cada linha da tabela representa uma realidade ligada ao mundo real**. O nome da tabela e o nome das colunas são definidos de forma que representem essa realidade. Pode-se ter uma tabela chamada ALUNO onde cada linha venha a ser o Nome de um Aluno a ser armazenado.

Podemos melhorar ainda mais essa representação, criando uma tabela com as colunas NOME, NÚMERO DE MATRÍCULA e CLASSE. **Cada linha da tabela representa várias informações de um ALUNO e cada coluna isoladamente, representa uma informação específica desse aluno**. Assim o nome da tabela e os nomes das colunas são capazes de dizer o que cada linha representa e também o que o conjunto representa.

No modelo relacional formal, cada **linha é chamada de tupla**, o nome da **coluna é conhecido como atributo ou variável**, e a **tabela, relação**. (FONSECA, 2016)

### Regras de integridade relacional

Visam garantir a fidelidade de informações em um banco de dados. Basicamente são três as formas mais comuns:

- **Integridade de domínio**: Diz respeito aos dados que são **permitidos nas colunas da relação (tabela)**. Um domínio é um **conjunto de valores do mesmo tipo**. Os domínios são, portanto, **conjuntos/faixas de valores a partir dos quais os valores reais são adicionados às colunas de uma tabela.**

- **Integridade de entidade**: Diz respeito à **unicidade de linhas da relação**. Para tal, cada tabela deve ter uma **chave primária (Primary Key - PK)**. Dessa forma, as colunas escolhidas para **PK devem ser únicas e de preenchimento obrigatório (não nulas)**.

- **Integridade referencial**: Diz respeito à **consistência entre as tuplas de relações**. Para tal, as tabelas devem possuir **chaves estrangeiras (Foreign Key – FK)**. A FK de uma tabela com, por exemplo, CodigoDepto na tabela EMP deve referenciar uma PK de outra tabela, no caso CodigoDepto da tabela Depto. Os valores possíveis em uma FK são limitados aos existentes na PK referenciada. Se em um banco de dados você tentar incluir uma linha com valor de FK não existente na PK da outra tabela, o SGBD gerará um erro e não permitirá a operação, garantindo assim a consistência dos dados.

![Banco de dados relacional](/media/Implementação-de-Banco-de-Dados/aula1/Image2.png)

Chave primária e chave estrangeira são conceitos importantes na modelagem de dados, pois implementam restrições que garantirão ao futuro banco de dados a integridade dos dados.

**Chave primária**: Atributo ou combinação de atributos que possuem a propriedade de identificar de forma única uma linha da tabela.

**Chave estrangeira**: A chave estrangeira ocorre quando um atributo de uma relação for chave primária em outra relação.

Na terminologia do modelo relacional formal, uma linha é chamada tupla, um cabeçalho de coluna é conhecido como atributo, e a tabela é chamada relação. O tipo de dado que descreve os tipos de valores que podem aparecer em cada coluna é representado pelo domínio de valores possíveis.

Uma tupla é uma linha de registro. Não faz sentido termos duas linhas de registros iguais. Principalmente se houver uma chave primária definida.

## Álgebra relacional

É o conjunto básico de operações para o modelo relacional. Essas operações permitem a **recuperação de tuplas** mediante instruções de consulta aplicadas ao banco de dados. O resultado dessa recuperação também será uma relação, que pode ser usada em outras operações de consulta.

A importância da álgebra relacional:

- Provê fundamento formal para operações do modelo relacional;

- Alguns de seus conceitos são incorporados na linguagem SQL padrão.

- E o mais importante: é usada como base para implementar e otimizar as consultas em sistemas de banco de dados relacional. (FONSECA, 2016, p. 15)

As principais operações da álgebra relacional são:

1. Seleção

2. Projeção

3. Produto cartesiano

4. Operações de conjunto (união, intersecção, diferença)

As operações de **SELECT (SELEÇÃO)** e **PROJECT (PROJEÇÃO)** são ditas operações unárias, pois atuam em relações únicas (ELMASRI, R.; NAVATHE, S., 2015).

### Operação de seleção

A operação de **Seleção** recupera os dados de uma ou mais tabelas, selecionando um subconjunto de tuplas que satisfaça determinada condição de seleção. Essa condição de seleção é usada para dividir horizontalmente uma relação em dois conjuntos de tuplas – as tuplas que satisfazem a condição e são retornadas e as tuplas que não satisfazem a condição e são ignoradas. (FONSECA, 2016, p.16)

A forma geral de uma operação de seleção é:

```sql

(nome da relação)<condição de seleção> σ

```

Onde:

**\<condição de seleção>** é a condição que a linha deve atender para ser selecionada.

Constituindo-se em uma expressão lógica, é construída a partir de cláusulas da forma: **\<nome de atributo>** **\<operador de comparação>** **\<valor constante >** ou **\<nome de atributo> \<operador de comparação> \<nome de atributo >**

Onde:

**\<nome de atributo>** é um atributo da relação definida em **\<nome da relação>**, **\<operador de comparação>** é normalmente um dos operadores relacionais **\{=, <, =<, =>, !=}** e **\<valor constante>** é um literal.

As cláusulas podem ser utilizadas em conjunto com os operadores lógicos {AND, OR NOT}, seguindo a Lógica Booleana, para formar uma condição de seleção composta.

**\<nome da relação>** é o nome da relação sobre a qual será aplicada a operação de **Seleção**. A relação resultante da operação tem os mesmos atributos da relação especificada em **\<nome da relação>**.

![Operação de seleção](/media/Implementação-de-Banco-de-Dados/aula1/Image3.png)

Exemplo:

Nome da tabela: **Disciplina_Nota**

|     | NOME_ALUNO     | NOME_DISCIPLINA | NOTA |
| --- | -------------- | --------------- | ---- |
| 1   | José Geraldo   | Álgebra         | 8    |
| 2   | Eduardo Tomaz  | Álgebra         | 10   |
| 3   | Cleber Dutra   | Álgebra         | 9    |
| 4   | Hernesto Paula | Álgebra         | 10   |
| 5   | Josué José     | Álgebra         | 10   |

Para selecionar os alunos da disciplina ‘álgebra’ cuja nota foi integral, pode-se especificar cada uma dessas condições em uma operação de SELEÇÃO:

```sql

NOME_DISCIPLINA = ‘ALGEBRA’ AND NOTA = 10 (Disciplina_Nota)

NOME_DISCIPLINA = ‘ALGEBRA’ AND NOTA = 10

```

Resultando a nova relação:

|     | NOME_ALUNO    | NOME_DISCIPLINA | NOTA |
| --- | ------------- | --------------- | ---- |
| 1   | Eduardo Tomaz | Álgebra         | 10   |
| 2   | Josué José    | Álgebra         | 10   |

### Operação de Projeção

A operação de Projeção recupera os dados de certas colunas de uma tabela e descarta outras. Se existir a necessidade de mostrar apenas alguns atributos de uma tabela em detrimento de outros, usa-se a operação PROJEÇÃO. (FONSECA, 2016, p. 17)

A forma geral da operação de projeção é:

```sql

π <lista de atributos> (<nome da relação>)

```

Onde:

**\<lista de atributos>** representa a lista de atributos que o usuário deseja selecionar e **\<nome da relação>** representa a relação sobre a qual a operação **projeção** será aplicada.

![Operação de Projeção](/media/Implementação-de-Banco-de-Dados/aula1/Image4.png)

Exemplo:

Para selecionar as disciplinas e as ocorrências de notas nas disciplinas na tabela da fig 4, teremos:

`π <Nome_Disciplina,Nota>(<Disciplina_Nota>)`

Resultando na relação:

|     | NOME_DISCIPLINA | NOTA |
| --- | --------------- | ---- |
| 1   | Álgebra         | 8    |
| 2   | Álgebra         | 9    |
| 3   | Álgebra         | 10   |
| 4   | Álgebra         | 10   |

### Sequencialidade de Operações

A Projeção e a Seleção podem ser combinadas, de forma que apenas algumas linhas e algumas colunas retornem na operação. A forma geral de uma operação sequencializada é:

```sql

π <lista de atributos> (σ <condição de seleção> (<nome da relação>))

```

Onde:

- π representa a operação de projeção;

- **\<lista de atributos>** representa a lista de atributos que o usuário deseja selecionar;

- σ representa a operação de seleção;

- **\<condição de seleção>** é a condição que a linha deve atender para ser selecionada;

- **\<nome da relação>** é o nome da relação sobre a qual será aplicada a operação de Seleção e Projeção

![Sequencialidade de Operações](/media/Implementação-de-Banco-de-Dados/aula1/Image5.png)

Para projetar a partir da Tabela Disciplina_Nota, o nome das disciplinas e a nota para alunos com nota diferente de 10 a expressão seria:

`π Nome_Disciplina, Nota( σ <> 10 (Disciplina_Nota))`

|     | NOME_DISCIPLINA | NOTA |
| --- | --------------- | ---- |
| 1   | Álgebra         | 8    |
| 2   | Álgebra         | 9    |

## Operação Produto Cartesiano

O produto cartesiano é uma operação binária que combina todas as tuplas de duas tabelas. O resultado de um produto cartesiano é uma nova tabela formada pela combinação das tuplas das tabelas sobre as quais aplicou-se a operação.

O formato geral do produto cartesiano entre duas tabelas A e B é:

![Operação Produto Cartesiano](/media/Implementação-de-Banco-de-Dados/aula1/Image6.png)

## Operação Junção

A operação **Join (Junção)** é usada para **combinar as tuplas relacionadas em duas relações dentro de uma única tupla**. Essa operação é uma das mais importantes em um banco de dados relacional, pois **ela nos permite retornar os relacionamentos entre as relações (tabelas)**.

A forma geral da operação junção entre duas tabelas A e B é a seguinte:

**A x B**

**\<condição da junção>**

Onde: **\<condição de junção>** é uma expressão relacional, normalmente utilizando o operador =, que determina qual coluna da tabela A deve ser comparada com qual coluna da tabela B. Observação: normalmente as colunas envolvidas na condição de junção são a Chave Primária de uma tabela e a Chave Estrangeira na outra.

![Operação Junção](/media/Implementação-de-Banco-de-Dados/aula1/Image7.png)

Considere o banco de dados composto pela tabela Disciplina_Nota. Imagine que nosso modelo de banco de dados definido anteriormente com a tabela DISCIPLINA_NOTA seja redefinido para um modelo mais trabalhado com as tabelas:

DISCIPLINA_NOTA, DISCIPLINA E PESSOA, inserindo uma chave primária (PK) que identifica unicamente um nome, a tabela DISCIPLINA_NOTA com a chave estrangeira (FK) FK_NOME_ALUNO relacionando com a tabela PESSOA e a FK_NOME_DISCIPLINA relacionando com a tabela DISCIPLINA. Temos, então, a seguinte melhoria em nosso banco de dados:

```
π NOME_DISCIPLINA, NOME_ALUNO, NOTA(PESSOA X DISCIPLINA_NOTA X Disciplina)
PK_NOME_PESSOA = FK_NOME DISCIPLINA - PK_DISCIPLINA
```

|     | NOME_ALUNO     | NOME_DISCIPLINA | NOTA |
| --- | -------------- | --------------- | ---- |
| 1   | José Geraldo   | Álgebra         | 8    |
| 2   | Eduardo Tomaz  | Álgebra         | 10   |
| 3   | Cleber Dutra   | Álgebra         | 9    |
| 4   | Hernesto Paula | Álgebra         | 10   |
| 5   | Josué José     | Álgebra         | 10   |

## Operação de Conjuntos

São operações derivadas das operações matemáticas padrão definidas a partir da teoria dos conjuntos. (FONSECA, 2016, p. 18) São elas: **UNION (UNIÃO), INTERSECTION (INTERSEÇÃO) e MINUS (SUBTRAÇÃO)**.

### UNION

UNION é a operação de UNIÃO da teoria de conjuntos. Se temos as relações R(A1, A2, ..., An) e S(B1, B2, ..., Bn) para haver a operação União, os atributos de cada relação devem ser compatíveis entre si, ou seja, devem ter o mesmo grau (n) e os domínios de cada atributo devem ser iguais ao domínio do outro atributo, ou seja, dom(A1) = dom(B1). Significando que cada relação possui o mesmo grau e que cada par de atributos possuem o mesmo domínio. Sendo assim, a operação UNION pode ser aplicada. (FONSECA, 2016, p. 18)

A forma geral da operação junção entre duas tabelas A e B é a seguinte: **A U B**

A Operação de União é comutativa, ou seja, A U B produz o mesmo resultado de B U A.

![Operação de União](/media/Implementação-de-Banco-de-Dados/aula1/Image8.png)

Exemplo:

Tabela PROFESSOR

|     | NOME_PROFESSOR |
| --- | -------------- |
| 1   | Fagundes Teles |
| 2   | Ferreira       |
| 3   | Elmasri        |
| 4   | Navathe        |
| 5   | Cleber Dutra   |

Temos a tabela DISCIPLINA_NOTA e a nova tabela PROFESSOR. Podemos fazer a união dos domínios ‘NOME_PESSOA’ com os nomes dos alunos e os nomes dos professores.

`π NOME_ALUNO(DISCIPLINA_NOTA) U PROFESSOR`

|     | NOME_PESSOA    |
| --- | -------------- |
| 1   | Cleber Dutra   |
| 2   | Eduardo Tomaz  |
| 3   | Elmasri        |
| 4   | Fagundes Teles |
| 5   | Ferreita       |
| 6   | Hernesto Paula |
| 7   | José Geraldo   |
| 8   | Josué José     |
| 9   | Navathe        |

**Atenção: Repare que a operação UNION não trouxe o nome repetido do Professor e aluno Cleber Dutra, essa operação garante tuplas únicas.**

### INTERSECTION

Da mesma forma como foi apresentada a operação UNION, pode-se usar a definição matemática de interseção para definirmos a operação de interseção entre as relações. As observações feitas para a operação UNION, no que diz respeito ao domínio dos atributos e ao grau da relação, também devem ser seguidas para a operação de INTERSECTION. (FONSECA, 2016, p. 20)

** A ∩ B **

Essa operação é comutativa, ou seja, A ∩ B produz o mesmo resultado de B ∩ A.

![Operação de interseção](/media/Implementação-de-Banco-de-Dados/aula1/Image9.png)

Exemplo:

Para intersecção entre nomes de professores e alunos, temos:

`π NOME_ALUNO(DISCIPLINA_NOTA) U PROFESSOR`

|     | NOME_PESSOA  |
| --- | ------------ |
| 1   | Cleber Dutra |

### MINUS

Por fim, apresentamos a operação MINUS (SUBTRAÇÃO), que representa a diferença de conjunto. O resultado dessa operação, tomando-se nossas relações S e R apresentadas anteriormente, é uma relação que inclui todas as tuplas que estão em R, mas não estão em S. As observações feitas para a operação UNION e INTERSECTION, no que diz respeito ao domínio dos atributos e ao grau da relação, também devem ser seguidas para a operação MINUS. (FONSECA, 2016, p. 20)

A forma geral da operação Diferença entre duas tabelas A e B é a seguinte:

**A – B**

Essa operação não é comutativa, ou seja, A - B produz um resultado diferente de B – A.

![Operação de diferença de conjunto](/media/Implementação-de-Banco-de-Dados/aula1/Image10.png)

Para obtermos o nome dos Professores que não são homônimos de alunos (FONSECA, 2016, p. 20), a expressão seria:

`PROFESSOR - π NOME_ALUNO(DISCIPLINA_NOTA)`

Resultando:

|     | NOME_PESSOA    |
| --- | -------------- |
| 1   | Elmasri        |
| 2   | Cleber Dutra   |
| 3   | Fagundes Teles |
| 4   | Navathe        |
