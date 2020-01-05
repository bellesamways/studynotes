# Linguagem de programação - Java

## Aula 1 - INTRODUÇÃO À LINGUAGEM DE PROGRAMAÇÃO JAVA

É uma linguagem que é compilada para um “bytecode”, que é **interpretada** por uma máquina virtual – JVM.


**Portabilidade**: O Java pode ser executado em qualquer plataforma ou equipamento que possua um interpretador Java e que tenha sido especialmente compilado para o sistema a ser utilizado.


**Orientada a Objetos**: Contém a sintaxe similar a linguagem C/C++, mas é baseada no modelo Simula67.


**Segurança**: Pode ser executado via rede, com restrições de execução, além de proteger o sistema do cliente contra possíveis ataques não intencionais.


**Orientação a Objetos**: totalmente OO - permitindo herança e reutilização de código de forma dinâmica e estática.


**Dinamismo**: permite ser aumentado durante a execução.


**Facilidade**: Derivada do C/C++ - Bem familiar. O ambiente retira do programador a responsabilidade de gerenciar a memória e os ponteiros.


<https://www.digitalocean.com/community/tutorials/como-instalar-o-java-no-ubuntu-com-apt-get-pt>


**Funcionamento de um programa Java**  
![Funcionamento de um programa Java](/media/Linguagem_de_Programacao-Java/Aula1/funcionamento-programa-java.png)



1. **Editor**: escrita ou desenvolvimento do programa.
2. **Compilador**: converte o código em bytecodes, que representam as tarefas a serem realizadas durante a execução.
3. **Carregador**: transfere os arquivos .class contendo os bytecodes do programa para a memória principal.
4. **Verificador**: examina os códigos para assegurar que eles sejam válidos e não violam restrições de segurança do Java.
5. **Interpretador**: a JVM executa o programa interpretando o bytecodes gerado na fase da compilação.

**Tipos de programas de Java**
![Tipos de programas de Java](/media/Linguagem_de_Programacao-Java/Aula1/Tipos_de_programas_de_Java.png)

**Como executar um programa Java?**

1. escreva o programa e salve com a extensão .java
2. para compilar, dentro da pasta onde foi salvo o código:
> javac PrimeiroPrograma.java
3. o arquivo .class foi gerado
4. para executar, basta chamar a máquina virtual:

> java PrimeiroPrograma

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

## Aula 3 - INTRODUÇÃO AS INTERFACES GRÁFICAS

##### Introdução as IDEs
![Introdução as IDEs](/media/Linguagem_de_Programacao-Java/Aula3/IntroducaoIDEs.png)

##### Introdução a concepção de interfaces gráficas
A interface gráfica com o usuário (GUI) fornece a um programa um conjunto consistente de componentes intuitivos, familiarizando o usuário com as diversas funções e diminuindo o tempo de aprendizado da nova ferramenta. As GUIs são construídas a partir de componentes GUI, que são objetos com o qual o usuário interage através dos dispositivos de entrada, ou seja, o mouse, o teclado, a voz, etc.

##### Criação de Interfaces Gráficas

As classes necessárias para criação de componentes gráficos, bem como para fornecer-lhes funcionalidade, estão agrupadas em dois grandes pacotes: **java.awt (pacote de núcleo) e javax.swing (pacote de extensão)**. Os dois pacotes definem componentes com peculiaridades distintas e que serão discutidas a seguir.

**Componentes swing**: maioria dos componentes Swing é escrita, manipulada e exibida completamente em Java, estes são conhecidos como componentes Java puros. Maior nível de portabilidade e flexibilidade. Os nomes de tais componentes recebem um “J”, como, por exemplo: JLabel, JButton, JFrame, JPanel, etc.

**Componentes básicos**: mostra a maioria das classes que compõem o Java Swing e mostra também a relação entre as classes AWT (claro) e as classes Swing (escuro).
![Fluxograma de relação entre as classes](/media/Linguagem_de_Programacao-Java/Aula3/componentesBasicos.png)

##### Painéis

Áreas que comportam outros componentes, inclusive outros painéis. São criados com a classe JPanel, que é derivada da classe Container. A classe JPanel não tem painel de conteúdo como JFrames, assim, os elementos devem ser diretamente adicioandos ao objeto painel.
```Java
import javax.swing.*;

public class Frm01 {
    public void criaTela(){
        JFrame f = new JFrame();
        f.setSize(290, 100);
        f.setTitle("Cadastro");
        f.setLocation(10, 10);
        f.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        f.setVisible(true);
    }
}
```
```Java
public class TestaFrm01 {
    public static void main(String []args){
        Frm01 tela = new Frm01();
        tela.criaTela();
    }
}
```
O método setDefaultCloseOperation()também pode ser executado com outras constantes como argumento

**DISPOSE_ON_CLOSE** - Destróia a janela
**HIDE_ON_CLOSE** - Apenas fecha a janela
**DO_NOTHING_ON_CLOSE** - Desabilita opção
**EXIT_ON_CLOSE** - Encerra a aplicação

## Aula 4 - PRINCÍPIOS DA ORIENTAÇÃO A OBJETOS

#### Introdução classes e objetos

As classes definem a estrutura e o comportamento de um tipo de objeto.
**Classes**: Um protótipo que define os atributos e os métodos comuns a todos os objetos de um determinado tipo e da própria classe, com a finalidade de servir de molde para a criação de objetos.
**Objetos**: São a representação de uma entidade do mundo real, que tem identificador único, propriedades embutidas e a habilidade de interagir com outros objetos e consigo mesmo.  Um objeto é uma instância de uma classe. A classe descreve todas as características e funcionalidades de um objeto. Modelamos os objetos através das classes.

##### Abstração
* Extrair tudo que for essencial e mais nada para o escopo do sistema;
* É o processo de filtragem de detalhes sem importância do objeto real, para que apenas as características apropriadas que o descrevam tenham relevância para o sistema permaneçam;
* Conceito aplicado a criação de software baseado em objetos, partindo do princípio que devemos considerar a essência de cada objeto e não pensar em todos os detalhes de implementação.

##### Encapsulamento
* Mecanismo utilizado em OO para obter segurança, modularidade e autonomia dos objetos;
* Implementamos através da definição de visibilidade privada dos atributos;
* Sempre definir os atributos de uma classe como privados;
* Esse mecanismo protege o acesso direto aos dados do objeto;
* Permite acesso através dos métodos públicos;
É a disponibilização de uma interface pública, com granularidade controlada, para manipular os estados e executar as operações de um objeto (* acesso permitido).

|Modificadores|Mesma classe|Mesmo pacote|Subclasses|Universo|
|:-:          |:-:         |:-:         |:-:       |:-:     |
|private      |*           |            |          |        |
|\<sem modif> |*          |*           |          |        |
|protected    |*           |*           |*         |        |
|public       |*           |*           |*         |*       |
Os atributos e métodos de um objeto podem ser escondidos de outros objetos por uma interface pública de métodos, de modo a impedir acesso indevidos.

#### Definindo uma classe em java
A primeira linha é um comando que inicia a declaração da classe.
Após a palavra-chave **class**, segue-se o nome da classe, que deve ser um identificador válido para a linguagem.
O modificador **modif** é opcional; se presente, pode ser uma combinação de **public** e **abstract** ou final.
A definição da classe, propriamente dita, está entre as chaves **{** e **}** que delimitam blocos na linguagem Java.
```Java
[modif] class NomeDaClasse {
   // corpo da classe...
}
```
Corpo da classe segue, geralmente, a ordem abaixo:
1. **Variáveis de classe** (definidas como static), ordenadas segundo sua visibilidade: iniciando pelas **public**, depois **protected**, depois com **visibilidades padrão** (sem modificador) e depois as **private**.
2. **Atributos** (variáveis de instância) dos objetos dessa classe, seguindo a mesma ordenação segundo a visibilidade definida para as variáveis de classe.
3. Os **construtores** de objetos dessa classe.
4. Os **métodos da classe**, geralmente agrupados por funcionalidade.

#### Criando objetos em java
Construtor é responsável por alocar memória para o objeto. A criação de um objeto se dá através da aplicação do operador new.
```Java
ClasseNome objeto = new ClasseNome();
```
O método a direita do operador new é o construtor da classe ClasseNome.

**Atributos**: representam as características do objeto. Devem ser privados.
```Java
[modificador] tipo nome [ = default];
```
* modificador é opcional, especificando a visibilidade diferente da padrão;
* tipo deve ser um dos tipos primitivos do java ou o nome de uma classe;
* nome deve ser um identificador válido do java;
* valor default é opcional; se presente, especifica um valor inicial para a variável.

**Métodos**: representam as funcionalidades que os objetos podem desempenhar. Além dos atributos de objetos, métodos podem definir e manipular variáveis locais; também podem receber parâmetros por valor através da lista de argumentos.
```Java
[modificador] tipo nome(argumentos)
{
    //corpo do método
}
```
* modificador (opcional) é uma combinação de: public, protected ou private; abstract ou final; e static;
* tipo é um indicador do valor de retorno, sendo void, se o método não tiver um valor de retorno;
* nome do método deve ser um indicador válido no java;
* os argumentos são representados por uma lista de parâmetros separados por vírgulas onde, para cada parâmetro, é indicado primeiro o tipo e depois (separado por espaço) o nome.

*Boa prática -> manter a funcionalidade de um método simples, desempenhando uma única tarefa*.

## Aula 5 - HERANÇA
**Herança** significa a capacidade de incorporar as características e as funcionalidades de uma classe.
Pode especializar métodos da super classe e especificar novas operações e dados, para refinar, especializar, substituir ou estender a funcionalidade da classe progenitora.
* uma classe define um conjunto de dados - Atributos - e um conjunto de métodos.
* todos os objetos de uma classe mantêm o mesmo conjunto de atributos e métodos.
* tendo definido uma classe base é possível criar classes derivadas que:
    * herdam os atributos e métodos da classe base;
    * definem novos atributos e métodos;
    * podem redefinir os métodos herdados.
#### Terminologias
* **Estender**: criar uma nova classe que herda todo o conteúdo da classe existente
* **Superclasse**: uma classe progenitora ou base
* **Subclasse**: uma classe filha que herda ou estende uma superclasse
![Fluxograma da hierarquia de classe](/media/Linguagem_de_Programacao-Java/Aula5/FluxogramaHeranca.png)


**Classe abstrata**: define atributos e métodos. Um método pode ser definido com o modificador "abstract".
* a classe abstrata não implementa os métodos abstratos
* as classes derivadas devem implementar os métodos abstratos
* Os métodos declarados na classe abstrata serão implementados em suas subclasses, através de polimorfismo.
*Exemplo*: uma funcionalidade existente em todas as subclasses quer ser apresentada na superclasse. Este método é definido na superclasse como Abstract. Nas subclasses, estes métodos serão implementados, cada um com a sua peculiaridade.

#### Métodos e classes abstratas
1. subclasses podem redefinir (sobrepor) um método de sua superclasse
2. usar o modificador abstract para indicar que um método de uma classe deve necessariamente ser redefinido em uma das suas subclasses
3. uma classe com um ou mais métodos abstratos, deve ser declarada explicitamente como abstrata. a classe pode ter construtores e métodos concretos (não abstratos)
4. uma classe declarada como abstract, não podem ser criados objetos desta classe.
5. subclasse derivada de uma superclasse que contém método abstrato, e se o método abstrato não for redefinido na subclasse, esse método permanece abstract na subclasse. subclasse deverá ser declarada explicitamente como abstract.
6. declarar um método como abstrato é uma forma de obrigar o programador a redefinir esse método em todas as subclasses para as quais se deseja criar objetos.
7. como um método abstrato deve ser redefinido nas subclasses, na superclasse ele não precisa ter implementação alguma.
*exemplo*:
```Java
// Class abstrata Empregado
public abstract class Empregado{ //Como a classe contém um método abstrado, ela deve ser declarada como abstrata.

    private String nome;
    private String familia;

    public Empregado(String n, String f){
        nome = n;
        familia = f;
    }

    public String getNome(){
        return nome;
    }
    public String getFamilia() {
        return familia;
    }

    public String toString(){
        return nome + ' ' + familia;
    }

    public abstract double ganha(); //Método abstrato. Deve ser implementado na subclasse


}
```
![Print de tela do código de uma classe abstrata](/media/Linguagem_de_Programacao-Java/Aula5/ExemploClasseAbstrata.png)

#### Polimorfismo
Capacidade que os métodos de mesmo nome têm de efetuarem tarefas diferentes.
O mesmo método com várias formas.
Acontece de duas maneiras em java: quando os métodos são definidos em função da classe que os utiliza (sobreposição), ou dos diferentes conjuntos de argumentos definidos para cada método (sobrecarga).

[![Icone de um arquivo PDF com o nome Polimorfismo.pdf](/media/Linguagem_de_Programacao-Java/Aula5/downloadPDF.png)](https://www.evernote.com/shard/s248/sh/509df3c5-42b5-47d9-9bbe-7ad99af234c5/6e0a676c82466316d5081467b38ee751/res/485fa420-41cf-4da3-a3f4-26483bce2951/polimorfismo.pdf)
