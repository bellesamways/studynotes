# Desenvolvimento de Software - Java

## Aula 1 - Características gerais e sintaxe básica

A linguagem Java teve origem na década de 1990 e de lá para cá foi se tornando cada vez mais popular, sendo amplamente utilizada em sistemas críticos.  

Como toda linguagem, essa também apresenta peculiaridades, como o uso de padrão de escrita CamelCase, paradigma orientado a objetos e processamento paralelo nativo.  

### Características Gerais do JAVA  

Java é uma linguagem de programação **orientada a objetos** desenvolvida na década de 1990.

Desde a sua concepção, o Java trouxe alguns princípios básicos que norteiam a sua própria evolução, destacando-se o cuidado em executar em **múltiplas plataformas** e garantir elementos de **conectividade**.

Em linguagens que geram código nativo para o Sistema Operacional, como C++ e Pascal, o código fonte deve ser compilado, gerando arquivos objeto, e estes arquivos devem ser combinados por **linkedição** para criar um executável.

Outras linguagens, classificadas como **interpretadas**, não passam por este processo de compilação, sendo executadas linha a linha por um interpretador, a exemplo da programação shell para Unix e do JavaScript nos navegadores.

A linguagem Java utiliza um artifício que permite a execução de seus programas em qualquer plataforma: uso de **máquina virtual**. Com esta abordagem, os programas em Java são compilados, não podendo ser classificados como interpretados, mas sem gerar executáveis para o Sistema Operacional, logo não sendo linkeditados.

Cada sistema operacional tem a sua versão da máquina virtual Java, normalmente necessitando da instalação do Java Runtime Environment (JRE), disponível gratuitamente no site da Oracle, e os programas feitos em Java irão executar nestas máquinas virtuais, sem se preocupar com o sistema hospedeiro.

Nós também temos uma grande facilidade para efetuar a conexão com outros sistemas em rede com o uso de Java, por que traz uma extensa biblioteca de componentes para a criação de **Sockets**, conexão **HTTP e FTP**, criação de clientes e servidores de e‑mail, entre diversos outros, garantindo a premissa básica de conectividade da linguagem.

Outra característica inovadora no lançamento do Java, e rapidamente adotada por outras linguagens, foi a inclusão de um coletor de lixo (**garbage collector**), o qual efetua a desalocação de memória de forma automática.

Em termos de programação, devemos estar atentos ao fato de que o Java é **fortemente tipado**, ou seja, o tipo da variável é definido na sua declaração, além de ser **case sensitive**, diferenciando letras minúsculas e maiúsculas, e adotar o padrão de nomenclatura **CamelCase**.

### Ambiente de desenvolvimento

Podemos desenvolver programas em Java com o simples uso de um editor de texto e os programas de compilação e execução oferecidos a partir do Java Development Kit (JDK), o qual pode ser obtido gratuitamente no site da Oracle (www.oracle.com).

Exemplo:

![Exemplo de ambiente de desenvolvimento usando bloco de notas](/media/desenvolvimento_de_software_java/aula1/img01_exemplo.png)

Poderíamos criar um pequeno programa de exemplo no bloco de notas.

Você deve salvar este programa com o nome “Exemplo001.java”, depois ir até o prompt e digitar dois comandos, no mesmo diretório onde o arquivo foi salvo, lembrando que o diretório bin do JDK deve estar no PATH.

``` 
javac Exemplo001.java 
java Exemplo001 
```

Nós utilizamos o primeiro comando para compilar o arquivo de código-fonte “.java” e gerar o arquivo-objeto “.class”, enquanto o segundo comando executa este “.class”, efetuando a chamada ao método main, ponto inicial de execução, e imprimindo a mensagem “Alô Mundo”.

Note que as linhas de código em Java são terminadas com o uso de ponto e vírgula, e o esquecimento deste terminador é uma fonte de erros muito comum para os programadores da linguagem.

Várias IDEs estão disponíveis para Java, algumas gratuitas e outras pagas, mas todas elas precisam da instalação do JDK antes que as mesmas sejam instaladas.

Alguns exemplos de IDEs para Java:

- Eclipse
- NetBeans
- IntelliJ IDEA
- BlueJ
- JCreator

Vamos adotar o NetBeans.

![Netbeans](/media/desenvolvimento_de_software_java/aula1/img02_netbeans.png)

1. **Menu Principal** – Controle global das diversas opções da IDE, ativação e desativação de painéis internos, instalação de plataformas, entre outras funcionalidades. Este é o controle de mais alto nível do NetBeans.

2. **Toolbar** – Acesso rápido, de forma gráfica, às opções mais utilizadas, como criar arquivos e projetos, salvar arquivos e executar o projeto.

3. **Painel de Controle** – Aceita várias configurações, mas no padrão normal apresenta uma divisão com a visão lógica dos projetos (Projetos), uma com a visão física (Arquivos) e outra com acesso ao banco de dados e aos servidores (Serviços).

4. **Navegador** – Permite o acompanhamento das características de qualquer elemento selecionado da IDE, como classes em meio ao código.

5. **Editor de Código** – Voltado para a edição do código, com diversos auxílios visuais e ferramentais de complementação.

6. **Saída** – Simula o prompt do sistema, permitindo observar a saída da execução, bem como efetuar entrada de dados via teclado.

O NetBeans pode ser obtido em netbeans.org/downloads, devendo ser escolhida a versão completa, pois já traz todas as plataformas de programação configuradas, além dos servidores GlassFish e Tomcat embutidos.

Após instalar o JDK e o NetBeans (verão completa), podemos executar esta IDE e criar o nosso primeiro programa já no ambiente de desenvolvimento completo.

Para criar um novo projeto devemos seguir os passos:

1. No menu principal do NetBeans escolha a opção Arquivo..Novo Projeto, ou `Ctrl+Shift+N`;
![Criar novo projeto - passo 01](/media/desenvolvimento_de_software_java/aula1/img03a_novo_projeto.png)

2. Na janela que se abrirá, escolha o tipo de projeto como Java..Aplicação Java e clique em Próximo;
![Criar novo projeto - passo 02](/media/desenvolvimento_de_software_java/aula1/img03b_novo_projeto.png)

3. Dê um nome para o projeto (Exemplo001) e diretório para armazenar seus arquivos (C:\MeusTestes) e clique em Finalizar.
![Criar novo projeto - passo 03](/media/desenvolvimento_de_software_java/aula1/img03c_novo_projeto.png)

Ao final destes passos, o projeto estará criado e sua estrutura poderá ser observada no Painel de Controle, bem como o código padrão estará presente no Editor de Código. Diversos comentários são adicionados a esse código, aparecendo normalmente na coloração cinza, e eles podem ser mantidos ou removidos sem qualquer interferência sobre a funcionalidade do projeto.

O que precisamos fazer agora é complementar esse código com a linha que falta no main, conforme pode ser observado a seguir.

```java

package exemplo001; 

public class Exemplo001 { 

  public static void main(String[] args) { 
    System.out.println("APENAS UM EXEMPLO"); 
  } 

} 

```

Após acrescentar a linha com o comando de impressão, basta executar o projeto com uso de `F6`, menu Executar..Executar Projeto, ou botão “play” da ToolBar.

O projeto será compilado e executado, e a frase “APENAS UM EXEMPLO” poderá ser observada na divisão de Saída do NetBeans.
![Criar novo projeto - fim](/media/desenvolvimento_de_software_java/aula1/img03d_novo_projeto.png)

### Tipos Nativos e Operadores

Quase tudo em Java é baseado em objetos. Basicamente, apenas os tipos nativos são considerados de forma diferente, mas para cada tipo nativo existe uma ou mais classes **Wrapper**.

Sempre devemos lembrar que um tipo nativo corresponde a uma simples posição de memória, enquanto uma classe Wrapper, além de comportar o valor correspondente ao tipo, oferece métodos específicos para tratamento do mesmo.

Podemos observar, no quadro seguinte, os principais tipos nativos do Java.


| Tipo Nativo | Wrapper   | Descrição do Tipo               |
| ----------- | --------- | ------------------------------- |
| byte        | Byte      | Inteiro de 1 byte               |
| short       | Short     | Inteiro de 2 bytes              |
| int         | Integer   | Inteiro de 4 bytes              |
| long        | Long      | Inteiro de 8 bytes              |
| char        | Character | Caracteres ASCII                |
| float       | Float     | Real de 4 bytes                 |
| double      | Double    | Real de 8 bytes                 |
| boolean     | Boolean   | Valores booleanos true ou false |

As variáveis aceitam diferentes formas de declaração e inicialização, como podemos observar a seguir:

```java

int a, b, c; 
boolean x = true; // Variável declarada e inicializada 
char letra = 'W'; 
String frase = "Teste"; 
double f = 2.5, g = 3.7; 
```

Para programas simples não há necessidade do uso extensivo de classes Wrapper, mas é aconselhável utilizá-las na criação de sistemas que usem tecnologias de Web Service, ou frameworks de persistência, entre outros.

Nas versões antigas do Java as classes Wrapper deveriam ser alocadas com uso de **new**, mas atualmente podem ser associadas direto ao valor armazenado pelas classes. Exceção feita à classe String, que sempre permitiu a inicialização direta.

Lembre-se sempre de comentar seu código para que você e outros programadores possam revisá-lo com mais facilidade em adaptações posteriores.

O Java aceita dois tipos de comentários:

Comentário de **linha**, com uso de `//`.

Comentário **longo**, iniciado com `/*` e finalizado com `*/`.

Tendo definidas as nossas variáveis, podemos efetuar as mais diversas operações sobre elas com o uso de operadores. Os principais operadores são divididos em aritméticos, relacionais e lógicos.

Os operadores aritméticos utilizados no Java são:

| Operador | Operação                      |
| -------- | ----------------------------- |
| +        | Soma (concatenção para texto) |
| -        | Subtração                     |
| *        | Multiplicação                 |
| /        | Divisão                       |
| %        | Resto da divisão inteira      |
| ++       | Incremento de 1               |
| --       | Decremento de 1               |
| &        | And (E) binário               |
| \|\|     | Or (ou) binário               |
| ˆ        | Xor (ou-exclusivo) binário    |

Exemplo:

```java
package exemplo002; 
 
public class Exemplo002 { 
  public static void main(String[] args) { 
    int a = 5, b = 32, c = 7; 
    System.out.printf("A: %d\t B: %d\t C:%d\n",a,b,c); 
    b = b - c; 
    b /= a; 
    System.out.printf("A: %d\t B: %d\t C:%d\n",a,b,c); 
    b = a ^ c; 
    System.out.printf("A: %d\t B: %d\t C:%d\n",a,b,c); 
    b++; 
    System.out.printf("A: %d\t B: %d\t C:%d\n",a,b,c); 
  } 
} 

```

Antes de descrever a saída e as operações utilizadas, vamos observar o comando **printf**.

Este comando permite uma saída formatada, onde cada **%d** receberá um valor inteiro, **\n** é utilizado para pular de linha e **\t** para representar uma tabulação. No caso, como existem três ocorrências de **%d** na expressão, ela receberá as três variáveis inteiras logo após a vírgula, preenchendo as lacunas **%d** com os valores dessas variáveis na ordem oferecida.

Observe agora a saída do programa.

![Saída do programa](/media/desenvolvimento_de_software_java/aula1/img04_saida_do_programa.png)


Na primeira impressão temos os valores originais, declarados na inicialização, mas em seguida são feitas duas operações, onde **b** recebe seu valor decrementado do valor de **c**, sendo dividido por **a** em seguida.

A expressão **b /= a** é equivalente a **b = b / a**, e isto pode ser feito com qualquer operador quando a variável sofre uma operação sobre ela mesma. Igualmente, poderíamos ter escrito **b - = c** na primeira operação.

Fazendo as contas teremos os valores da segunda linha que foi impressa.

Em seguida temos uma operação binária entre **a** e **c**, com o valor armazenado em **b**. É uma operação de ou-exclusivo, onde o valor será 1 apenas se os dois bits comparados tiverem valores distintos.

![Tabela A ou-exclusivo C](/media/desenvolvimento_de_software_java/aula1/img05_exemplo.png)

Com esta operação justificamos na terceira impressão o valor de 2 para **b**, o qual é acrescido de 1 com o operador **++**, apresentando o valor 3 na quarta impressão.

Os operadores relacionais permitem a comparação entre valores, tendo como resultado um valor verdadeiro (**true**) ou falso (**false**), o que pode ser armazenado em uma variável booleana.

Podemos observá-los no quadro seguinte.

| Operador | Operação                                    |
| -------- | ------------------------------------------- |
| ==       | Compara igualdade entre termos              |
| !=       | Compara a diferença entre os termos         |
| >        | Compara se o primeiro é maior que o segundo |
| <        | Compara se o primeiro é menor que o segundo |
| >=       | Compara se o valor é maior ou igual         |
| <=       | Compara se o valor é menor ou igual         |

Estes operadores serão de grande importância para as estruturas de decisão e de repetição que utilizaremos em nossos programas, pois elas tratam diretamente com valores booleanos para o controle do fluxo de execução.

Nós também podemos combinar valores booleanos com o uso de operadores lógicos, os quais são expressos pela tabela-verdade a seguir:

| A (Booleano 1) | B (Booleano 2) | A && B - AND | A \|\| B - OR |
| -------------- | -------------- | ------------ | ------------- |
| false          | false          | false        | false         |
| false          | true           | false        | true          |
| true           | false          | false        | true          |
| true           | true           | true         | true          |

```java
package exemplo003; 
 
public class Exemplo003 { 

  public static void main(String[] args) { 
    int a = 5, b = 32, c = 7; 
    boolean x; 
    x = a < b; 
    System.out.println("PASSO 1: "+x); 
    x = (b > a) && (c > b); 
    System.out.println("PASSO 2: "+x); 
    b /= a -= 1; 
    c++; 
    x = (b==c); 
    System.out.println("PASSO 3: "+x); 
  } 

} 

```

No primeiro passo temos x recebendo a comparação a < b, que é verdadeira.

No segundo passo, a comparação b > a é verdadeira, mas c > b é falsa, e com o operador lógico aplicado teremos o resultado final como falso.

Em seguida são feitas algumas operações aritméticas de forma concatenada, e que poderiam ser expressas como:

```java
a = a – 1; // a passa a valer 4 
 
b = b / a; // b é divido por a (4) e fica com 8 
 
c = c + 1; // c passa a valer 8 

```

Após estas operações, os valores de b e c são iguais, e a condição se torna verdadeira para o terceiro passo.

Podemos observar a saída resultante a seguir.

![Saída do programa](/media/desenvolvimento_de_software_java/aula1/img06_saida_do_programa.png)

Uma observação final é a de que na linguagem Java a divisão entre inteiros retorna um valor inteiro, enquanto para variáveis do tipo ponto flutuante será um valor real, ou seja, se efetuarmos a operação 5 / 2 teremos 2, enquanto 5.0 / 2 dará 2.5.

### Estruturas de Decisão

O fluxo de execução sequencial indica que as diversas instruções serão executadas na ordem em que são apresentadas no código, mas existem formas de redirecionar o fluxo de execução para partes específicas.

É comum encontrarmos situações onde efetuamos determinadas ações apenas perante certas condições. Para isso, em termos de algoritmos, contamos com as estruturas de decisão.

Basicamente, contamos com duas estruturas de decisão:

- `if..else`
- `switch..case`

![Fluxo if](/media/desenvolvimento_de_software_java/aula1/img07_fluxo_if.png)

#### Estrutura `if..else`

A sintaxe da estrutura if..else é muito simples, conforme podemos observar a seguir.

```java
if ( <<condição>> ) { 

   // instruções para o caso verdadeiro 

} else { 

   // instruções para o caso falso 

} 

```

Se a condição especificada entre parênteses tiver valor verdadeiro, o primeiro bloco de comandos será executado, e se for falsa quem será executado é o segundo bloco.

O uso de chaves é necessário apenas quando temos blocos constituídos de mais de um comando, e o uso de else é opcional.

Vamos observar um pequeno exemplo de uso da estrutura if..else:

```java
package exemplo004; 
import java.util.Scanner; 

public class Exemplo004 { 

  public static void main(String[] args) { 
    Scanner s1 =new Scanner(System.in); 
    System.out.println("DIGITE UM NÚMERO:"); 
    int x = s1.nextInt(); 
    if(x%2==0) 
      System.out.println("O NÚMERO É PAR"); 
    else 
      System.out.println("O NÚMERO É ÍMPAR"); 
  } 

} 

```

Neste exemplo foi utilizado um objeto do tipo Scanner, inicializado com a entrada de dados padrão via teclado (System.in) para obter um número inteiro digitado pelo usuário. Isto pode ser observado na chamada s1.nextInt( ).

Após o usuário entrar com o número pelo teclado, ocorre o teste do if para saber se o resto da divisão por dois resulta em zero, imprimindo a mensagem “O NÚMERO É PAR” e, se o resto não for zero, imprimir “O NÚMERO É ÍMPAR” a partir do else.

Como os blocos tinham apenas uma instrução cada, o uso de chaves não foi necessário em nenhum dos dois.

Podemos observar uma possível saída para a execução desse código a seguir.

![Saída do programa exemplo 004](/media/desenvolvimento_de_software_java/aula1/img08_saida_exemplo04.png)

#### Estrutura switch..case

Utilizamos a estrutura switch..case quando desejamos efetuar ações específicas para cada valor de uma variável. Um exemplo simples de utilização seria a construção de um menu de opções para um sistema.  

A sintaxe básica utilizada por essa estrutura seria:

```java
switch (<<variável>>) { 
  case valor1: 
    // instruções para o valor1 
    break; 
  case valor2: 
    // instruções para o valor2 
    break; 
  default: 
    // instruções para valores que não foram previstos 
} 

```

O comando switch irá desviar o fluxo de execução para os comandos case, de acordo com o valor da variável, sendo que o comando default será executado caso o valor não esteja entre aqueles que foram previstos.

Devemos observar que cada seção case deve ser terminada com o comando break, pois sua ausência irá causar a continuidade da execução, “invadindo” a seção seguinte.

Vamos observar um exemplo de utilização da estrutura switch..case a seguir:

```java
package exemplo005; 

import java.util.GregorianCalendar; 
import java.util.Scanner; 

public class Exemplo005 { 

    public static void main(String[] args) { 
       Scanner s1 =new Scanner(System.in); 
       System.out.println("DIGITE O DIA ATUAL:"); 
       int d = s1.nextInt(); 
       System.out.println("DIGITE O MÊS ATUAL:"); 
       int m = s1.nextInt(); 
       System.out.println("DIGITE O ANO ATUAL:"); 
       int a = s1.nextInt(); 
       GregorianCalendar g1 = new GregorianCalendar(a,m-1,d); 
       switch(g1.get(GregorianCalendar.DAY_OF_WEEK)){ 
           case 1: 
              System.out.println("DOMINGO! FERIADO! :)"); 
              break; 
           case 2: 
           case 3: 
           case 4: 
           case 5: 
           case 6: 
              System.out.println("DIA ÚTIL! TRABALHANDO. :("); 
              break; 
           case 7: 
              System.out.println("SÁBADO! FERIADO! :)"); 
              break; 
           default : 
              System.out.println("ALGO ESTÁ ERRADO...."); 
              break; 
       } 
    } 

} 

``` 

Aqui utilizamos, além do Scanner, um objeto do tipo GregorianCalendar. Esse objeto permitirá tratar elementos de data e hora, sendo inicializado com ano, mês (0 a 11) e dia.

Após a inicialização, utilizamos get(GregorianCalendar.DAY_OF_WEEK) para verificar o dia da semana, o qual é obtido como um valor inteiro de 1 a 7, correspondendo aos dias de domingo a sábado.

Em nosso exemplo, a estrutura switch utiliza esse valor para imprimir a frase equivalente a cada dia da semana, sendo a opção default executada apenas para valores fora da faixa de 1 a 7, algo que não ocorrerá devido ao uso de GregorianCalendar.

Podemos observar uma possível saída para a execução desse código a seguir.

![Saída do programa exemplo 004](/media/desenvolvimento_de_software_java/aula1/img09_saida_exemplo05.png)


### Estruturas de repetição

Outra forma de redirecionar o fluxo de execução é através do uso de estruturas de repetição. Elas servem para repetir a execução de um comando ou bloco de comandos enquanto determinada condição for verdadeira.

A linguagem Java permite a utilização das seguintes estruturas de repetição:

- for;
- while;
- do..while.

![Fluxo estrutura de repetição](/media/desenvolvimento_de_software_java/aula1/img10_estrutura_repeticao.png)

#### Estrutura for

A implementação de estruturas do tipo PARA..FAÇA utiliza a seguinte sintaxe: 

```java

for ( <<inicialização>>; <<condição>>; <<incremento>> ) 

```

Inicialização: definição dos valores iniciais das variáveis de controle

Condição: expressão booleana que determina a execução do comando ou bloco de comandos

Incremento: comandos para atualização das variáveis de controle

Por exemplo, um loop de 1 a 5 seria `for( int i=1 ; i<=5 ; i++ )`.

Estruturas deste tipo são utilizadas quando trabalhamos com uma regra de execução com início e fim bem determinados, como no caso de passeios em vetores, ou quando somamos os valores de uma sequência. Vamos observar o exemplo a seguir.

```java

public class Exemplo006 { 
public static void main(String[] args) { 
   // Calculo do valor médio da sequencia y = f(x) = x * x 
  // Media = Somatorio dos valores / quantidade 
  // Limites 1 a 5 
  double soma = 0.0; 
  for(int x=1; x<=5; x++) 
    soma += Math.pow(x, 2); 
    // eleva x a potência 2 e acumula 
  System.out.println(soma/5); 
} 
} 

```

#### Estrutura while e do..while

A implementação de estruturas do tipo ENQUANTO..FAÇA utiliza a seguinte sintaxe:

condição: Expressão booleana que determina a execução do comando ou bloco de comandos.

```java

while ( <<condição>> ) { 

   // Bloco de Comandos 

} 
```

Com relação às estruturas do tipo FAÇA..ENQUANTO, a sintaxe utilizada seria:

```java

Do { 

   // Bloco de Comandos 

} while ( <<condição>> ); 

```

No exemplo seguinte podemos observar a utilização do comando while.

```java
public class Exemplo007 { 

  public static void main(String[] args) { 
    int[] x1 = {21, 32, 15, 27, 33, 17}; 
    int posicao = 0; 
    int soma = 0; 
    while(posicao< x1.length){ 
      // Enquanto for menor que o tamanho do vetor 
      soma += x1[posicao]; 
      posicao++; 
    } 
    System.out.println(soma); 
  } 

} 
```

Neste exemplo é criado um vetor inicializado na criação, assumindo 6 posições, ou seja, terá os índices de 0 a 5.

![Vetor com valores](/media/desenvolvimento_de_software_java/aula1/img11_vetor.png)

Em seguida procedemos ao somatório desses valores com o uso de um comando while, tendo como condição posicao< x1.length. Como o length neste caso é 6, a posição varia de 0 a 5.

A cada rodada, o valor do vetor na posição equivalente é adicionado à variável soma, e não podemos esquecer de incrementar a posição, pois caso contrário teríamos uma repetição infinita.

O uso de length permite que seja alterada a quantidade de elementos de x1 na inicialização sem a necessidade de modificações no restante do código.

Ao final teremos impresso o valor 145, que corresponde à soma 21+32+15+27+33+17.

O comando do..while tem funcionamento similar, mas o teste é feito ao final, o que garante pelo menos uma execução.

Podemos observar um exemplo de utilização do comando do..while a seguir.

```java
public class Exemplo008{ 
 
import java.util.Scanner; 
 
public class Exemplo008 { 

  public static void main(String[] args) { 
    Scanner teclado = new Scanner(System.in); 
    int soma = 0; 
    do{ 
      System.out.print("Digite um numero (0 para sair):"); 
      valor = teclado.nextInt(); 
      soma += valor; 
    } while(valor!=0); 
    System.out.printf("\nA soma dos numeros "+ 
                      "digitados e: %d\n",soma); 
  } 

} 
```

Neste nosso exemplo serão solicitados os números ao usuário até que ele digite 0, sendo apresentado a seguir o somatório dos números digitados por ele.

Podemos verificar uma possível saída desse programa a seguir.

![Saída do programa 08](/media/desenvolvimento_de_software_java/aula1/img12_saida_exemplo08.png)

## Aula 2 - Orientação de Objetos

Tem como objetivo:

- Aumento do reuso de código;
- Facilidade de manutenção;
- Documentação automatizada.

Começamos a utilizar de forma mais ampla a programação orientada a objetos (POO) com o advento das interfaces gráficas, pois ficou muito evidente que a programação estruturada não era a melhor opção para construir ambientes constituídos de janelas.

Antigamente tínhamos que utilizar as APIs do sistema operacional para a construção de cada janela, de forma independente, mas com a POO podemos definir um personagem denominado “Janela”, o qual terá atributos como “posição”, “largura” e “altura”, e será capaz de efetuar ações como “abrir”, “minimizar” e “maximizar”, e, a partir daí, colocarmos a quantidade necessária de personagens deste tipo para implementar as interfaces de nossos sistemas.

### Abstração

Um dos pilares da POO é o conceito de **abstração**, que se refere à definição de um modelo simplificado de algo maior.

Quando abstraímos algo, estamos preocupados apenas com os detalhes que sejam relevantes para o problema de interesse, e essas abstrações serão representadas como **classes** na POO, as quais trazem a definição dos atributos e métodos suportados pelos personagens:

- ATRIBUTOS: definem características físicas, como cor, idade, endereço, etc
- MÉTODOS: as ações ou os verbos que podem ser praticados, tais como comer, andar, dormir.

Neste ponto podemos abandonar a palavra “personagem” e passar a tratar dos dois níveis de programação que utilizaremos:

- CLASSE: funciona como um molde (tipo ou domínio), para definir como serão os objetos criados a partir da mesma. Elas definem apenas os tipos destes atributos, sem assumir valores.
- OBJETOS: São como variáveis ou elementos físicos criados a partir do molde que é a classe. Cada objeto irá assumir valores específicos para os atributos definidos na classe.

Exemplo:

Poderíamos considerar uma classe “Pessoa”, que apresenta como atributos o nome e o telefone.

Mas qual nome e telefone?

Cada objeto dessa classe irá assumir valores específicos, como p1 se chama João e seu número de telefone é 1111-1111, enquanto p2 se chama Maria e seu número de telefone é 2222-2222.

Vamos observar estes conceitos iniciais a seguir. Para esse exemplo deveremos criar dois arquivos, um para **Pessoa** e outro para **Exemplo010**.

```java
package exemplo010; 

public class Pessoa { 
  String nome; 
  String telefone; 
 
  void exibir(){ 
    System.out.println(nome+"::"+telefone); 
  }
}
```

```java
package exemplo010; 

public class exemplo010 { 

  public static void main(String[] args) { 
    // Instanciando os objetos p1 e p2 
    Pessoa p1 = new Pessoa(); 
    Pessoa p2 = new Pessoa(); 
 
    // Preenchimento dos atributos dos objetos p1 e p2 
    p1.nome = "João"; 
    p1.telefone = "1111-1111"; 
    p2.nome = "Maria"; 
    p2.telefone = "2222-2222"; 
 
    // Chamada ao método exibir em p1 e p2 
    p1.exibir(); 
    p2.exibir(); 
  }
}
```

Conforme podemos observar, o primeiro arquivo (Pessoa.java) contém a classe Pessoa, a qual define os atributos nome e telefone e o método exibir.

No outro arquivo (`Exemplo010.java`) teremos a classe chamadora e seu ponto inicial de execução `main`, onde inicialmente são **instanciados** os objetos `p1` e `p2` com o uso do operador `new`, responsável por alocar esses objetos na memória.

Acompanhando a sequência de comandos, teremos o preenchimento dos atributos nome e telefone para cada um dos objetos, e a chamada ao método exibir de cada um deles.

Teremos como resultado final a impressão do nome e o telefone de cada objeto.

![Saída Programa exemplo 10](/media/desenvolvimento_de_software_java/aula2/img01_resultado_exemplo10.png)

Existe também um método especial chamado de **construtor**, responsável pela **inicialização** de um objeto recém-criado. Note que ele não aloca o objeto, sendo esta responsabilidade do operador `new`, mas permite inicializar atributos do objeto em seu primeiro momento de existência.

Em algumas linguagens temos também o método **destrutor**, mas o Java não necessita deste método, particularmente por trazer o **garbage collector**, tecnologia que remove da memória qualquer objeto que não possa ser acessado e não tenha mais utilidade para o programa.

Refazendo o exemplo anterior:

```java
package exemplo010; 

public class Pessoa { 
  String nome; 
  String telefone; 
 
  Pessoa(String nome, String telefone){ 
    this.nome = nome; 
    this.telefone = telefone; 
  } 
 
  void exibir(){ 
    System.out.println(nome+"::"+telefone); 
  }
}
```

```java
package exemplo010; 

public class exemplo010 { 

  public static void main(String[] args) { 
    // Instanciando e inicializando os objetos p1 e p2 
    Pessoa p1 = new Pessoa("João","1111-1111"); 
    Pessoa p2 = new Pessoa("Maria","2222-2222"); 
 
    // Chamada ao método exibir em p1 e p2 
    p1.exibir(); 
    p2.exibir(); 
  } 

} 

```

Essa modificação do código não irá alterar a saída, mas podemos observar como o uso de um construtor simplificou muito a inicialização dos objetos no main.

Todo construtor é definido pela criação de um método com o mesmo nome da classe, e seria possível utilizar parâmetros com nomes diferentes dos atributos que serão inicializados, mas ocorreria uma grande perda de semântica.  

O problema agora é como iremos diferenciar os **parâmetros** e **atributos**, já que eles têm os mesmos nomes. É neste ponto que surge um elemento da orientação a objetos chamado de ponteiro de **autorreferência**, expresso em Java como `this`, e que sempre aponta para os atributos e métodos do objeto corrente.

```java
this.nome = nome; 
```

A forma mais fácil de ler essa linha seria “o nome **deste** objeto receberá o nome passado como parâmetro”.

Algumas classes apresentam vários construtores diferentes, cada um deles com um conjunto de parâmetros distintos, de forma a se adaptarem a contextos diversos, e a aplicação dessa técnica é chamada de **sobrecarga**.

Embora nós utilizemos muito a sobrecarga na orientação a objetos, principalmente na criação de métodos construtores, esta é uma técnica antiga, já existente na programação estruturada, e amplamente utilizada na linguagem C.

### Pacotes e bibliotecas

Quando fazemos um sistema orientado a objetos é comum ocorrer um grande número de classes, e precisamos de uma maneira organizada para classificar e agrupar essas classes de acordo com suas afinidades a determinado contexto.

O primeiro nível de organização são os pacotes (**package**), que seria equivalente ao diretório no qual a classe se encontra, segundo um caminho relativo, tomando como base o diretório raiz do projeto.

EXEMPLO: O diretório “\java\math” equivaleria ao pacote “java.math”.

Se observarmos os códigos de exemplo anteriores, veremos a presença da palavra `package`, imediatamente no início dos mesmos. Todo arquivo Java deve ter a assinatura de pacote correspondente ao diretório onde se encontra.

Quando utilizamos classes pertencentes ao mesmo pacote não há necessidade de importar elementos, mas ao tratar de pacotes diferentes, será necessário importar elementos de outro pacote com o uso de `import`.

Podemos importar classes dos pacotes do projeto ou de bibliotecas externas.

As bibliotecas são conjuntos de pacotes Java, e suas respectivas classes, compactados para um arquivo com extensão **“.zip”** ou **“.jar”**. Essas bibliotecas podem ser referenciadas pelo projeto, ou adicionadas ao **CLASSPATH**, no qual estão relacionadas as bibliotecas padrão do ambiente.

Se quisermos acessar um banco de dados MySQL, podemos adicionar o arquivo mysql-connector.jar ou similar às bibliotecas do projeto. Depois é só utilizar as importações corretas.

O comando `import` pode ser usado de duas formas:

_Incluindo apenas uma classe, como `import java.util.ArrayList`_ ou _Incluindo todas as classes do pacote (sem recursividade), como `import java.util.*`

### Herança

 segundo pilar da orientação a objetos é a **herança**, que nos permite criar uma nova classe a partir de outra já existente, configurando um reaproveitamento estrutural.

A árvore de família de animais que nos é apresentada nas aulas de Biologia.

Ela segue o mesmo princípio da herança em termos de programação, pois ao definir um cachorro ou coelho aproveitamos o conceito já existente de mamífero.

Para derivar uma classe de outra utilizaremos a palavra reservada `extends`, e assim como podemos acessar os atributos e métodos internos com `this`, utilizamos a palavra `super` para ter acesso aos atributos e métodos da classe original.

```java
package exemplo010; 

public class Profissional extends Pessoa{ 
  String profissao; 
  Profissional(String nome, String telefone, String profissao) { 
    super(nome, telefone); 
    this.profissao = profissao; 
  } 
}
```

Aqui nós criamos uma classe Profissional descendente de Pessoa com o uso de extends. Esta nova classe teve o atributo “profissao” adicionado.

Não é permitido utilizar acentuação em nomes de atributos, e também um construtor com três parâmetros.

A nova classe apresenta os atributos nome, telefone e profissao, sendo os dois primeiros herdados de Pessoa, e a palavra `super` foi utilizada para chamar o construtor de Pessoa a partir do construtor de Profissional.

### Encapsulamento  

Quando consideramos uma estrutura fechada qualquer, observamos que alguns elementos são visíveis, enquanto outros não.

Exemplo: Ao observarmos uma pessoa nós podemos ver sua face, seu cabelo, seus braços, mas não temos acesso ao seu estômago nem pulmão.

Na orientação a objetos temos esta mesma característica, pois classes definem estruturas fechadas, nas quais o acesso a seus atributos e métodos deve ser controlado, e para tal iremos contar com três níveis de acesso:

- Público (public): Permite que qualquer um acesse o atributo ou método.
- Privado (private): Não permite acessos externos, sendo utilizado apenas na programação interna da classe.
- Protegido (protected): Permite a utilização na classe e nos descendentes, mas não permite acessos externos.

Quando não definimos nada em termos de nível de acesso, o padrão é o de pacote, ou seja, todas as classes do mesmo pacote podem acessar livremente, mas se ocorrer a importação desse pacote por uma classe pertencente a outro, essa classe externa não terá acesso aos atributos e métodos com nível de pacote.  

Mais uma pequena alteração em nossa classe Pessoa...

```java
package exemplo010; 
 
public class Pessoa{ 
  private String nome; 
  private String telefone; 
 
  public Pessoa(String nome, String telefone){ 
    this.nome = nome; 
    this.telefone = telefone; 
  } 
 
  public void exibir(){ 
    System.out.println(nome+"::"+telefone); 
  }
}
```

Essa alteração não impactará na classe chamadora, pois o construtor e o método exibir estão definidos como públicos, mas se tentarmos acessar os atributos de p1 ou p2 a partir do main, como na primeira versão, ocorrerá um erro de compilação.

```java

p1.nome = "João"; // Esta linha irá gerar um erro de compilação 

```

É muito comum que precisemos controlar o acesso a determinado atributo sem, no entanto, impedir esse acesso, e nesse ponto devemos utilizar os getters e setters.  

Esse controle é chamado de encapsulamento, que trata de mais um dos pilares da orientação a objetos e, em termos formais, visa ocultar detalhes da implementação interna da classe, fornecendo apenas uma interface com métodos de negócio e métodos de acesso.

O método **getter** serve para obter o valor de um atributo interno, enquanto o **setter** permite escrever um valor nesse atributo. O conjunto dos dois define uma **propriedade** da classe.

Podemos implementar muito facilmente a técnica de encapsulamento em nossa classe Pessoa modificada.

```java
package exemplo010; 

public class Pessoa{ 
  public String getNome(){ 
    return nome; 
  } 
  public void setNome(String nome){ 
    this.nome = nome; 
  } 
  public String getTelefone(){ 
    return telefone; 
  } 
  public void setTelefone(String telefone){ 
    this.telefone = telefone; 
  } 
  private String nome; 
  private String telefone; 
  public Pessoa(String nome, String telefone){ 
    this.nome = nome; 
    this.telefone = telefone; 
  } 
  public void exibir(){ 
    System.out.println(getNome()+"::"+getTelefone()); 
  }
}
```

Note que foram apenas acrescentados os métodos de leitura (getNome e getTelefone) e os métodos de escrita (setNome e setTelefone). Para não ocorrer perda de semântica devido a alteração de nomes, o uso de `this` é necessário nos **setters**.

### Polimorfismo

O último dos pilares da orientação a objetos é o polimorfismo, consistindo na possibilidade de uma classe descendente efetuar alterações sobre métodos herdados, de forma a adaptar as funcionalidades a seu próprio contexto.

Esta talvez seja a característica mais poderosa da orientação a objetos, proporcionando grande flexibilidade a qualquer sistema, e devemos compreendê-la corretamente para tirar o melhor proveito da metodologia.

Como já é de nosso conhecimento, por meio do processo de herança, as classes descendentes herdam todas as caraterísticas existentes nas ancestrais.

Mas e se algumas ações não forem exatamente o que se espera?

É nesse ponto que precisamos do polimorfismo (Significa “múltiplas formas”, ou seja, as diversas formas com que uma ação pode ser efetuada).

![Diagrama de Classes Profissional e suas subclasses](/media/desenvolvimento_de_software_java/aula2/img02_diagrama_classe.png)

Este é um diagrama de classes da **UML** (Unified Modeling Language) representando a classe Profissional e descendentes diretos e indiretos da mesma.

Tomando como base Profissional, podemos dizer que todo objeto deste tipo irá trabalhar, assim como os objetos das classes descendentes, mas certamente irão trabalhar de forma diferente.

- se for um engenheiro pode estar indo fazer o projeto de uma casa ou de um carro;
- no caso do médico talvez esteja indo operar alguém;
- e um advogado estará acompanhando algum processo.

No entanto, a frase seria a mesma: “Estou indo trabalhar”.

O uso de polimorfismo permitirá alterar a funcionalidade do método trabalhar para as diversas classes envolvidas.

Vamos observar um código com uso de polimorfismo, com a alteração da nossa classe Profissional de exemplo. Essa alteração é necessária para que o método exibir passe a mostrar também a profissão, e não apenas o nome e telefone.

```java
public class Profissional extends Pessoa { 

  private String profissao; 
  
  public Profissional(String nome, String telefone, String profissao) {
    super(nome, telefone); 
    this.profissao = profissao; 
  } 

  @Override 
  public void exibir() { 
    // Chama o exibir de Pessoa, imprimindo nome e telefone 
    super.exibir(); 
    
    // Complementa a informação acerca da profissão 
    System.out.println("\tTrabalha como "+profissao);
  }
} 

```

Note que foi criado um vetor de Pessoa, aceitando tanto Pessoa quanto Profissional. Isto se deve a uma lei da POO que define o seguinte: “qualquer **descendente** pode ser utilizado no lugar da classe”.

Se observarmos o mundo real, esta lei também pode ser aplicada, pois um profissional é uma pessoa, embora nem sempre uma pessoa seja um profissional.

A saída desse programa será a seguinte:

![Saída do programa exemplo 10a](/media/desenvolvimento_de_software_java/aula2/img03_resultado_exemplo10a.png)

Note que mesmo definido o vetor como do tipo **Pessoa**, o exibir correto foi chamado para o **Profissional** existente neste vetor, e isso se deve ao polimorfismo.

### Classes abstratas e interfaces

Normalmente confundimos muito as palavras abstração e abstrato, mas elas apresentam sentidos muito distintos:

- *Uma abstração é um modelo simplificado de algo.*
- *Um elemento abstrato é algo intangível, que não é palpável ou concreto.*

Existem dois tipos de elementos abstratos em Java: classes abstratas e interfaces.

As **classes abstratas** são incompletas, não podem gerar objetos, mas servem de base para impor determinada característica funcional a seus descendentes, que serão obrigados a implementar as funcionalidades abstratas para gerar objetos.

Vamos observar um exemplo de classe abstrata em Java envolvendo a criação de quatro classes.

```java
public abstract class Mamifero { 
  protected String familia; 
  public abstract void mamar(); 
  public String getFamilia(){ 
    return familia; 
  } 
} 
```

```java
public class Cachorro extends Mamifero{ 
  public Cachorro() { 
    familia = "Canidae"; 
  } 
  @Override 
  public void mamar() { 
    System.out.println("Cachorro mamando..."); 
  } 
}
```

```java
public class Gato extends Mamifero{ 
  public Gato() { 
    familia = "Felidae"; 
  } 
  @Override 
  public void mamar() { 
    System.out.println("Gato mamando..."); 
  } 
}
```

```java
public class Exemplo011 { 
  public static void main(String[] args) { 
    Mamifero m = new Gato(); 
    m.mamar(); 
  } 
} 
```

Nós criamos inicialmente a classe abstrata Mamifero, com uso da palavra `abstract` em termos da definição da classe e do método abstrato interno.

Essa classe não pode gerar instâncias, afinal falta uma parte dela que é o método **mamar( )**, mas permite herança e obriga a definição do método faltante. Isso pode ser observado nas classes Cachorro e Gato, descendentes de Mamifero, e que por serem concretas podem ser instanciadas.  

Ao final, podemos ver uma classe de teste, onde é instanciado um Gato no lugar de Mamifero, sendo chamado em seguida o método mamar( ) implementado na classe descendente. Como esperado, teremos a impressão da frase “Gato mamando...”.  

Outro tipo de elemento abstrato é a interface, e esta não deve ser confundida com interface visual, que trata da interação com o usuário.

Aqui estamos preocupados com a interface programacional, que se preocupa em definir quais métodos estarão disponíveis para uso de determinado tipo de componente.

Em termos práticos, uma interface é um conjunto de assinaturas de métodos abstratos, os quais devem ser implementados pelas classes que se proponham a tal. Ao implementar esses métodos, as classes passam a ser reconhecidas por algum ferramental que os utiliza, promovendo funcionalidades específicas.

As interfaces são de grande utilização no Java, e podemos observar um exemplo a seguir, complementando o exemplo anterior.

```java
public interface Voo { 
  void voar(); 
} 
```

```java
public class Morcego extends Mamifero implements Voo{ 
  public Morcego() { 
    familia = "Phyllostomidae"; 
  } 
 
  @Override 
  public void mamar() { 
    System.out.println("Morcego mamando..."); 
  } 
 
  @Override 
  public void voar() { 
    System.out.println("Morcego voando..."); 
  } 
 
}
```

```java
public class Exemplo011a { 
  public static void main(String[] args) { 
    Object[] objetos = {new Gato(), new Morcego(), 
                       new Cachorro()}; 
 
    for(int i=0; i< 3; i++) { 
      if(objetos[i] instanceof Voo) 
        ((Voo)objetos[i]).voar(); 
          // Conversão de tipo (type cast) necessária 
    } 
  } 
} 
```

Neste exemplo temos a definição de uma `interface`, com o uso da palavra `interface` no lugar de `class`. Uma interface é naturalmente abstrata, logo seus métodos são considerados por padrão **públicos** e **abstratos**.

Uma observação é a de que as interfaces não aceitam atributos, e podem ser consideradas como conjuntos de assinaturas de métodos.

Podemos observar que a classe Morcego **deriva** de Mamifero e **implementa** a interface Voo com o uso da palavra `implements`. Ao implementar a interface, ela se torna obrigada a implementar o método **voar( )**.

Ao final temos um pequeno teste, onde é percorrido um vetor de objetos, e perguntado a cada um deles se implementa Voo ou não com o uso de `instanceof`, e caso implemente, ocorre a conversão (**type cast**) para o tipo da interface e a subsequente chamada de **voar ( )**.

Executando o exemplo teremos apenas a frase “Morcego voando...” sendo impressa.

Note que implementar é muito diferente de herdar. Nesse caso fica claro que Morcego é um Mamifero, e que ele implementa Voo, mas não herda do mesmo.

Embora muitos confundam as interfaces com classes abstratas, as diferenças em termos metodológicos são muito grandes:

**As classes abstratas definem uma regra para sua família de classes.** X **As interfaces podem ser implementadas por qualquer classe que necessite participar de algum processo específico.**

## Aula 3 - Exceções e elementos comportamentais

### Exceções

Muitas vezes temos que preparar nossos sistemas para a possibilidade de ocorrência de erros durante a execução, podendo ocorrer pela indisponibilidade de algum recurso, como rede ou espaço em disco, pela entrada de dados em formato incorreto, entre diversas outras situações.

Outro assunto muito relevante para os sistemas atuais é a utilização de modelagem comportamental, aumentando o reuso de processos e estruturas, o que pode ser feito no ambiente Java por meio de classes genéricas ou pelo uso de anotações. Inclusive, uma importante biblioteca Java para o manuseio de coleções apresenta uma implementação atual baseada em classes genéricas.

Nos ambientes orientados a objetos, os diversos erros de execução são encapsulados em classes especiais denominadas **exceções**.

Temos a classe básica Exception, que define apenas um código de erro e uma mensagem, voltada para erros genéricos.

A partir desta classe, e utilizando o mecanismo de herança, são definidas exceções mais específicas, com maior gama de informações acerca do erro.

![Diagrama Exceções](/media/desenvolvimento_de_software_java/aula3/img01_diagrama_excecoes.png)

Para tratarmos uma exceção devemos utilizar uma estrutura de fluxo específica, baseada no comando `try` (tentar), o qual utiliza a seguinte sintaxe:

```java
try { 
  // Bloco de comandos protegido 
} catch (IOException e1) { 
  // Tratamento de erro de IO 
} catch (Exception e2) { 
  // Tratamento de erro genérico 
} finally { 
  // Execução obrigatória, independente da ocorrência de erros 
}
```

Inicialmente é executado o bloco protegido pelo comando `try`, e se ocorre uma exceção do tipo **IOException**, ela é capturada em **e1** com o uso de `catch(IOExeption e1)`, sendo executado o tratamento de erro de IO e seguindo para o bloco do `finally`.

Para qualquer outro tipo de exceção, será executado o bloco para tratamento de erro genérico, com a captura do erro em **e2**, e seguindo para `finally` ao término. Lembrando que, segundo a orientação a objetos, qualquer descendente pode ser utilizado no lugar da classe original, o que viabiliza essa funcionalidade.

Se invertermos a ordem dos blocos catch ocorrerá um erro de compilação, pois o fato de Exception ser mais genérico impediria a captura de quaisquer outras exceções.

Quanto ao bloco `finally`, mesmo sem ocorrência de erros, ele será executado.

Um exemplo prático no qual utilizaríamos essas instruções seria na inserção de dados em um banco, onde devemos abri-lo, inserir os registros e fechar o banco. Ocorrendo ou não erros durante a inserção, o banco deve ser fechado.

```java
ABRIR_BANCO_DE_DADOS( );
try {
  INSERIR( );
  INSERIR( );
  // Diversos comandos de inserção 
} catch (Exception e) { 
  // Tratamento de erro genérico
} finally {
  FECHAR_BANCO_DE_DADOS( );
} 
```

Para qualquer exceção não silenciosa, o compilador considerará como erro caso a possibilidade de ocorrência da mesma não seja tratada. Nesses casos precisamos utilizar a estrutura **try..catch**, ou avisar ao compilador que não será tratado, mas sim ecoado para o chamador do método, por meio da assinatura com `throws`.

Também podemos criar nossas próprias exceções, de forma a utilizá-las como sinalizações de erros específicos de nossos sistemas.

```java
public class ErroCalc extends Exception{
  public ErroCalc(int a, int b){
    super("Erro com os numeros "+a+" e "+b);
  }
}
```

Em nossa exceção personalizada (ErroCalc) temos um construtor que recebe dois valores inteiros, e chama o construtor de Exception, com o uso de super, passando a mensagem correta.

Esta exceção poderia ser utilizada em uma classe de nosso sistema.

```java
public class Calculadora { 
  public int somar(int a, int b){ 
    return a+b; 
  } 
  public int dividir(int a, int b) throws ErroCalc { 
    if(b==0) 
      throw new ErroCalc(a, b); 
    return a/b; 
  } 
} 
```

No caso da classe Calculadora, temos os métodos somar, onde não ocorre exceção, e dividir, que gera ErroCalc quando o parâmetro **b** tem valor zero. Note que não basta alocar o objeto ErroCalc com `new`, sendo necessário o uso do comando `throw` para lançar a exceção.

Caso não ocorra tratamento com try..cath, ao lançar ErroCalc a execução de dividir é imediatamente interrompida, retornando ao chamador, sendo também necessário informar ao compilador que esse método pode gerar uma exceção desse tipo com o uso do comando `throws` em sua assinatura.

Podemos testar facilmente nossa exceção com o uso de um objeto do tipo Calculadora.

```java
public class TesteCalc { 
  public static void main(String[] args) { 
    Calculadora c1 = new Calculadora();
    try {
       System.out.println(c1.somar(2, 3));
       System.out.println(c1.dividir(6, 3));
       System.out.println(c1.dividir(6, 0));
    } catch (ErroCalc e)
       System.out.println(e.getMessage());
    }
  }
```

Neste exemplo, a condição que irá gerar a exceção será a chamada **c1.dividir(6,0)**, mas mesmo que não colocasse o valor zero, o compilador exigiria o tratamento, já que dividir assinala uma possibilidade de exceção com `throws ErroCalc`.

A saída que obteremos será a seguinte:

![Saída do programa TesteCalc](/media/desenvolvimento_de_software_java/aula3/img02_saida_programa_test_calc.png)

### O que é modelagem comportamental?

Em muitas situações não conseguimos expressar a realidade por meio de simples objetos.

Para uma situação desse tipo, não importa qual carro esteja entrando ou saindo, mas sim que o trecho esteja engarrafado. Logo, não são os objetos que definem a abstração principal, mas sim o **comportamento**.

Poderíamos dizer o mesmo sobre uma fila. Você pode ter uma sequência de pessoas, elefantes, carros, ou qualquer outra coisa, e todas essas sequencias organizadas seriam filas, independente dos objetos que as constituem.

Essa generalização também pode ser feita para uma pilha de pratos ou de livros, pois não importa de qual tipo de objeto se trate, e sim que estejam empilhados.

Na programação utilizamos diversos comportamentos, normalmente definidos por estruturas de dados, como as próprias **Filas** e **Pilhas**, por exemplo.

Em termos de orientação a objetos, existem duas ferramentas que permitem a implementação de modelos comportamentais: **Classes Genéricas** e **Anotações**.

### Classes genéricas

As **classes genéricas**, também chamadas de **classes template**, já tinham sido idealizadas no início da orientação a objetos, e eram comuns em linguagens como o C++, mas veio para o Java em versões um pouco mais recentes por intermédio dos **Generics**.

Quando criamos uma classe genérica estamos modelando um comportamento com lacunas bem definidas ao qual serão atribuídas classes para preencher tais lacunas e completar a funcionalidade abstrata previamente definida.

Vamos observar um exemplo.

```java

package exemplo020; 
 
  public class Pilha‹;K›; { 
 
   class NoPilha‹;K›; { 
      K dado; 
      NoPilha‹;K›; proximo; 
   } 
 
   private NoPilha‹;K›; topo = null; 
 
   public void empilhar(K dado){ 
      NoPilha‹;K›; novo = new NoPilha<>(); 
      novo.dado = dado; 
      novo.proximo = topo; 
      topo = novo; 
   } 
 
   public K desempilhar(){ 
      if(topo==null) 
         return null; 
      NoPilha‹;K›; antigo = topo; 
      topo = topo.proximo; 
      return antigo.dado; 
   } 
 
} 
```

Neste exemplo foi definida uma classe genérica de Pilha, com os métodos para empilhar e desempilhar (push/pop), podendo ser observada a presença da lacuna definida pela letra K. Na verdade poderia ser qualquer letra, devendo apenas ser colocada junto ao nome da classe. `public class Pilha‹K›`

A letra K representa algo genérico e será substituída em todas as ocorrências posteriores quando definirmos o tipo de objeto a ser utilizado.

Por exemplo, se utilizarmos String, o método empilhar pode ser lido da seguinte forma:

```java

public void empilhar(String dado){ 

     NoPilha ‹String› novo = new NoPilha‹›(); 

     novo.dado = dado; 

     novo.proximo = topo; 

     topo = novo; 

} 
```

É interessante observar também a definição de uma inner class chamada NoPilha, ou seja, uma classe utilitária interna, que só pode ser utilizada na programação da classe Pilha. Na prática ela auxilia na construção de uma estrutura de pilha típica, onde um valor é colocado no topo, e deve apontar para o elemento logo abaixo na pilha (proximo).

![Diagrama Push operation - operação de adicionar elemento em uma fila](/media/desenvolvimento_de_software_java/aula3/img03_push_operation.png)

Sempre devemos lembrar que a pilha trata de uma estrutura LIFO (Last In First Out), o que significa que o último a entrar é o primeiro a sair. Isto faz sentido se fizermos uma analogia com uma pilha de pratos, já que não é possível pegar o prato de baixo sem que os demais caiam.

Agora podemos criar um programa para testar nossa classe de Pilha.

```java

package exemplo020; 

public class Exemplo020 { 

  public static void main(String[] args) { 
    Pilha pilha1 = new Pilha<>(); 
    pilha1.empilhar(5); 
    pilha1.empilhar(7); 
    pilha1.empilhar(9); 
    Integer x; 
    while((x=pilha1.desempilhar())!=null) 
    System.out.println(x); 
  } 

} 
```

Esse programa inicialmente cria uma **Pilha** de elementos `Integer` (classe **wrapper** para `int`, ou seja, inteiros de 4 bytes), e em seguida empilha os valores 5, 7 e 9.

Observando o que ocorre a seguir, vemos a declaração de uma variável **x** que receberá os valores desempilhados, enquanto esse valor for diferente de nulo, imprimindo **x** a cada rodada.

Por se tratar de uma estrutura **LIFO**, é natural que os números sejam impressos na ordem inversa da entrada, ou seja, serão impressos os valores 9, 7 e 5.

### Coleções

As coleções são de grande importância para o Java, sendo organizadas pela Oracle em um grupo denominado **JCF (Java Collections Framework)**, o qual foi todo implementado com o uso de classes genéricas.

Ao contrário de vetores, que apresentam um número de elementos fixo, as coleções funcionam internamente como listas encadeadas, e permitem que objetos sejam adicionados ou removidos a qualquer momento.

Nós podemos verificar a relevância dessa família de classes pelo simples fato de ter sido criada uma nova funcionalidade para a estrutura `for` baseada em coleções, e que posteriormente foi expandida para vetores.

Em outras linguagens existem estruturas `foreach`, com funcionamento similar, e a leitura que devemos fazer é “para cada elemento pertencente à coleção”.

A sintaxe básica seria a seguinte:

```java

for( Classe obj: Coleção ‹Classe› ) { 

  // Bloco de instruções 

} 
```

Uma **Collection** é uma classe abstrata e que, portanto, não pode ser utilizada diretamente, mas nós podemos instanciar os seus diversos descendentes com funcionalidades específicas.

Podemos observar, a seguir, um exemplo de uso de **ArrayList**, descendente de Collection.

```java

package exemplo021; 
import java.util.ArrayList; 

public class Exemplo021 { 
  
  public static void main(String[] args) { 
    ArrayList‹String› lista = new ArrayList<>(); 
    lista.add("Primeiro"); 
    lista.add("Segundo"); 
    lista.add("Terceiro"); 
    for(String x: lista){ 
        System.out.println(x); 
    } 
  } 

} 
```

Neste exemplo é criada uma coleção do tipo ArrayList, com elementos do tipo String, e em seguida adicionamos três elementos nessa coleção com o uso do método **add**.

Depois de adicionados os elementos, podemos percorrer a lista com uso do for, e a variável x receberá o primeiro valor da lista na primeira rodada, em seguida, o segundo e finalmente o terceiro, imprimindo o valor recebido a cada rodada.

Com isso teremos a seguinte saída:

![Saída do programa Exemplo021](/media/desenvolvimento_de_software_java/aula3/img04_saida_exemplo21.png)

Nas versões atuais do Java é possível também utilizar operadores **lambda**, segundo o **paradigma funcional**, e o trecho voltado para a impressão dos valores poderia ser escrito da seguinte forma:

```java

lista.forEach((x) -> { 

  System.out.println(x); 

}); 
```

Os principais métodos do ArrayList‹E› são apresentados no quadro abaixo: 
![Principais métodos de Array List](/media/desenvolvimento_de_software_java/aula3/img05_metodos_arraylist.png)

Dentre as diversas outras classes do JCF, além do **ArrayList** outra de grande utilização é **HashMap**. Com o uso desta classe é possível estabelecer relações do tipo chave-valor com muita facilidade.

Se quisermos fazer um controle no qual temos o código de nossos produtos no formato inteiro e os nomes no formato texto, poderemos declarar o HashMap da seguinte forma: `HashMap ‹ Integer, String > produtos = new HashMap‹›( );`

Observando a declaração do HashMap, vemos que devem ser colocadas na tipificação dele a classe da chave e a classe do dado (valor).

```java

package exemplo022; 
import java.util.HashMap; 
import java.util.Scanner; 

public class Exemplo022 { 

  public static void main(String[] args) { 
    Scanner teclado = new Scanner(System.in); 
    HashMap‹Integer,String› produtos = new HashMap<>(); 
    int opcao; 
    do{ 
      System.out.println("Digite 1 para incluir, "+ 
                        "2 para consultar, 0 para sair"); 
      opcao = teclado.nextInt(); 
      switch(opcao){ 
        case 1: 
          System.out.println("Código do novo produto:"); 
          int codigoN = teclado.nextInt(); 
          System.out.println("Nome do novo produto:"); 
          String nomeN = teclado.next(); 
          produtos.put(codigoN, nomeN); 
          break; 
        case 2: 
          System.out.println("Digite o código:"); 
          int codigo = teclado.nextInt(); 
          String nome = produtos.get(codigo); 
          if(nome!=null) 
            System.out.println(nome); 
          break; 
        } 
    } while(opcao!=0); 
  } 

} 
```

Nesse programa utilizamos uma estrutura de repetição do tipo **do..while**, onde é solicitada ao usuário qual ação ele deseja efetuar, sendo 1 referente à inclusão de um produto, 2 para a consulta e 0 para encerrar a execução. 

Ao escolher a opção 1, será executado o primeiro bloco do **switch..case**, onde iremos solicitar o código e o nome do novo produto, procedendo a inclusão dele no HashMap com o uso do método put. 

Se a opção escolhida for 2, solicitaremos o código do produto e buscaremos o nome dele no HashMap por meio do método **get**, o qual poderá retornar o nome, ou nulo no caso em que a chave não estiver presente nesse HashMap.

Podemos observar, a seguir, uma possível saída para esse programa.

![Saída do programa Exemplo022](/media/desenvolvimento_de_software_java/aula3/img06_saida_programa_exemplo22.png)

Os principais métodos do **HashMap ‹K,V›** são apresentados no quadro seguinte:

![Principais métodos de HashMap](/media/desenvolvimento_de_software_java/aula3/img07_metodos_hashmap.png)

Nós vimos aqui apenas os dois principais elementos do JCF, mas existem muitas outras classes disponíveis nessa biblioteca.

É interessante observar também que, como estruturas de dados, tais elementos podem ser combinados para criar, por exemplo, listas de mapas de listas.

`ArrayList‹ HashMap‹ Integer, ArrayList‹String› > >`

Esta estrutura de exemplo, um pouco mais complexa, permitiria guardar coleções de tabelas de mapeamento, onde cada mapeamento se refere a uma coleção.

### Reflexividade Computacional  

Podemos definir **reflexividade computacional** como a habilidade de um objeto conhecer a si próprio, sua estrutura e a utilização de seus métodos.

Na linguagem Java os objetos derivam direta ou indiretamente da classe `Object`, que seria a classe base de toda a plataforma. No entanto, existe outra classe chamada `Class`, que permite observar a estrutura de qualquer objeto por meio da reflexividade.

Não confundir a palavra reservada `class` (minúsculo) para definição de classes com a classe `Class` (maiúsculo) para gerência de classes.

Por meio de `Class` podemos obter informações acerca dos atributos da classe em objetos do tipo `Field` e de seus métodos por meio de objetos `Method` e `Parameter`.

Além de consultar as informações, podemos mudar o valor de atributos e invocar métodos com o uso destas classes.

Vamos observar um pequeno exemplo, com uma classe Pessoa definida de forma simples.

```java

package exemplo023; 

public class Pessoa { 
     public String nome; 
     public String telefone; 
 
     public void exibir(int quantidade){ 
          for(int i=0; i ‹ quantidade; i++) 
               System.out.println(nome+"::"+telefone); 
     } 
} 
```

```java
package exemplo023;
import java.lang.reflect.Field;

public class Exemplo023 {
     public static void main(String[] args) throws Exception { 
          Object objeto =
               Class.forName("exemplo023.Pessoa").newInstance();
          Class classe = objeto.getClass();
          // Reconhecendo os atributos do objeto...
          for(Field f: classe.getFields())
              System.out.println(f.getName()+"::"+f.getType());
          // Alterando os valores e invocando o método...
          classe.getField("nome").set(objeto,"João");
          classe.getField("telefone").set(objeto,"1111-1111");
          classe.getMethod("exibir", int.class).invoke(objeto, 2);
     }
}
```

Note que no exemplo o objeto da classe Pessoa é criado a partir de seu nome completo, incluindo o pacote, no formato texto, e que conseguimos extrair os atributos com objetos `Field`. Qualquer nome de classe que fosse utilizado iria funcionar e mostraria os atributos definidos no âmbito da classe.

Uma observação a ser feita é a de que o método `main` acrescenta `throws Exception` em sua assinatura. Isto é necessário porque o método **forName** pode gerar uma exceção caso não encontre o nome da classe passada como parâmetro no CLASSPATH.

Além de obter os dados acerca dos atributos, também alteramos os valores dos campos com o comando **set**. Abaixo, podemos observar uma linha com método **set** desdobrada para melhor compreensão.

```java
Field f = classe.getField("nome"); 
     // Captura o atributo nome da classe no Field f 
f.set(objeto, "João"); 
     // Utiliza o método set para alterar o valor em objeto. 
```

Finalmente, invocamos um método passando parâmetros para o mesmo com o uso do invoke. Novamente vamos desdobrar a linha para facilitar a compreensão.

```java
Method m = classe.getMethod("exibir", int.class); 
     // Captura a versão do método exibir que recebe um valor 
     // inteiro como parâmetro 
m.invoke(objeto,2); 
     // Invoca este método passando o valor 2 para o parâmetro. 
```

Podemos observar, a seguir, a saída esperada para a execução desse código:

![Saída do programa](/media/desenvolvimento_de_software_java/aula3/img08_saida_programa.png)

### Anotações

Por que falamos acerca de reflexividade computacional?

Certamente é um assunto complexo, mas necessário para compreender os fundamentos da criação e utilização de **anotações**.

As anotações são metadados anexados às classes que podem ser reconhecidos por ferramentas externas para as mais diversas finalidades. Atualmente, é comum seu uso em diversos frameworks, principalmente os de persistência de dados.

Sem a reflexividade computacional essas ferramentas não conseguiriam reconhecer tais anotações em meio ao código da classe.

Essa é uma modelagem comportamental que segue o caminho inverso das classes genéricas, pois nessas primeiras as classes são aplicadas ao comportamento, enquanto nas anotações iremos aplicar o comportamento às classes.

```java

package exemplo024; 
import java.lang.annotation.ElementType; 
import java.lang.annotation.Retention; 
import java.lang.annotation.RetentionPolicy; 
import java.lang.annotation.Target; 
 
@Retention(value=RetentionPolicy.RUNTIME) 
@Target(value=ElementType.TYPE) 
public @interface Autoria { 
    String autor(); 
    int ano(); 
    String empresa() default "UNESA"; 
} 
```

Para definir uma anotação precisamos utilizar o comando `@interface`, além de definir a utilização dela com `@Target`, e neste exemplo indica que a anotação será voltada para classes, mas que poderiam ser diversos outros tipos, como métodos e atributos, bem como o escopo de utilização com `@Retention`, colocado aqui como em tempo de execução.

Para essa anotação criamos três campos, sendo que dois são de preenchimento obrigatório e um opcional, no caso **empresa**, já que é definido um valor padrão com `default`.

Após criar nossa interface de anotação, podemos aplicá-la a uma classe.

```java
package exemplo024; 
@Autoria(autor = "Denis", ano = 2018) 
public class Carro { 
      // O código interno da classe não será criado 
}
```

Note que o uso da aplicação é bastante simples, assemelhando-se muito a um comentário, mas necessitando sempre do preenchimento de campos obrigatórios.

O passo final é o mais complexo, justamente por necessitar de elementos de reflexividade computacional, e trata do reconhecimento das anotações pelas ferramentas externas.

O processo demonstrado a seguir é o mesmo utilizado pelos frameworks na automatização de diversas atividades.

```java
package exemplo024; 
  public class Exemplo024 { 
     public static void main(String[] args) { 
      Object[] objetos = {new Carro(), "XPTO" }; 
      for(Object obj: objetos){ 
         Class c1 = obj.getClass(); 
         if(c1.isAnnotationPresent(Autoria.class)){ 
            Autoria a1 = 
                 (Autoria)c1.getAnnotation(Autoria.class); 
            System.out.println("Classe " + c1.getName() + 
                 " escrita por " + a1.autor() + " em " + 
                 a1.ano()); 
         } else { 
            System.out.println("Classe " + c1.getName() + 
               " sem autoria definida"); 
         }
      }
   }
}
```

Incialmente definimos um vetor de objetos, recebendo um `Carro` e uma `String`, e nesse caso apenas o Carro traz a anotação de **Autoria**.

Ao percorrer o vetor, para cada `Object` do mesmo iremos obter o `Class`, e em seguida perguntar se a anotação de Autoria está presente.

`if(c1.isAnnotationPresent(Autoria.class))`

Estando presente iremos capturar a anotação encontrada, sendo necessário uma conversão de tipo, já que o método retorna uma anotação de forma genérica.

```java
// Conversão de tipo com (Autoria)
Autoria a1 = (Autoria)c1.getAnnotation(Autoria.class); 
```

Com isso conseguimos imprimir os valores digitados para autor e ano, ou a mensagem de que a autoria não está definida quando a anotação não está presente.

Podemos observar a saída do programa a seguir:

```java
Classe exemplo024.Carro escrita por Denis em 2018 

Classe java.lang.String sem autoria definida 
```

## Aula 4 – Interfaces visuais para desktop

### GUI (Graphical User Interface)

Os primeiros computadores pessoais trabalhavam no modo texto, com comandos simples de entrada e saída para interação com vídeo e teclado e até mesmo jogos eram feitos com caracteres ASCII.

Os pesquisadores da Xerox foram pioneiros na criação de interfaces gráficas, definindo conceitos que persistem até os dias atuais, como janelas, menus, caixas de opção, caixas de seleção e ícones.

As empresas Apple e Microsoft seguiram as ideias definidas pela Xerox na criação de suas interfaces gráficas, sendo o **Macintosh** lançado em 1984, o qual se tornou o primeiro produto de sucesso a utilizar uma interface gráfica.

No caso da Microsoft, as interfaces gráficas inicialmente eram chamadas a partir do MS-DOS, recebendo o nome de **Windows**, e foi somente a partir de 1990, com a versão 3.0, que este sistema de janelas se popularizou.

Outras plataformas também passaram a disponibilizar ambientes baseados em janelas, como XWindow no UNIX e Linux, Workbench no Commodore Amiga, e GEM nos computadores Atari.

Qualquer que seja a GUI, ela deve utilizar um conjunto de tecnologias visando à criação de uma plataforma de interação com o usuário.

Em computadores pessoais, o conjunto padrão é denominado **WIMP** (window, icon, menu, pointer), ou seja, é um ambiente composto de janelas, ícones, menus e ponteiros. Nesse sistema, utiliza-se um dispositivo de ponteiro como o mouse para controlar a posição do cursor e apresentar informação organizada em janelas e representada por meio de ícones.

Em ambientes WIMP, os gerenciadores de janelas facilitam a interação entre as representações gráficas, aplicações e o sistema de gerenciamento de hardware. A sensação proporcionada por estes gerenciadores de janelas, incluindo a interação entre janelas e outros elementos gráficos, produz um ambiente denominado **desktop**.

### Bibliotecas gráficas do Java

O ambiente Java traz, por padrão, duas bibliotecas que objetivam a criação de sistemas baseados em janelas:

- **awt** (Abstract Window Toolkit),
  trata da API original do Java para GUI.

- **swing**, parte da JFC
  (Java Foundation Classes).

Existe também uma terceira biblioteca denominada **swt** (Standard Widget Toolkit), criada pela IBM e mantida pela Eclipse Foundation.

Nós utilizaremos a biblioteca **swing**, por ser padrão do ambiente Java e por definir o aspecto para os componentes visuais de forma independente, ao contrário do **awt**, que exibe os componentes de acordo com o aspecto proporcionado pela plataforma ou pelo sistema operacional.

Nas bibliotecas swing e awt temos componentes visuais como botões, campos de texto e listas, voltados para a interação com o usuário, e componentes chamados de contêineres, responsáveis por agrupar os componentes iniciais.

O principal contêiner é a janela, e dentro dela podemos ter botões e outros componentes visuais simples, bem como painéis, que podem agrupar outros componentes visuais e painéis de forma recursiva.

Para ajustar a forma como estes componentes serão dispostos sobre o contêiner, devemos utilizar os componentes de layout.

Vamos ilustrar este processo no exemplo seguinte.

```java

import java.awt.BorderLayout;
import java.awt.Button;
import java.awt.FlowLayout;
import java.awt.HeadlessException;
import javax.swing.JFrame;
import javax.swing.JPanel;


public class MinhaJanela extends JFrame{

  public MinhaJanela() throws HeadlessException {

    super("Apenas um teste");

    setLayout(new BorderLayout());

    setBounds(10, 10, 300, 200);

    JPanel jp = new JPanel(new FlowLayout());

    jp.add(new Button("OK"));

    jp.add(new Button("Cancela"));

    add(jp,"South");

  }


  public static void main(String[] args) {

    new MinhaJanela().setVisible(true);

  }

}
```

Neste exemplo nós criamos uma classe descendente de JFrame, que na prática seria uma janela, e efetuamos algumas configurações.

Inicialmente chamamos o construtor do pai com a passagem do título da janela, definimos o layout como BorderLayout (dividido em Norte, Sul, Leste, Oeste e Centro), e definimos a posição, altura e largura com uso de setBounds.

Em seguida foi criado um painel com layout sequencial (FLowLayout), sendo adicionados dois botões a este painel, o qual é finalmente adicionado à janela na posição Sul.

O resultado você confere na imagem.

![Resultado JFrame](/media/desenvolvimento_de_software_java/aula4/img01_jframe.png)

Podemos verificar alguns layouts disponíveis na tabela seguinte.

| Layout        | Descrição                                                                                                                                                   |
| ------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BorderLayout  | Aceita até cinco componentes, os quais devem ser posicionados em North, South, East, West e Center.                                                         |
| BoxLayout     | Coloca os componentes em uma linha ou coluna simples, podendo ser alinhados.                                                                                |
| CardLayout    | Controlado por uma lista drop-down, permite exibir painéis de componentes de forma alternada.                                                               |
| FlowLayout    | Apenas coloca os componentes sequencialmente em uma linha, mas serve como base aos painéis de CardLayout.                                                   |
| GridBagLayout | Extremamente sofisticado e complexo, divide o layout em um grid e depois permite mesclar células e adicionar espaços para o posicionamento dos componentes. |
| GridLayout    | Trabalha com um grid simples, e os componentes vão preenchendo sequencialmente os espaços definidos.                                                        |

O método **main** irá apenas **instanciar** um objeto de janela e torná-lo visível.

Além das janelas criadas com **JFrame** podemos definir caixas de diálogo com **JDialog**, e utilizar alguns diálogos padronizados com **JOptionPane**. Iremos utilizar os diálogos nas situações em que fazemos uma pergunta ao usuário, ou quando desejarmos informá-lo acerca de algo.

Até mesmo em sistemas de linha de comando podemos utilizar os diálogos, e o componente **JOptionPane** já traz boa parte das necessidades usuais de entrada de dados para um sistema deste tipo.

| Método            | Descrição                                           |
| ----------------- | --------------------------------------------------- |
| showConfirmDialog | Diálogo de confirmação no estilo “sim/não/cancela”. |
| showInputDialog   | Solicitação de dados ao usuário.                    |
| showMessageDialog | Exibe uma mensagem para o usuário.                  |
| showOptionDialog  | Unificação dos outros três tipos.                   |

Vamos observar um pequeno exemplo de utilização do JOptionPane.

```java

import javax.swing.JOptionPane;

public class ExemploOptionPane {

  public static void main(String[] args) {

    int a = new Integer(

    JOptionPane.showInputDialog("Primeiro Numero:"));

    int b = new Integer(

    JOptionPane.showInputDialog("Segundo Numero:"));

    int c = a + b;

    JOptionPane.showMessageDialog(null, "A soma será: "+c, "Soma",

    JOptionPane.INFORMATION_MESSAGE);

  }

}

```

A sequencia de execução resultará na exibição dos seguintes diálogos:

![Resultado Diálogos com JOptionPane](/media/desenvolvimento_de_software_java/aula4/img02_dialogos_exemplo_joptionpane.png)

Neste pequeno exemplo temos o uso do método `showInputDialog` para solicitar os valores ao usuário, os quais devem ser convertidos para inteiro, pois são recebidos como texto. Em seguida, efetuamos a soma dos números fornecidos e exibimos o resultado por meio do método `showMessageDialog`.

Note que o parâmetro `JOptionPane.INFORMATION_MESSAGE` fará com que apareça o ícone padrão de informação na caixa de diálogo, podendo ser utilizados também outros ícones.

| Método                          | Descrição                             |
| ------------------------------- | ------------------------------------- |
| JOptionPane.INFORMATION_MESSAGE | Informação comum.                     |
| JOptionPane.ERROR_MESSAGE       | Indicativo de erro.                   |
| JOptionPane.QUESTION_MESSAGE    | Interrogação, para efetuar perguntas. |
| JOptionPane.WARNING_MESSAGE     | Sinal de atenção ou alerta.           |

### Componentes visuais

A padronização de componentes nas diversas plataformas trouxe muitos benefícios em termos de aprendizagem para os usuários. Como as interfaces gráficas apresentam os mesmos conceitos visuais, a utilização de um novo sistema se torna intuitiva.

É importante que saibamos utilizar os diversos componentes visuais para a construção de nossas telas.

Toda biblioteca GUI apresenta componentes visuais padronizados, como:

- Botões: Interação com o usuário a partir da operação de clique do mouse.
- Caixas de texto: Digitação de valores pelo usuário.
- Elementos selecionáveis: Podem ser marcados ou desmarcados com o clique do mouse.
- Listas: Representação de conjuntos de dados, podendo ser retráteis ou não.
- Menus: Conjuntos de listas de ações agrupadas, localizados normalmente na parte superior da tela.

A figura seguinte mostra a maior parte destes componentes, segundo o aspecto visual proporcionado pela biblioteca swing.

![Componentes Swing](/media/desenvolvimento_de_software_java/aula4/img03_componentes_swing.png)

Podemos ver no quadro abaixo as informações acerca dos componentes swing expostos na figura, de acordo com a numeração adotada.

| Número | Componente    | Funcionalidade                                                                                             |
| ------ | ------------- | ---------------------------------------------------------------------------------------------------------- |
| 1      | JLabel        | Representa um texto estático, podendo aceitar imagens (icon).                                              |
| 2      | JTextField    | Campo de entrada de texto.                                                                                 |
| 3      | JButton       | Representa um botão tradicional.                                                                           |
| 4      | JToggleButton | É um botão selecionável, estilo on/off.                                                                    |
| 5      | JProgressBar  | Barra de progresso, muito utilizada para acompanhamento de tarefas demoradas.                              |
| 6      | JRadioButton  | Deve ser utilizado para opções mutuamente exclusivas, ou seja, quando apenas uma opção pode ser escolhida. |
| 7      | JCheckBox     | Utilizado para situações em que podemos escolher mais de uma opção.                                        |
| 8      | JTable        | Representação de dados de forma tabular, como em uma planilha.                                             |
| 9      | JTree         | Representação de dados em forma hierárquica (**árvore**).                                                  |
| 10     | JComboBox     | Conhecido como caixa de combinação, este componente é uma lista **drop-down** ou “retrátil”.               |
| 11     | JList         | Representa uma lista de valores.                                                                           |

Para utilizarmos estes diversos componentes deveremos saber como instanciá-los e agrupá-los de forma adequada em meio aos contêineres visuais. Alguns componentes irão exigir um modelo de programação mais robusto, particularmente aqueles que representam coleções de dados, como listas e árvores.

O exemplo seguinte demonstra a criação de uma janela com alguns dos componentes visuais.

```java

import java.awt.GridLayout;
import javax.swing.*;


public class JanelaSimples extends JDialog{

  private JTextField txt1;
  private JCheckBox chk1,chk2;
  private JRadioButton rb1, rb2;
  private JButton btn1, btn2;


  public JanelaSimples() {

    setLayout(new GridLayout(4,2));

    add(new JLabel("Nome"));

    add(txt1=new JTextField(10));

    // Campo de Texto com 10 posições

    add(new JLabel("Opções de Leitura"));

    JPanel jp1 = new JPanel(new GridLayout(2,1));

    jp1.add(chk1 = new JCheckBox("Revista Mensal"));

    jp1.add(chk2 = new JCheckBox("Versão Digital"));

    // Painel com as caixas de seleção

    add(jp1);

    add(new JLabel("Graduado"));

    JPanel jp2 = new JPanel(new GridLayout(2,1));

    jp2.add(rb1 = new JRadioButton("sim"));

    jp2.add(rb2 = new JRadioButton("não"));

    // Painel com os botões de rádio

    bp.add(rb1);

    bp.add(rb2);

    // // Agrupamento dos botões de rádio

    add(jp2);

    add(btn1 = new JButton("OK"));

    add(btn2 = new JButton("Cancela"));

  }



  public static void main(String[] args) {

    JanelaSimples j1 = new JanelaSimples();

    j1.setModal(true);

    j1.setBounds(0,0, 300, 300);

    j1.setVisible(true);

  }

}
```

Neste exemplo nós criamos uma janela a partir de JDialog, organizando o posicionamento dos componentes com um GridLayout de 4 linhas por 2 colunas.

```java

setLayout(new GridLayout(4,2));

```

![Exemplo Grid](/media/desenvolvimento_de_software_java/aula4/img04_exemplo_grid.png)

Em seguida, começamos a adicionar os componentes ao grid, preenchendo sequencialmente as posições, ou seja, os componentes vão sendo adicionados na primeira linha, e quando não há mais espaço vai para a linha seguinte, repetindo-se o processo sucessivamente.

Nos momentos em que precisamos adicionar mais de um componente em uma mesma célula, como no caso das caixas de seleção e dos botões de rádio, utilizamos JPanel com organização via GridLayout de 2 linhas por 1 coluna. Os componentes são adicionados ao JPanel, e este é adicionado ao JDialog.

```java

JPanel jp1 = new JPanel(new GridLayout(2,1)); 

jp1.add(chk1 = new JCheckBox("Revista Mensal")); 

jp1.add(chk2 = new JCheckBox("Versão Digital")); 

// Painel com as caixas de seleção 

add(jp1); 
```

Por fim, os botões de rádio se tornam mutuamente exclusivos apenas se estiverem pertencendo ao mesmo grupo, e por isso precisamos criar um ButtonGroup e adicionar os botões de rádio.

```java

ButtonGroup bp = new ButtonGroup(); 

bp.add(rb1); 

bp.add(rb2); 
```

A chamada para a nova janela é feita no método main, ao instanciarmos um objeto do tipo JanelaSimples, definirmos seu posicionamento e suas dimensões, e deixá-lo visível. Embora não tenha influência agora, setar como modal significa que ficará em frente à janela chamadora, em um ambiente de múltiplas janelas, evitando perder o foco.

```java

JanelaSimples j1 = new JanelaSimples(); 

j1.setModal(true); 

j1.setBounds(0,0, 300, 300); 

j1.setVisible(true); 
```

Note que alguns dos componentes ficaram com dimensões um pouco estranhas, algo que pode ser corrigido com um pouco mais de código, mas como o NetBeans permite alterar visualmente este tipo de configuração, seria desnecessário aumentar a complexidade.

### Utilização de eventos

Agora que já conseguimos criar o design de nosso sistema, devemos nos preocupar com a interatividade dele, e nesse ponto precisaremos entender o conceito e uso de eventos.

Podemos definir evento como uma ação predeterminada que, ao ocorrer, permite iniciar uma ação personalizada, o que certamente será feito através de programação.

Cada linguagem apresenta sua própria versão de resposta a eventos, e no Java utilizamos a implementação de interfaces “ouvintes” para responder aos eventos.

Como existem diversos tipos de eventos disponíveis, devemos nos preocupar apenas com o ouvinte, ou listener, adequado à ação que esperamos do usuário.

| Listener            | Métodos                                                          | Parâmetro   |
| ------------------- | ---------------------------------------------------------------- | ----------- |
| ActionListener      | actionPerformed                                                  | ActionEvent |
| FocusListener       | focusGained focusLost                                            | FocusEvent  |
| KeyListener         | keyPressed keyReleased keyTyped                                  | KeyEvent    |
| MouseListener       | mouseClicked mouseEntered mouseExited mousePressed mouseReleased | MouseEvent  |
| MouseMotionListener | mouseDragged mouseMoved                                          | MouseEvent  |
| TextListener        | textValueChanged                                                 | TextEvent   |

Inicialmente devemos implementar a interface ouvinte desejada na janela, para permitir que os componentes possam adotá-la como ouvinte.

Vamos entender melhor com o seguinte exemplo:

Vamos considerar uma janela com dois campos de texto e um botão, como no fragmento de código seguinte.

```java

public class JanelaSoma extends JFrame { 

private JTextField txt1, txt2; 

private JButton btn1; 

```

Nós podemos implementar uma funcionalidade na qual o clique sobre o botão irá efetuar a soma dos valores digitados nos dois campos de texto, e apresentar esta soma através de um **JOptionPane**.

```java

public class JanelaSoma extends JFrame implements ActionListener{ 

@Override 

public void actionPerformed(ActionEvent e) { 

Integer i1 = new Integer(txt1.getText()); 

Integer i2 = new Integer(txt2.getText()); 

JOptionPane.showMessageDialog(this, "A soma será "+(i1+i2)); 

} 

```

Note que nossa janela agora implementa a interface **ActionListener**, e o processo é desenvolvido no método **actionPerformed**. Inicialmente são definidos os valores dos inteiros **i1** e **i2** a partir dos textos de **txt1** e **txt2**, e a seguir apresentamos o **JOptionPane** com a soma dos dois.

Agora só falta definir o construtor da janela e atrelar o botão que receberá o clique com o método de resposta por meio de **addActionListener**.

```java

public JanelaSoma() throws HeadlessException { 

  setLayout(new FlowLayout()); 

  add(txt1=new JTextField(5)); 

  add(txt2=new JTextField(5)); 

  add(btn1=new JButton("Somar")); 

  btn1.addActionListener(this); 

}
```

 Podemos observar, a seguir, o código completo da janela e o seu aspecto executando.

```java

import java.awt.FlowLayout; 
import java.awt.HeadlessException; 
import java.awt.event.ActionEvent; 
import java.awt.event.ActionListener; 
import javax.swing.JButton; 
import javax.swing.JFrame; 
import javax.swing.JOptionPane; 
import javax.swing.JTextField; 


public class JanelaSoma extends JFrame implements ActionListener{ 
 

  @Override 
  public void actionPerformed(ActionEvent e) { 

    Integer i1 = new Integer(txt1.getText()); 
    Integer i2 = new Integer(txt2.getText()); 
    JOptionPane.showMessageDialog(this, "A soma será "+(i1+i2)); 
  
  }

  private JTextField txt1, txt2; 
  private JButton btn1; 

  public JanelaSoma() throws HeadlessException { 

    setLayout(new FlowLayout()); 
    add(txt1=new JTextField(5)); 
    add(txt2=new JTextField(5)); 
    add(btn1=new JButton("Somar")); 
    btn1.addActionListener(this); 
  
  } 

  public static void main(String[] args) { 

    JanelaSoma j1 = new JanelaSoma(); 
    j1.setBounds(0,0, 300, 100); 
    j1.setVisible(true); 

  } 

} 

```

![Resultado Programa JanelaSoma](/media/desenvolvimento_de_software_java/aula4/img05_janela_soma.png)

Uma alternativa a esta forma de trabalho seria criar a resposta localmente e associar direto ao botão, retirando a necessidade da implementação do Listener pelo JFrame.

```java

btn1.addActionListener(new ActionListener() { 

  public void actionPerformed(ActionEvent e) { 

    Integer i1 = new Integer(txt1.getText()); 

    Integer i2 = new Integer(txt2.getText()); 

    JOptionPane.showMessageDialog(JanelaSoma.this, "A soma será "+(i1+i2)); 

  } 

}); 
```

Esta segunda forma é muito utilizada por permitir um objeto de resposta a cada componente, ao invés de tratar todos os eventos daquele determinado tipo em um mesmo método.

### Criação de janelas no NetBeans


Além do editor de código com **syntax highlighting**, que até aqui simplificou muito a nossa tarefa de programar, com a identificação dos diversos tipos de comandos e estruturas por meio de cores, e da complementação automática de código, entre outras ferramentas de auxílio à codificação, o NetBeans traz um ambiente excelente para a criação visual de janelas **swing** e **awt**.

Utilizando este ambiente, e entendendo algumas pequenas mudanças no estilo de código, passaremos a nos preocupar apenas com a codificação das regras de negócio e resposta a eventos em nossos sistemas.

Toda a extensa área de código reservada à criação e configuração dos componentes visuais será gerada automaticamente a partir das ações efetuadas no ambiente visual de criação, o que trará grande produtividade ao programador Java para desktop.

De início devemos compreender as ferramentas disponíveis, e o NetBeans apresenta:

- Editor visual de janelas;
- Paleta de componentes **swing** e **awt**;
- Editor de propriedades;
- Visualização hierárquica dos componentes; e
- Integração direta com o editor de código Java.

Para acrescentar uma janela do tipo JFrame ao nosso projeto devemos utilizar a opção de menu **Novo Arquivo** (CTRL + N), selecionar **Forms GUI Swing..Form JFrame** na janela que se abrirá e clicar em **Próximo**.

Na tela seguinte devemos dar um **nome** (Somadora) para nosso JFrame, escolher o **pacote** e clicar em **Finalizar**.

Estes passos podem ser observados nas duas figuras seguintes.

![Criando uma GUI](/media/desenvolvimento_de_software_java/aula4/img06_criando_gui.png)

Ao finalizar a criação de nosso **JFrame**, o ambiente de edição visual será aberto, e poderemos começar a criar nossa tela com simples operações de clique e arraste.

Teremos ao centro o **editor visual**, e do lado direito a **paleta de componentes**. Estes componentes podem ser arrastados da paleta para a tela do editor, e depois de posicionados serem configurados no painel de propriedades, que estará também à direita, porém, oculto até que seja selecionada a instância de componente.

As duas figuras seguintes mostram o momento inicial, onde um componente é arrastado para a tela, e o segundo passo, onde suas propriedades são observadas. Para abrir o painel de propriedades devemos clicar na instância, de forma a selecioná-la, e clicar na aba do painel para que ele se expanda.

![Editor visual e Paleta de componentes](/media/desenvolvimento_de_software_java/aula4/img07_paleta_componentes.png)

Com isso já podemos criar a nossa janela de forma visual. Iremos precisar de dois componentes **Label**, dois componentes do tipo **Campo de Texto** e um **Botão**.

Eles devem ser posicionados no editor visual, de forma a obter o aspecto da imagem ao lado.

Em seguida devemos renomear os componentes e configurar a propriedade **text**.

![Resultado JFrame](/media/desenvolvimento_de_software_java/aula4/img08_resultado_jframe.png)

O quadro seguinte mostra as mudanças.

| Nome Original | Novo Nome   | Valor de text               |
| ------------- | ----------- | --------------------------- |
| jLabel1       | lblParcela1 | Parcela 1                   |
| jLabel2       | lblParcela2 | Parcela 2                   |
| jTextField1   | txtParcela1 | (vazia – apagar o conteúdo) |
| jTextField2   | txtParcela2 | (vazia – apagar o conteúdo) |
| jButton1      | btnSomar    | Somar                       |

Efetuadas as alterações, a hierarquia da tela poderá ser conferida pelo navegador, posicionado no canto inferior esquerdo do ambiente, e a tela estará preparada para a fase de programação.

![Hierarquia de componentes](/media/desenvolvimento_de_software_java/aula4/img09_hierarquia.png)

O objetivo da tela será exibir a soma dos valores digitados quando ocorrer o clique sobre o botão. Para tal devemos responder ao evento através do método **actionPerformed**. Porém, no ambiente visual isto é um pouco diferente.

Clique com o botão direito do mouse sobre btnSomar e, sobre o menu de contexto que aparecerá, escolha **Eventos..Action..actionPerformed**.

Será aberto um método denominado btnSomarActionPerformed, no qual deverá ficar a programação do evento. Note que existem trechos com fundo cinza que não permitem alteração no código, e que a janela mudou da aba **Projeto** para **Código-Fonte**.

Estas abas ficam na parte superior do editor visual, e permitem intercambiar entre o código Java e o desenho da janela. 

![Menu Action Performed](/media/desenvolvimento_de_software_java/aula4/img10_action_performed.png)


Agora, tudo que precisamos fazer é programar o que foi planejado no método gerado de forma automática.

```java

private void btnSomarActionPerformed(java.awt.event.ActionEvent evt){  

  Integer i1 = new Integer(txtParcela1.getText()); 

  Integer i2 = new Integer(txtParcela2.getText()); 

  JOptionPane.showMessageDialog(this,"A soma será: "+(i1+i2)); 

} 
```

Pronto! Agora é só executar o arquivo com `SHIFT+F6`.

Note como a programação, com uso deste ambiente de criação visual, é bem mais simples. Porém, essa simplicidade implica em um código final muito maior.

Se tiver a curiosidade de observar todo o código protegido (com fundo cinza), inclusive os códigos ocultos, que podem ser abertos clicando no sinal de “+” no lado esquerdo do editor, poderá observar a real complexidade do código completo.

Mesmo com um código-fonte bem maior, o que é fruto da generalização necessária, o uso desta ferramenta trará grande produtividade para qualquer programador Java desktop.

## Aula 5 – Interfaces visuais para web

### Linguagem HTML5

Como nas versões iniciais, o HTML 5 é uma linguagem de marcação baseada em etiquetas (tags) que devem controlar diversos aspectos do texto. Nas versões iniciais do HTML ocorria o controle tipográfico e estrutural, mas no HTML 5 a preocupação é apenas estrutural, sendo delegado ao CSS (Cascade Style Sheet) o controle de características tipográficas.

### Sintaxe do HTML5

Como o HTML na versão 5 segue o padrão de escrita do XML, a primeira linha deve definir o tipo de documento.

![Tag HTML](/media/desenvolvimento_de_software_java/aula5/img00001.png)

Em seguida, definimos o documento HTML, dividindo-o nas seções de cabeçalho e corpo. 

No cabeçalho ficam informações de configuração e pré-carga, enquanto no corpo será colocada a parte visual da página.

![HTML Cabeçalho](/media/desenvolvimento_de_software_java/aula5/img00002.png)

Nesse fragmento de código, podemos observar a inserção do título de uma página com o uso de `<title>` e a escolha da acentuação utilizada através de `<meta/>`.

Diversas tags aceitam a definição de atributos específicos, como `<meta charset="UTF-8"/>`, e tais atributos devem ter seus valores inseridos entre aspas ou apóstrofes. Essa é apenas uma das diversas características controladas com o uso de `<meta/>`.

As tags mais comuns na seção de cabeçalho são resumidas a seguir.

| Tag        | Utilização                                                                                                                              |
| ---------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| `<title>` | Define o título da página, normalmente apresentado no topo da janela.                                                                   |
| `<meta>`   | Permite a inclusão de informações e controle de características do documento, como o uso de UTF-8 para acentuação da língua portuguesa. |
| `<link>`   | Efetua a ligação da página com um recurso externo, como folha de estilo CSS ou biblioteca JavaScript.                                   |
| `<style>`  | Define uma folha de estilo interna para a página.                                                                                       |

Na parte do corpo ficam os elementos estruturais constituintes da parte visual. É onde será definido o conteúdo, que pode ser estruturado em termos de títulos, parágrafos, listas, tabelas e diversos outros elementos que promoverão a organização visual do texto da página.

![HTML com pequena lista](/media/desenvolvimento_de_software_java/aula5/img00004.png)

Nesse fragmento de código, referente ao corpo da página, podemos observar a tag `<p>` para a definição de um parágrafo, e a construção de uma lista com `<ul>` e `<li>`.

A lista é iniciada e finalizada com `<ul>` e cada elemento é inserido em um conjunto `<li>`.

Essas tags criarão um efeito visual como o que pode ser observado a seguir:

![HTML pequena lista renderizado na página](/media/desenvolvimento_de_software_java/aula5/img00005.png)

A sintaxe HTML traz diversas tags estruturantes para o conteúdo do body, até mesmo por ser uma linguagem de hipermídia, onde é comum a criação de listas, camadas e até tabelas (estas últimas apenas para dados tabulares, segundo recomendações atuais).

Podemos observar algumas das tags estruturais a seguir:

| Tag                                              | Utilização                                                                                                                           |
| ------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `<h1>` `<h2>` `<h3>` `<h4>` `<h5>` `<h6>` `<h7>` | Definem elementos de texto utilizados como títulos em diferentes tamanhos de fonte, sendo `<h1>` para o maior e `<h7>` para o menor. |
| `<b>` `<i>` `<u>` `<em>` `<strong>`              | Negrito, itálico e outros efeitos de texto. São consideradas obsoletas, sendo recomendado o uso de folhas de estilo CSS.             |
| `<p>` `<div>`                                    | Definem trechos de texto, sendo que `<p>` ressalta o parágrafo e `<div>` é muito utilizado para a criação de camadas.                |
| `<ul>` `<ol>`                                    | Iniciam a criação de listas de elementos, sendo numeradas com `<ol>`.                                                                |
| `<li>`                                           | Define um item de lista.                                                                                                             |
| `<hr/>`                                          | Quebra de linha.                                                                                                                     |
| `<table>` `<tr>` `<td>`                          | Utilizadas para a criação de tabelas. Hoje em dia seu uso é recomendado apenas para dados tabulares.                                 |
| `<span>`                                         | Define um trecho avulso, ao qual podem ser aplicadas formatações.                                                                    |


Uma funcionalidade essencial das páginas HTML é a possibilidade de **navegar** entre páginas de um site ou entre sites, permitindo acessar os mais diversos recursos ao longo da Web, identificados de forma única através de sua **URL** (Universal Resource Locator).

Criaremos hiperlinks para efetuar essa navegação, sendo utilizada a tag `<a>`, ou âncora (do inglês **anchor**), sempre apontando para alguma **URL** e apresentando um texto que representa o recurso. Quando o usuário clica sobre o texto é redirecionado para o recurso.

![HTML Anchor](/media/desenvolvimento_de_software_java/aula5/img00006.png)

Com o uso conjunto de todos esses elementos, seremos capazes de criar nossas páginas, podendo tratar de simples páginas, ainda sem elementos dinâmicos e formatações adequadas, mas com toda a parte estrutural definida.

Podemos observar uma página completa a seguir:

```html

<!DOCTYPE html> 

<html> 
  <head> 
    <title>Página de Exemplo </title> 
    <meta charset="UTF-8"/> 
  </head> 

  <body> 

    <h1>Alguns links úteis <h1> 

    <ul> 

      <l1> <a href="//www.mpf.mp.br/">Ministério Público Federal</a> </l1> 

      <l1> <a href="//www.pf.gov.br/">Polícia Federal</a> </l1> 

      <l1> <a href="//portal.stf.jus.br">Superior Tribunal Federal</a> </l1> 

    <ul> 

  </body> 

</html> 
```

![HTML da Página de Exemplo renderizado](/media/desenvolvimento_de_software_java/aula5/img00007.png)

Temos uma lista onde cada item corresponde a determinado hiperlink para algum site, além de trazer um título e uma definição para acentuação.

Como citado anteriormente, precisamos utilizar as tags `<ul>` e `<l1>` em conjunto, sendo que a primeira determina o início e final da lista, enquanto a segunda determina os itens que farão parte dessa lista.

### CSS

A metodologia de criação de sites atualmente aceita, prioriza a divisão da página em termos de estrutura e formatação, ficando a estrutura a cargo do HTML e a formatação efetuada via folhas de estilo CSS (Cascade Style Sheets).

Com essa regra definida, nosso próximo passo é configurar os elementos tipográficos e o aspecto visual da página com o uso do CSS.

Vamos modificar o exemplo anterior, aplicando uma formatação através de folhas de estilo:

**Exemplo 3 **

```html

<!DOCTYPE html> 

<html> 

  <head> 

    <title>Página de Exemplo </title> 

    <meta charset="UTF-8"/> 

    <style> 

      h1 {color: orange} 

      a {color: yellow} 

      a:hover {color: red} 

      body {background-color: #000032; color:yellow} 

    </style> 

  </head> 

  <body> 

    <h1>Alguns links úteis<h1> 

    <ul> 

      <l1> <a href="//www.mpf.mp.br/">Ministério Público Federal</a> </l1> 

      <l1> <a href="//www.pf.gov.br/">Polícia Federal</a> </l1> 

      <l1> <a href="//portal.stf.jus.br">Superior Tribunal Federal</a> </l1> 

    <ul> 

  </body> 

</html> 
```

![HTML da Página de Exemplo renderizado](/media/desenvolvimento_de_software_java/aula5/img00008.png)

Observe como o acréscimo da tag `<style>` com as formatações adequadas trouxe enorme diferença para o aspecto visual da página.

A sintaxe geral do CSS pode ser definida como:

![HTML da Página de Exemplo renderizado](/media/desenvolvimento_de_software_java/aula5/img00009.png)

Iniciamos com o seletor e, entre as chaves, definimos os vários elementos de formatação como fontes e cores, alinhamentos, figuras de fundo, entre vários outros, sempre seguindo a sintaxe propriedade: valor.

No exemplo anterior, a tag `<h1>` foi formatada com a fonte de cor laranja, enquanto `<body>` recebe fundo de tonalidade azul (RGB=#000032) e fonte amarela.

O conjunto de seletores a e a:hover traz um comportamento bem interessante. O primeiro define a formatação do link no modo normal e o segundo define a formatação quando o mouse passa sobre o mesmo.

Além de formatar as tags, é possível utilizar classes e identificadores como seletores do CSS, bastando colocar o sinal de hash na frente dos identificadores e ponto na frente das classes.

A questão maior é quando devemos utilizar identificadores ou classes. Os identificadores são utilizados em elementos que não se repetem, como camadas, e as classes são utilizadas para utilizar a mesma formatação em diversos pontos da página.

Podemos observar esses seletores mais adiante:

```html

<!DOCTYPE html> 

<html> 

  <head> 

    <title>Exemplo de Camadas</title> 

    <meta charset="UTF-8"/> 

    <style> 

      #C1 {position:absolute; top:10px; left:10px; width:300px; height:200px; background-color:lightblue} 

      #C2 {position:absolute; top:50px; left:50px; width:220px; height:120px; background-color:blue; color:yellow} 

      .destaque {background-color:black; color:orange} 

    </style> 

  </head> 

  <body> 

    <div id="C1">Camada 1 com algum <span class="destaque">texto ressaltado</span> </div> 

    <div id="C2">Camada 2, e agora o<span class="destaque">texto ressaltado</span> está aqui </div> 

  </body> 

</html> 

```

![HTML da Página de Exemplo renderizado](/media/desenvolvimento_de_software_java/aula5/img00010.png)

Aqui nós utilizamos o CSS para definir o posicionamento, o tamanho e as cores de duas camadas, identificadas como C1 e C2 a partir do atributo id da `<div>`, e com o uso de `<span>` e o atributo class aplicamos a formatação específica para alguns fragmentos de texto.

### JavaScript

A linguagem JavaScript nem sempre teve esse nome. Desenvolvida originalmente pela Netscape, ela se chamava Mocha, e teve o nome modificado posteriormente para LiveScript, quando ocorreu seu lançamento junto ao navegador Netscape 2.0 versão beta, em setembro de 1995.

Em dezembro de 1995, em um anúncio conjunto com a Sun Microsystems, é lançado o Netscape 2.0B3, com suporte à tecnologia de Applets. O nome da linguagem foi modificado para JavaScript, o que causa muita confusão até hoje com relação à sua relação com a linguagem Java.

É importante que tenhamos em mente que JavaScript não é Java, e a similaridade entre as duas linguagens ocorre apenas pelo fato de ambas utilizarem sintaxes baseadas na linguagem C.

Utilizamos o JavaScript para controle de elementos da página HTML e viabilização da interatividade, caracterizando-se originalmente como uma tecnologia cliente. Pode ser embebida na própria página, ou organizada no formato de biblioteca, como arquivo externo.

Recentemente, o JavaScript passou a ser utilizado também do lado servidor, através de tecnologias como o node.js.

Outro ambiente que recebeu a possibilidade de desenvolvimento com JavaScript foi o dos dispositivos móveis, com uso de ferramentas como Ionic.

#### Sintaxe do JavaScript

Inicialmente, devemos compreender a declaração de variáveis e operações aritméticas da linguagem.

Uma variável pode ser declarada com o uso de var, ou simplesmente com sua inicialização. Como o JavaScript não é fortemente tipado, a variável assume o tipo do valor associado a ela.

Os tipos com os quais a linguagem trabalha são: inteiro, ponto flutuante, booleano, texto, objeto e vetor (como objeto da classe Array).

Os operadores matemáticos são os mesmos utilizados pelo Java; afinal, ambas as linguagens derivaram do C, mas com pequenas diferenças: enquanto no Java a divisão entre inteiros resulta em um número inteiro, no JavaScript não temos como diferenciar um inteiro de um real, e por isso a divisão poderá retornar um número real.

**Exemplo 5**

```html

<!DOCTYPE html> 

<html> 

  <script> 

    var a = 5, b = 32, c = 7; 

    document.writeln("<br/>A:"+a+" B:"+b+" C:"+c); 

    b = b - (c * 2); 

    b /= a; 

    document.writeln("<br/>A:"+a+" B:"+b+" C:"+c); 

    b++; 

    document.writeln("<br/>A:"+a+" B:"+b+" C:"+c); 

  <script> 


</html>  

```

![HTML da Página de Exemplo renderizado](/media/desenvolvimento_de_software_java/aula5/img00011.png)

Aqui são declaradas três variáveis com o uso de var, sendo efetuadas algumas operações aritméticas sobre as mesmas.

A cada passo é impresso na página o valor das variáveis através de `document.writeln`. É interessante observar que esse comando escreve sobre a página HTML, permitindo a inclusão de tags, como o uso de `<br/>` para quebra de linha.

Se estivéssemos efetuando essas mesmas operações em Java, para variáveis inteiras, o resultado de B na segunda linha seria 3, e não 3.6, como ocorre no JavaScript.

Assim como os operadores aritméticos do JavaScript são similares aos do Java, os relacionais e lógicos também são, e podemos utilizá-los da mesma forma nas duas linguagens, apenas observando o fato de que o JavaScript não é fortemente tipado.

Uma observação a ser feita é que a comparação entre Strings é muito diferente entre as duas linguagens. Enquanto Java necessita do uso de equals, o JavaScript utiliza o operador para comparação de igualdade.

| Java                                               | JavaScript                                      |
| -------------------------------------------------- | ----------------------------------------------- |
| String a; <br/> boolean b;                         | var a,b;                                        |
| // Operações sobre a <br/> b = (a.equals("XPTO")); | // Operações sobre a <br />  b = (a == "XPTO"); |

#### Estruturas de decisão e de repetição

A similaridade entre Java e JavaScript não fica apenas na definição dos operadores, mas também na utilização da mesma sintaxe para as estruturas de decisão e de repetição.

É claro que os métodos de entrada e saída de dados são completamente diferentes, até mesmo pela finalidade de cada uma das linguagens. No caso do JavaScript, toda entrada e saída deve ocorrer a partir do navegador.

Vamos observar um exemplo com uso de if:

**Exemplo 6** 

```html

<!DOCTYPE html> 

<html> 

  <body> 

    <script> 

      var x = eval(prompt("Entre com o valor:","")); 

      if(x > 5) 

        document.writeln("<h1>Valor maior que 5</h1>"); 

      else 

        document.writeln("<h1>Valor menor ou igual a 5</h1>" 

    </script> 

  </body> 

</html>  
```

![Javascript estrutura de decisão](/media/desenvolvimento_de_software_java/aula5/img00012.png)

A função prompt serve para solicitar ao usuário a digitação de um valor a partir de um diálogo de entrada, enquanto a função **eval** efetua a conversão de String para número.

Em nosso exemplo, a variável x recebe o valor digitado pelo usuário com o uso da função prompt, mas com o valor, que era originalmente texto, convertido para número com o uso de eval.

De acordo com o valor digitado a página irá apresentar uma das alternativas de frase, ambas formatadas pela tag `<h1>`, sendo a escolha da frase a ser apresentada controlada pela estrutura **if..else**, segundo a condição **x < 5**.

Agora temos um exemplo com uso de for, que imprime os números primos de 1 a 50:

**Exemplo 7** 

```html

<!DOCTYPE html> 

<html> 

  <body> 

    <ul> 

      <script> 

        for(i=1 ; i<=50 ; i++){ 

          primo = true; 

          for (j=2 ; j<i ; j++) 
            if ( i % j == 0 ){ 
              primo = false; 
              break; 
            } 

          if(primo)
            document.writeln("<li>"+i+"</li>"); 

        } 

      </script> 

    </ul> 

  </body> 

</html>  
```

![Javascript estrutura de decisão](/media/desenvolvimento_de_software_java/aula5/img00013.png)

Observe que cada frase é iniciada com `<li>` e terminada com `</li>`, o que faz com que sejam transformadas em uma lista iniciada imediatamente antes do script com a tag `<ul>`.

Nesse código, utilizamos um `for` executando de 1 a 50, e dentro utilizamos outro for para dizer se é primo, segundo a regra de que se i for divisível por algum número entre 2 e i-1 ele não é primo.

Tendo verificado que o número não é primo, não é necessário testar outras divisões, o que justifica o uso de `break` para sair do loop interno.

Finalmente, um exemplo com utilização da estrutura `while`:

**Exemplo 8**

```html

<!DOCTYPE html> 

<html> 
  <body> 
    <table border="1" width="100%"> 
      <tr> 
        <td> 
          A 
        </td> 
        <td> 
          Fatorial(A) 
        </td> 
      </tr> 

      <script> 
        var a = 1; 
        while(a<10){ 
          document.writeln("<tr><td>"+a+"</td>"); 
          fat = b = a; 
          while(--b>=1){ 
            fat *= b; 
            document.writeln("<td>"+a+"</td></tr>"); 
            a++; 
          } 
      </script> 

    </table> 

  </body> 

  </html> 
```

![HTML Exemplo 08 renderizado](/media/desenvolvimento_de_software_java/aula5/img00014.png)

Aqui nós imprimimos o fatorial de cada número entre 1 e 9. Para tal, utilizamos um controle **while** externo, aumentando o valor de a enquanto não atingir o valor 10, e internamente efetuamos o cálculo do fatorial com outro bloco **while**.

![fatorial ](/media/desenvolvimento_de_software_java/aula5/img00015.png)

Nas linhas acima, podemos observar que os valores de `fat` e `b` são ambos inicializados com o valor atual de `a`. Em seguida ocorre um loop onde `b` é decrementado e já testado se o valor é maior que **1**; se for maior, o valor de `fat` é multiplicado por `b` naquela rodada.

Esse processo apenas segue a forma natural de cálculo de fatorial. Se a vale 4, então `4! = 4 * 3 * 2 * 1`. Se observarmos a expressão, podemos dizer que começa com o valor de a (4) e multiplica por todos os menores que 4 até chegar a 1.

### Funções e evento

As funções, assim como os métodos em ambientes orientados a objetos, correspondem a ações ou processos, que são nomeados, e que podem ou não receber parâmetros e retornar valores.

Nós criamos funções no JavaScript com o uso de `function`, os parâmetros não são tipados, e elas podem retornar um resultado para o chamador com uso de `return`.

![javascript function exemplo](/media/desenvolvimento_de_software_java/aula5/img00016.png)

Quanto ao conceito de eventos, é o mesmo utilizado nos ambientes desktop, ou seja, um conjunto de ações predeterminadas para as quais podemos dar uma resposta programada ao chamador.

Nesse caso, o modelo de resposta parte dos atributos de evento existentes nas tags HTML sendo relacionados com funções em JavaScript. Esse modelo é bem simples, e permite grande flexibilidade.

Observe este exemplo de tratamento de eventos:

**Exemplo 9**

```html

<!DOCTYPE html> 
<html> 

  <head> 
    <meta charset="UTF-8"/> 
  </head> 

  <body> 

    <button onclick="mostraMensagem()">Clique Aqui </button> 

    <script> 
      function mostraMensagem(){ 
        alert("OLA MUNDO"); 
      } 
    </script> 

  </body> 
</html> 
```

A página contém apenas um botão. Ao clicar sobre ele, a mensagem “OLA MUNDO” aparecerá em um **alert**.

Podemos observar a associação do evento de clique com a função de tratamento na seguinte linha:


![javascript button onclick](/media/desenvolvimento_de_software_java/aula5/img00017.png)

#### Formulários

Quando efetuamos o cadastro em algum site de compras pela Web, o que estamos efetuando é o preenchimento de um formulário HTML. Essas informações são enviadas para o servidor de duas formas, denominadas “métodos”:

- GET: Os dados são enviados através da própria URL.

- POST: Os dados são enviados em background.

Todo formulário é iniciado com a tag `<form>`, que terá como principais atributos o método de envio (method) e o destino para a informação (action).

Dentro do formulário, podemos incluir os componentes de entrada de dados, como caixas de texto, botões de rádio, caixas de marcação, entre outros. A grande maioria é definida através da tag `<input>`, cujos atributos principais são type, referente ao tipo de componente, name, utilizado para identificação do dado na chegada ao servidor, e value, para identificar o valor preenchido.

Os tipos que a tag `<input>` pode utilizar são explicados na tabela seguinte.

| Tipo     | Utilização                                                                                                                                                                                |
| -------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| text     | Cria uma caixa de texto, podendo ter um valor inicial definido através de value.                                                                                                          |
| hidden   | Quando queremos guardar um valor para envio, mas sem ficar visível.                                                                                                                       |
| radio    | Opções mutuamente exclusivas. Quando marcamos um, todos com o mesmo atributo name serão desmarcados. O que ficar marcado, ao final, enviará seu atributo value como dado para o servidor. |
| checkbox | Quando queremos a possibilidade de marcar várias opções. Todos que forem marcados enviarão seus atributos value como dados para o servidor.                                               |
| submit   | Cria um botão de envio para o formulário.                                                                                                                                                 |
| reset    | Cria um botão que reinicia (limpa) o formulário.                                                                                                                                          |

Podemos observar, a seguir, um formulário simples, com o uso das tags `<form>` e `<input>`.

**Exemplo 10**

```html 
<!DOCTYPE html> 
<html> 
  <head> 
    <title>Exemplo de Formulário</title> 
    <meta charset="UTF-8"/> 
    <style> 
      body {background-color:blue; color:white; font-style: bold} 
    </style> 
  </head> 

  <body> 
    <form action="//servidor/app.asmx" method="get"> 

      Nome:<input name="N1" type="text"/><br/><br/> 

      Opções de Envio: <br/> 
      <input type="checkbox" name="OPT" value="Revista"/> 
      Revista Mensal 
      
      <input type="checkbox" name="OPT" value="Digital"/> 
      Versão Digital 
      
      <input type="checkbox" name="OPT" value="SMS"/> 
      Mensagens SMS<br/><br/> 
      
      <input type="submit" value="Cadastrar"/> 

    </form> 
  </body> 

</html> 
```

![HTML Exemplo 10 renderizado](/media/desenvolvimento_de_software_java/aula5/img00018.png)

Nesse exemplo, se escrevermos o nome XPTO e selecionarmos as opções “Versão Digital” e “Mensagem SMS”, ao clicarmos em Cadastrar verificaremos a seguinte URL na barra de navegação:

`//servidor/app.asmx?N1=XPTO&OPT=Digital&OPT=SMS`

O trecho ressaltado após a **interrogação** corresponde ao que chamamos de **Query String**, onde estarão os dados, no formato **nome=valor**, separados pelo sinal **&**.

Caso modificássemos o método para “**post**”, a informação enviada não ficaria visível para o usuário, mas vale ressaltar que estaria transitando em um pacote sem criptografia na rede para o caso do **HTTP** comum.

#### Validação de formulários

Após entender como criar os formulários, devemos aprender a efetuar a validação dos dados preenchidos. 

Essa validação será feita através de **eventos** e métodos de acesso aos elementos HTML do JavaScript, e a validação dependerá bastante dos tipos de componente e informação considerados.

A forma mais aceita para o tratamento de elementos do HTML a partir do JavaScript é através do uso de identificadores nas tags HTML, com instruções getElementById, as quais seguem o formato abaixo.

![HTML e javascript com uso de identificadores](/media/desenvolvimento_de_software_java/aula5/img00019.png)

Quanto aos eventos, podemos observar alguns, no quadro seguinte, com suas respectivas aplicações no processo de validação.

| Evento   | Aplicação                                                                                                                                                       |
| -------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| onsubmit | Efetua a validação do formulário imediatamente antes do envio para o servidor. Necessita o retorno booleano, indicando se os valores podem ser enviados ou não. |
| onclick  | Normalmente uma chamada explícita de validação. Bastante utilizado em botões de rádio e caixas de marcação.                                                     |
| onchange | Ocorre quando o valor (value) sofre uma alteração.                                                                                                              |
| onfocus  | Ocorre quando o componente ganha o foco. Pode ser utilizado, por exemplo, para apagar o valor do campo.                                                         |
| onblur   | Ocorre na perda do foco pelo componente. É comum a aplicação de máscaras em valores numéricos como CEP e CPF.                                                   |
| onsearch | Este evento é iniciado quando um usuário digita algo em um campo de pesquisa (type=“search”).                                                                   |
| onselect | Utilizado quando algum texto é selecionado no campo.                                                                                                            |


**Exemplo 11**

```html

<!DOCTYPE html>

<html>
  <head>
    <title>Exemplo de Formulário</title>

    <meta charset="UTF-8" />

    <style>
      body {
        background-color: blue;
        color: white;
        font-style: bold;
      }
    </style>
  </head>

  <body>
    <form action="//servidor/app.asmx" method="get">
      Nome:<input name="N1" type="text" /><br /><br />

      Opções de Envio: <br />

      <input type="checkbox" name="OPT" value="Revista" />

      Revista Mensal

      <input type="checkbox" name="OPT" value="Digital" />

      Versão Digital

      <input type="checkbox" name="OPT" value="SMS" />

      Mensagens SMS<br /><br />

      <input type="submit" value="Cadastrar" />
    </form>

    <script>
      var objNome = document.getElementById("N1");

      var objOpt1 = document.getElementById("OPT1");

      var objOpt2 = document.getElementById("OPT2");

      var objOpt3 = document.getElementById("OPT3");

      function validar() {
        if (objNome.value == "") {
          alert("Nome deve ser preenchido");

          objNome.focus();

          return false;
        }

        if (!objOpt1.checked && !objOpt2.checked && !objOpt3.checked) {
          alert("Selecione ao menos uma opção de envio");

          return false;
        }

        return false;
      }
    </script>
  </body>
</html>

```

Devemos observar o formato da função de validação, a qual deverá retornar true ou false para o evento onsubmit, de forma a permitir ou não o envio da informação para o servidor. Por essa razão, a chamada desse evento é um pouco diferente dos outros.

![form html](/media/desenvolvimento_de_software_java/aula5/img00020.png)

No código JavaScript devemos estar atentos à forma como se relaciona com o HTML, capturando os componentes a ser validados nas variáveis objNome, objOpt1, objOpt2 e objOpt3, com o uso de **getElementById**, o qual recebe como parâmetro o id equivalente na tag da página.

Capturados nessas variáveis, podemos manusear as propriedades de cada componente em meio à função **validar**, relacionada com a submissão do formulário através do evento **onsubmit**.

Caso o nome não seja preenchido, a mensagem “Nome é obrigatório” é apresentada e o foco é direcionado para a caixa de texto referente a esse dado, através do método **focus()**.

Para o teste dos componentes do tipo checkbox, devemos verificar se nenhum deles foi marcado, e para isso utilizamos suas propriedades checked. Lembrando que, pelo fato de a propriedade ser booleana, a negação será equivalente à comparação com false.

![detalhe if](/media/desenvolvimento_de_software_java/aula5/img00021.png)

Ao final de cada comando **if** ocorre uma instrução **return false**, a qual sai imediatamente da função, retornando o valor false para onsubmit, e impedindo o envio. Apenas se ambos os testes forem falsos irá ocorrer **return true**.

O evento onsubmit é destinado a uma validação global antes do envio, mas não é a única opção do modelo de validação. Outras validações e formatações podem ser efetuadas no momento da perda do foco pela caixa de texto, ou quando selecionamos o elemento de uma lista de valores, entre diversas outras opções.
