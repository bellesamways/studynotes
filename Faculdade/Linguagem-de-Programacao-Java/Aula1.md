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
