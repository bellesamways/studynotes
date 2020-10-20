# Aula 9 -  Tratamento de exceção 
 

### Exceção 

Uma exceção é uma ocorrência que altera o fluxo normal da execução de um programa. Esta ocorrência deve ser tratada para evitar que o programa encerre seu funcionamento.  

Um método pode detectar uma falha, mas não estar apto a resolver sua causa, devendo repassar essa função a quem saiba. Se o tratamento de falhas for introduzido ao longo do fluxo normal de código, pode-se estar comprometendo muito a inteligibilidade do código. 

**Exceções em Java**

O lançamento de uma exceção causa uma interrupção abrupta no trecho de código que a gerou. O controle da execução volta para o primeiro trecho de código (na pilha de chamadas) apto a tratar a exceção lançada.  

Isso prejudica o bom design das aplicações. Se um método for usado em aplicações diferentes, o mesmo erro sempre será tratado da mesma maneira. Isso limita a flexibilidade de lidar com situações de exceção. 

Informando o compilador que o método poderá lançar uma ou mais exceções. No final do cabeçalho de um método que poderá lançar exceções, coloca-se a informação: 

throws <lista das classes de exceção que o método poderá lançar> 

Por exemplo: 
~~~java
public void f() throws NumberFormatException, IOException { 

... 

} 
~~~

Para certas classes a declaração é obrigatória, enquanto para outras é opcional.  
 

**Capturando e tratando exceções** 

os blocos try { }, catch(){ }, e finally { } 
~~~java
try {  

<comandos>  

} 
~~~
 
No caso de ocorrer uma exceção no bloco try, ela será lançada, os demais comandos do bloco serão suspensos, e o controle passará para o primeiro bloco catch que tenha um parâmetro de tipo compatível com a exceção lançada. Pode haver zero, um ou mais blocos catch após um bloco try. Os blocos catch e finally são opcionais, mas não é permitido haver apenas o bloco try sem pelo menos um bloco catch ou um bloco finally associado.  

O bloco finally será sempre executado após o bloco try terminar normalmete, ou após os blocos catch executarem, mesmo que a saída desses blocos seja causada pelo lançamento de outra exceção não tratada, ou por comando return. O bloco finally somente não será executado se ocorrer uma chamada para terminar a JVM, com System.exit(0).  

Comandos após o bloco finally serão executados se não houver os casos citados acima. Tipicamente, o bloco finally conterá comandos de liberação de recursos alocados no bloco try (abertura de arquivos, de banco de dados, etc). Se esses comandos ficassem no final do bloco try, poderiam nunca ser executados em caso de lançamento de exceção. 
 
~~~java
public void g() {  

    try{  

        f();  

    }  

     

    catch (NumberFormatException nfe){  

        <comandos para tratar a exceção>  

    }  

     

    catch (Exception e){  

        <comandos para tratar a exceção>  

    }  

} 
~~~
 
Suponha que ao executar, o método f() lance uma exceção do tipo NumberFormatException. Ela será capturada pelo primeiro bloco catch acima. Se lançar outro tipo de exceção, ela será capturada pelo segundo bloco catch. 
 

**Exceções verificadas e não-verificadas:**

A linguagem Java admite dois tipos de exceção.  

As **não verificadas (unchecked, em inglês)** são instâncias de subclasses de RuntimeException. O compilador não verifica se existe possibilidade de serem lançadas, e não exige que os métodos onde possam ocorrer façam qualquer tratamento. Elas representam erros ou defeitos na lógica do programa que podem causar problemas irrecuperáveis em tempo de execução (run time).

Por outro lado, instâncias de Exception, ou de qualquer outra de suas subclasses, são **verificadas (checked)** como, p.ex, IOException, ClassNotFoundException e CloneNotSupportedException. Elas representam erros que podem ocorrer em tempo de execução, mas que não dependem da lógica do programa, em geral defeitos nos dispositivos de entrada ou saída (arquivos, rede, etc).  

O compilador exige que um método onde possam ocorrer exceções verificadas faça uma de duas coisas: ou utilize blocos try-catch-finally para capturar e tratar essas exceções, ou declare que pode lançar essas exceções para o método chamador, colocando uma cláusula "throws" no seu cabeçalho, como por exemplo:  
~~~java
public void M() throws IOException, CloneNotSupportedException {  

..............  

}  
~~~
 
Essa cláusula é facultativa para o caso de exceções não-verificadas. 
 

## Construtores 

A classe java.lang.Exception, e todas as suas subclasses, têm pelo menos dois construtores da forma:  
 
<nome da classe de Exceção> (String <mensagem de erro>) 

<nome da classe de Exceção> ()  

A mensagem de erro é sempre retornada pelo método toString(). Toda exceção também aceita a mensagem printStackTrace(), que imprime na stream apontada por System.err um stack trace. O stack trace é um relatório detalhado da seqüência de chamadas a métodos que antecederam o lançamento da exceção. 

Para lançar uma exceção que seja instância das classes de verificação obrigatória a linguagem obriga o programador a declarar no cabeçalho do método quais as classes de exceção podem ter instâncias lançadas. Portanto, o formato completo do cabeçalho de definição de um método é:  
~~~java
<modificadores> <tipo> <nome>(<parametros>) throws <classes>  

static void m() throws ErroDoTipoX, ErroDoTipoY, ErroDoTipoZ{ . 

..  

throw new ErroDoTipoX(); 

...  

throw new ErroDoTipoY(); 

...  

throw new ErroDoTipoZ();  

} 
~~~

Se o programador quiser estender a classe que contém o método m() da tela anterior e se o programador quiser sobrepor o método m() então o novo método terá de declarar o lançamento de instâncias das mesmas classes. Isso garante que um código que trabalha com a classe base trabalhará também com as classes derivadas.  