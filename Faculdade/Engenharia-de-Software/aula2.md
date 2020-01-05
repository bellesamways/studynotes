### Revisando modificadores de métodos
A seguir estão relacionados alguns modificadores de acesso e qual o recado que uma classe manda para duas subclasses quando utiliza cada um deles:

* `abstract`: Um método abstrato precisa ser obrigatoriamente implementado em uma subclasse concreta. Isto é, que esse é um `hook method` que foi definido na superclass e precisa ser definido.

* `final`: Um método final não pode ser sobreescrito pelas suas subclasses e por isso nunca representará um `hook method`. Métodos `final` representada funcionalidades da classe que precisam ser imutáveis para seu bom funcionamento.

* `private`: Os métodos privados só podem ser invocados dentro da classe que são definidos, ou seja, eles representam métodos de apoio internos da classe e nunca poderão ser substituídos pela sublclasse como um `hook methdo`.

* `protected` e `public`: Todos os métodos públicos e protegidos, desde que não sejam `final`, são candidatos a `hook method`, isto é, estes métodos podem ser sobrescrito na subclasse que pode ser utilizado para a inserção de comportamento.