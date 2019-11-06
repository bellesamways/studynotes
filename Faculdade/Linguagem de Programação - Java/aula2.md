## Aula 2 - TIPOS DE DADOS E ESTRUTURAS BÁSICAS DE PROGRAMAÇÃO

Java é **Case Sensitive**. 
* Nomes de **variáveis e métodos** começam com letras **minúsculas**
* Nomes de **classes** iniciam com letras **maiúsculas**
* Nomes **compostos**: utilizar letras **maiúsculas** para as **iniciais** das palavras
* **Constantes** tem letras **maiúsculas**.

**Comentários** em Java:
1. // comentário em uma linha
2. /* comentário em uma ou mais linhas */
3. /** documento comentários */

##### Tipos de dados em Java
Linguagem fortemente **tipada**, ou seja, necessidade que todas as variáveis tenham tipo declarado.

|TIPO   |TAMANHO |
|-------|------- |
|int    | 4 bytes|
|short  |2 bytes |
|byte   |1 byte  |
|long   |8 bytes |
|float  |4 bytes |
|double |8 bytes |
|char   |2 bytes |
|boolean|1 bit   |


##### Declarando e atribuindo valores a variáveis

Inicia a declaração indicando o **tipo da variável e o nome desejado**.
```Java
int x, y; //declarando duas variáveis inteiras
                   x = 6; //atribuindo valores a variáveis
                   y = 1000;
 
                   float f = 3,141516f; //ponto flutuante
                   double w = 3,2310834; //ponto flutuante de dupla precisão

                   char ch = ‘a’; //Caractere
 
                   final int MAX = 9; //Define a constante MAX com o valor de 9
```
##### Operadores aritméticos e relacionais

Obs: O operador **!** é chamado de **not** ou **negado**.


|OPERADORES RELACIONADOS                            | | | 
|:-----------:|:--------:|:----------------------------:|
|**OPERADOR** |**USO**   |**RETORNA VERDADEIRO SE**     |
|    >        |op1>op2   |op1 for maior que op2         |
|    >=       |op1>=op2  |op1 for maior ou igual que op2|
|    <        |op1<op2   |op1 for menor que op2         |
|    <=       |op1<=op2  |op1 for menor ou igual que op2|
|    ==       |op1==op2  |op1 for igual que op2         |
|    !=       |op1!=op2  |op1 for diferente que op2     |
|    &&       |op1&&op2  |Se op1 e op2 forem verdadeiros|
|    \|\|     |op1\|\|op2|Se op1 ou op2 for verdadeiro  |

|OPERADORES ARITMÉTICOS                                        | | | 
|:------:|:-------:|:---------------------------------------------:|
|**OPERADOR**| **USO** |**DESCRIÇÃO**                                  |
|    +       |op1 + op2|retorna a soma de op1 e op2                    |
|    -       |op1 - op2|retorna a subtração de op1 por op2             |
|    *       |op1 * op2|retorna a multiplicação de op1 por op2         |
|    /       |op1 / op2|retorna a divisão de op1 por op2               |
|    %       |op1 % op2|retorna o resto da divisão de op1 por op2      |
|    ++      |  ++op   |incrementa op de 1, depois retorna o valor     |
|    ++      |  op++   |retorna o valor de op, depois o incrementa de 1|
|    --      |  --op   |decrementa op de 1, depois retorna o valor     |
|    --      |  op--   |retorna o valor de op, depois o decrementa de 1|

##### Estruturas básicas de programação

**Blocos**: conjunto de linhas entre um abre e fecha de chaves {}. É permitido criar blocos dentro de blocos.
```Java
{ //início do bloco
...
  /*bloco de comandos*/
...
} //fim do bloco
```
**Escopo das variáveis**: indica em que parte do código ou bloco que podemos utilizar ou enxergar a variável.
* Locais: disponíveis apenas dentro do bloco
* Globais: disponíveis em qualquer bloco do programa
          **escopo != visibilidade**

**Comando condicional**: desvia o fluxo natural do programa de acordo com o resultado de um teste lógico. Quando o programa encontra um if, a expressão booleana é avaliada.
```Java
if (expressão booleana)
    comando1 ou {bloco de comandos1}
else
    comando2 ou {bloco de comandos2}
```

##### Desvios de fluxo: break; e continue;
* **break** termina a execução de um loop sem executar o resto dos comandos e força a saída do laço
* **continue** termina a execução de um laço sem executar o resto dos comandos, voltando para o início do laço para uma nova iteração.

##### Estruturas de repetição ou laço
1. **while**: Enquanto a expressão for verdadeira, o comando será executado. Quando for falsa, o programa segue para o seu caminho normal.
```Java
while(expressão)
    comando ou {bloco de comandos}
```
2.  **do-while**: Faz o comando, enquanto a expressão for verdadeira. Quando for falsa, o programa segue para o seu caminho normal. O programa executa pelo menos uma vez o comando do laço, para depois verificar se vai continua verdadeira para executar de novo.
```Java
do
    comando ou {bloco de comandos}
while(expressão);
```
3. **for**:  executa o laço enquanto a expressão for verdadeira, só que pode ser controlada por um contador. Permite que o usuário inicialize e incremente o contador no controle do laço.
```Java
for(inicialização; expressão; incremento)
    comando ou {bloco de comandos}
```
##### Manipulando com strings
Java é totalmente OO. Todos os valores utilizados são objetos descritos por classes. Um dos mais utilizados é o String (S maiúsculo, porque String é uma classe).
String é uma sequência de caracteres.
```Java
String um = "curso";
String dois = "java";
```
Não podem ser comparados usando operadores relacionais, porque são objetos.

##### Manipulando com vetores
Vetores são estruturas utilizadas para armazenar um conjunto de dados do mesmo tipo (qualquer tipo). Alocação de memória é sempre contínua.
```Java
int[] vetor = new int[100]; //aloca uma área de memória continua com 100 posições para armazenar 100 inteiros

int[] pares = {0, 2, 4, 6, 8, 10};

int[][] matriz = new int[3][4];
```
Vetores podem ter várias dimensões;
Matrizes ou vetores bi-dimensionais são vetores bi-dimensionais.

##### Conversão entre tipos de dados
**Implícita**: sem a necessidade do programador interferir. Valores são **convertidos automaticamente**. Ocorre na conversão de **inteiro** para **real**, de **números** para **strings** ou com o uso de operadores unários.
```Java
double x;
int i = 20;
x = i; // x recebe um valor inteiro
System.out.print(“i= ” + x);

/* O valor de x é convertido para string e concatenado com a outra string para ser apresentada na tela */
```
**Explícita**: o programador controla a conversão informando qual tipo será utilizado, através de um operador unário.
```Java
float eventos = 25.7;
float dias = 7.2;
 
x = (int) (eventos / dias); // O resultado é o inteiro 3, pois 25/7 é 3.57
```