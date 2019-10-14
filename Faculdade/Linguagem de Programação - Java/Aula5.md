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
![Print de tela do código de uma classe abstrata](/media/Linguagem_de_Programacao-Java/Aula5/ExemploClasseAbstrata.png)

#### Polimorfismo
Capacidade que os métodos de mesmo nome têm de efetuarem tarefas diferentes.
O mesmo método com várias formas.
Acontece de duas maneiras em java: quando os métodos são definidos em função da classe que os utiliza (sobreposição), ou dos diferentes conjuntos de argumentos definidos para cada método (sobrecarga).

[![Icone de um arquivo PDF com o nome Polimorfismo.pdf](/media/Linguagem_de_Programacao-Java/Aula5/downloadPDF.png)](https://www.evernote.com/shard/s248/sh/509df3c5-42b5-47d9-9bbe-7ad99af234c5/6e0a676c82466316d5081467b38ee751/res/485fa420-41cf-4da3-a3f4-26483bce2951/polimorfismo.pdf)