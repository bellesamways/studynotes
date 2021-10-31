# Estrutura de Dados

## Aula 1 - Apresentando as Estruturas de Dados

Árvore binária: Duas subárvores. A binária tem no máximo grau 2 \
Grau de uma árvore é definido pelo número de subárvores de um nó. \
Grau 0: terminais ou folhas

Tudo que requer hierarquia, pode usar árvore.

**Grafo:** estrutura de dados não linear; conjunto de nós (vértices) e suas conexões (arcos) entre eles. Não existe limitações para os vértices.

**Fila:** segue a regra **FIFO** - first in, first out. **Inserção** de elementos na fila acontece **sempre ao final**. **Remoção** de um elemento sempre acontece no **início**.

Métodos de **pesquisa**: sequencial e binária

* **sequencial**: listas não ordenadas
* **binária**: listas ordenadas

**Lista**: mais simples para **agrupar** dados, formando um conjunto de elementos do **mesmo tipo** e preservando a relação de ordem linear entre os elementos.

* **nós** ou nodos: elementos de uma lista
* operações podem ser feitas com as listas
formas de inserção definem o tipo de lista: **pilha, fila**.
* Listas lineares: sequencial e encadeada.
  * **sequencial**: dados são armazenados na memória principal de forma **contígua** (matrizes)
  * **encadeada**: dados armazenados na memória em posições não adjacentes (**não contíguas**)

**Ordenação**: classificação dos dados.

**Pilha**: **inserção** de elementos sempre acontece no **topo** da pilha e a **remoção** também.

* método de acesso: **LIFO** (last in, first out)

**Struct**: conjunto de elementos geralmente agrupados sob uma **lógica** e associados por um **nome**.

* cada elemento da estrutura é chamado de membro ou campo.

**Função**: bloco contendo cabeçalho, início e fim. Serve para executar tarefas menores.

**Lista encadeada:** se caracteriza por não ter seus nós alocados de forma contígua. **Cada nó da lista leva o endereço do próximo nó para não perder o encadeamento.**

* Ponteiro para o primeiro nó
* do primeiro ao último segue o encadeamento através dos ponteiros presentes em cada nó
* último elemento aponta para o NULL

**Tipo de dados abstratos (TDA)**: conjunto de valores e uma coleção de operações que atuam sobre esses valores.

Dimensionando matrizes:

* **tipo nomeMatriz[tamanho];**
* **tipo nomeMatriz[tamLinha][tamColuna];**

tipo: int, float, double, char, long long int, etc

localizar um elemento da matriz: endereço-base + deslocamento * tamanho do tipo

0 significa que não tem deslocamento em relação ao endereço-base.

\0 finaliza o vetor de char

## Aula 2 - Funções

Única função obrigatória é a main.

**Modularização**: melhorar o entendimento do programa, encontrar erros com mais facilidade, simplificar a manutenção, reutilização de código, etc. São "pequenos programas" conhecidos como funções.

### Função

Uma função é um conjunto de comandos limitado por um par de chaves e precedido por um cabeçalho.

**Definição de função:**

```
<tipo de função> nome da função (declarações dos parâmetros) {
    <declaração das variáveis locais>
        comandos que formam o corpo da função
    return <valor>; // return; ou nada
}
```

* tipo de função: tipo de retorno da função
* nome da função: deve sugerir a finalidade da função
* variáveis locais: variáveis que vão ser utilizadas dentro da função (tipo e nome)
* corpo da função: conjunto de comandos
* return \<valor>: só existe esse comando se a função retornar um valor para a função chamadora
* return; ou nada: para função do tipo *void*

**Protótipo de uma função:**

```
<tipo de função> nome_da_função (declarações dos parâmetros);
```

Podem ser colocadas **antes ou depois** da *main*.

* **Antes**: serão conhecidas pelo compilador antes de serem chamadas, evitando problemas. Isso diminui a legibilidade do programa dependendo do tamanho dele.
* **Depois**: aumenta a legibilidade, mas cria-se um problema: função é chamada antes da identificação dela pelo compilador. Resolve-se esse problema com os **protótipos** das funções **antes** da *main* e as definições depois da main.

**Chamada da função e o seu retorno**
Quando uma função é chamada, o fluxo de controle é direcionado a executar os comandos da função e depois ele volta para onde foi ativado (se for void) ou ao ponto de onde ela foi chamada, para funções com retorno.

Não podemos desconsiderar o tipo de retorno e os parâmetros caso existam.

**Tipos de funções:**

1. **Funções sem parâmetros**
    No C++ não é obrigatório o uso de parâmetros em todas as funções. Uma função que não retorna nada é do tipo void, e é hierarquicamente considerado abaixo da main.
    Ela é chamada pelo nome, sem necessitar de comando que a anteceda.

    ```
    nomeDaFuncao();
    ```

2. **Funções com parâmetros**

   1. **Passagem por valor**: uma cópia do valor, ou valores, é passada para os parâmetros formais da função chamada através dos parâmetros reais da função chamadora. Podendo ser representados por variáveis ou constantes.
   2. **Passagem por referência**: o endereço da variável é passado para a função chamada e dessa forma o valor poderá ser alterado. Em C era passado usando ponteiro, em C++ usa-se a **referência** (&).

        ```
        void troca (float &a, float &b);
        ```

        1. *Passagem por referência por ponteiros (passagem por nome ou passagem por endereço):* **&** é o endereço e **\*** é o conteúdo do endereço apontado
        2. *Passagem por referência*: referência não é ponteiro, mas ambos manipulam endereço.

| Função                                           | Significado                                                                                                                                                      |
| ------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **void linha(char c, int n);**                   | Função que recebe dois argumentos por passagem de valor. Um do tipo char e outro do tipo int, mas não retorna nada para função chamadora.                        |
| **int descobreIdade(int anoAtual, int anoNas)**; | Função que recebe dois argumentos por passagem de valor. Os dois do tipo inteiro e retorna, para a função chamadora, um valor inteiro.                           |
| **float areaRetangulo(float, float);**           | Função que recebe dois argumentos reais e retorna, para a função chamada, um valor real.                                                                         |
| **void troca(float&, float&)**                   | Função que recebe dois argumentos que são endereços que armazenam números reais, por passagem por referência. A função não retorna nada para a função chamadora. |

Uma função que retorna valor deverá ser chamada através de um comando, não importando se ela tem, ou não, parâmetros. Uma função só poderá retornar um valor!

**Return**: Uma função que retorna valor terá, obrigatoriamente esse comando no corpo da função. Isso não quer dizer que não poderá ter mais de um comando return no corpo da função. Quando existir múltiplas respostas, poderemos ter vários tipos de retorno. Pode estar presente uma variável, uma constante, uma expressão.

**Variáveis locais**: variáveis só visualizáveis dentro das funções onde foram declaradas. \
**Variáveis globais:** variáveis declaradas fora do escopo de todas as funções. Pode ser manipulada por qualquer função.

**Padrão da main**: *int main ();* \
Return da main poderia ser dispensável, pois ele já retorna automaticamente para o SO. \
Bom hábito: *return 0;* ou *return EXIT_SUCESS;*

**Passando uma estrutura de dados homogênea para uma função**

## Aula 3 - Estruturas heterogêneas

**Struct**
Conjunto de elementos, geralmente, agrupados sob uma lógica e associados por um nome. Esses elementos podem ser variáveis simples, matrizes, outras estruturas e até funções. Por essa definição, podemos concluir que uma estrutura pode ser formada por elementos de tipos diferentes. Cada elemento da estrutura é chamado de membro ou campo.

**Definição**:

```
struct <identificador> {
    <tipo do membro> <identificador>;
    <tipo do membro> <identificador>;
};
```

* **Struct**: palavra que inicia a definição da estrutura.
* **\<identificador>**: nome da estrutura
* **\<tipo do membro>**: pode ser int, float, double, char.
* **\<identificador>**: nome do membro (campo) que segue a mesma regra das variáveis

com o nome da struct é possível declarar variáveis, inclusive arrays e nem precisa usar a palavra struct antes.
pode ser definida dentro de uma função sendo local ou antes de todas as funções sendo global.

dois métodos de declarar variáveis:

* declaração é feita depois da definição. se for global, acontece em cada função.

    ```
    struct nomeDaEstrutura {
    ...
    };
    nomeDaEstrutura nomeDaVariavel;

    struct cadastro {
    ...
    };
    cadastro aluno;
    ```

* declaração é feita junta com a definição.

    ```
    struct nomeDaEstrutura {
    ...
    } nomeDaVariavel;

    struct cadastro {
    ...
    } aluno;
    ```

Um membro da estrutura pode ser acessado usando o operador membro da estruturas(.), chamado operador ponto, colocado entre o nome da variável estrutura e o nome do membro.\
**nomeDaVariavelEstrutura.nomeDoMembro**

```
struct coordenadas {
    int x, y;
};
.
int main(){
    coordenadas a, b;
}
```

![estrutura_coordenadas](/media/estrutura_dados/estrutura_coordenadas.png)

Nome da variável estrutura: a\
Nome do primeiro membro: x\
Nome do segundo membro: y\
Acessando o membro x da variável estrutura a: a. x\
Acessando o membro y da variável estrutura a: a. y\
Nome da variável estrutura: b\
Nome do primeiro membro: x\
Nome do segundo membro: y\
Acessando o membro x da variável estrutura b: b. x\
Acessando o membro y da variável estrutura b: b. y

**Atribuindo valores aos membros:**\
1º método: Usando comando de atribuição na hora da declaração das variáveis.
![atribuindo_valores](/media/estrutura_dados/atribuindo_valores.png)

2º método: Atribuição na hora da definição/declaração das variáveis. Atribuição de uma estrutura a outra estrutura um ponto a favor das estruturas em relação aos vetores.

```
struct prod {
char nomeProd[21];
float valor;
} produto1={“martelo”, 35.90}, produto2={“furadeira”, 256.75};
```

Acessando cada membro de cada variável estrutura do tipo prod\
Nome da variável estrutura: produto1\
Nome do primeiro membro: nomeProd\
Nome do segundo  membro: valor\
Acessando o membro nomeProd da variável estrutura produto1: produto1. nomeProd\
Acessando o membro valor da variável estrutura produto1: produto1. valor\
Nome da variável estrutura: produto2\
Nome do primeiro membro: nomeProd\
Nome do segundo  membro: valor\
Acessando o membro nomeProd da variável estrutura produto2: produto2. nomeProd\
Acessando o membro valor da variável estrutura produto2: produto2. valor

3º método: Atribuição através da leitura via teclado.

```
struct  prod
{
  char nomeProd[21];
  float valor;
} produto1, produto2;
```

**Construindo um array de estruturas**

```
struct <identificador>
{
...
};
<identificador> nomeDaVariavel;

struct alCad
{
...
};
alCad alunos[15];

struct <identificador>
{
...
} nomeDaVariavel;

struct alCad
{
...
} alCad alunos[15];
```

Como acessar um elemento do array de estrutura

```
struct prodCad
{
    int codigo;
    float precoCompra, precoVenda;
};
prodCad produtos[1000];
```

produtos[1].codigo\
produtos[1].precoCompra\
produtos[1].precoVenda

**Estruturas aninhadas**\
Usar esta estrutura com membro de outra estrutura que iremos definir/declarar.

```
struct data {
  int dia, mes, ano;
};

struct pagto {
  int codigo;
  float valor;
  data venc;
} promissorias[2];
```
![estrutura_aninhadas](/media/estrutura_dados/estruturas_aninhadas.png)

**nomeDoArrayl[deslocamento no array].nomeDaEstruturaAninhada.membro**

**Passagem por valor**: na passagem por valor, passamos uma cópia do conteúdo logo, o valor original não se altera.\
**Passagem por referência**: SAADE, Joel(2003, p.112): “Pode-se dizer que a passagem por referência é uma forma disfarçada de ponteiro”.

**Estrutura como parâmetro de uma função:** função que recebe uma estrutura para ser manipulada dentro da função.\
**Estrutura como valor de retorno de função:** função do tipo estrutura logo, terá como retorno uma estrutura.\
**Funções como membros de estrutura:** estrutura cujos dois membros são funções. Uma com retorno e outra sem retorno.
