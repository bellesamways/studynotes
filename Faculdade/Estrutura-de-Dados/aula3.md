# Aula 3 - Estruturas heterogêneas

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
