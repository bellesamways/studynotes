# Aula 1 - ORIENTAÇÃO A OBJETOS E UML

A modelagem de sistemas consiste no desenvolvimento de modelos (**diagramas**) que representem o mundo real, sob a perspectiva do desenvolvimento de sistemas e está intimamente relacionada a dois fatores: ao **paradigma de desenvolvimento e ao processo de desenvolvimento em uso.**

**Paradigma** é uma forma de abordar um problema.

No **paradigma orientado a objetos**, o enfoque está na **identificação de classes e seus respectivos objetos** que interagem para a solução do problema.

Dentro da **perspectiva do desenvolvimento orientado a objetos**, surge a UML (Unified Modelling Language), uma linguagem unificada de modelagem, que permite aos desenvolvedores construírem diagramas sob diferentes perspectivas.

O desenvolvimento de sistemas é um processo intelectual e progressivo, em que os profissionais envolvidos adquirem mais conhecimento do sistema à medida que avançam no entendimento da realidade em que o sistema está inserido.

No início do processo, é preciso conversar com os profissionais envolvidos no negócio em questão para **compreender a realidade e o funcionamento do mesmo.**

Para representar a realidade e entender o que se passa no contexto do sistema a ser construído, precisamos **traduzir** a realidade em **modelos.**

**Modelos** = Nada mais são que **diagramas gráficos** que representam a realidade e ajudam os desenvolvedores  a compreendê-la. Portanto, modelar um sistema consiste em **criar um conjunto de modelos sob a forma de diagramas**, que representam a estrutura e o comportamento de um sistema.

**Paradigma imperativo ou estruturado**, caracterizado pelo uso das técnicas de Análise Estruturada e Análise Essencial, que foram eficientes para sistemas de **pequeno porte.**

**Paradigma Orientado a Objetos**, também chamado paradigma OO, para sistemas **mais complexos e robustos.**

Na OO, tarefa principal passa a ser a **identificação dos objetos do mundo real** envolvidos no contexto do sistema e a relação entre eles. Ao identificar os objetos, são identificados também os **dados (atributos) e as funcionalidades (funções)** inerentes àquele objeto.

OBJETO = DADOS + FUNÇÕES

Na medida em que são identificados todos os objetos pertinentes a um sistema, já teremos os **dados e os procedimentos** relacionados.

Um modelo OO tem com entidade fundamental o **Objeto**, que **recebe e envia mensagens**, executa procedimentos e possui um estado que, por proteção, apenas ele próprio pode modificar. Nesse processo, problemas são resolvidos, por meio de objetos, que enviam mensagens uns aos outros.

## Elementos básicos da OO:

1. **Objeto:** principal elemento do modelo. Representam as “coisas” a serem modeladas do mundo real. Cada objeto possui os dados inerentes a ele e possui as operações que ele executa.
2. **Mensagens:** Quando um objeto deseja que seja executada uma operação de responsabilidade de outro objeto, ele manda uma mensagem a esse objeto informando o que ele deseja que seja feito. A operação desejada será implementada por meio de um método da classe que recebe a mensagem.
3. **Atributos:** dados que caracterizam o objeto.
4. **Métodos:** procedimento (implementado por uma rotina ou função) que executa uma operação em um objeto, que define parte do seu comportamento. 
5. **Classes:** conjunto de objetos com as mesmas características (atributos e métodos).

**“Objeto é uma instância de uma classe”, isto é, a classe é o molde e o objeto, a “coisa real”.**

## Pilares da OO:

1. **Encapsulamento:** esconder; o objeto esconde seus dados (atributos) do acesso indevido de outros objetos.
2. **Herança:** Mecanismo para derivar novas classes a partir da definição de classes existentes através de um processo de refinamento.
3. **Polimorfismo:** muitas formas; a partir do momento em que uma classe herda **atributos e métodos** de uma (herança **simples**) ou mais (herança **múltipla**) classes base, ela tem o poder de **alterar o comportamento de cada um desses procedimentos (métodos).**
4. **Visibilidade:** uma classe pode visualizar da outra. Como princípio, devemos garantir o encapsulamento, ou seja, os atributos devem ser privados (acessíveis apenas por métodos da própria classe) e determinados métodos públicos (acessíveis por todas as classes), e acessar esses dados.

O uso de técnicas orientadas a objetos facilita o controle da complexidade uma vez que promove uma melhor estruturação de seus componentes e também permite que componentes já usados e validados possam ser reaproveitados.

As hierarquias de classes (herança) são componentes portáveis entre aplicações.

Proporciona modularidade trazendo os seguintes benefícios:

- Reusabilidade: softwares podem ser escritos com base em componentes já existentes;
- Extensibilidade: novos componentes de software podem ser desenvolvidos a partir de outros, já existentes, sem afetar o comportamento do componente de origem.

Um sistema desenvolvido com as características do modelo OO tende a ser bem estruturado posto que os objetos são unidades coesas com interfaces simples que escondem as suas implementações.

## Conceitos de Análise e Projeto Orientado a Objeto
Análise de sistemas significa uma investigação dos problemas e dos requisitos de um contexto, em particular, com vistas ao desenvolvimento de um sistema automatizado. A ideia básica é identificar quais seriam as funções que esse sistema precisa ter, de forma a atender eficientemente as necessidades de seus usuários.

**Atividade de análise e projeto:**

- Análise de requisitos (investigação dos requisitos);
- Análise do domínio do problema.


**Análise implica em identificar e descrever os conceitos no domínio do problema.**


**Atividade de análise:** definição dos objetos de software e como eles colaboram para que os requisitos dos usuários sejam plenamente satisfeitos.
**Atividade de projeto:** denota uma solução, voltada a atender aos requisitos, considerando aspectos de tecnologia.


**Análise pode ser traduzida em “faça a coisa certa”, e projeto em “faça certo a coisa”.**


Identificação e modelagem dos objetos do mundo real que afetam o sistema.


**UML** = (Unified Modeling Language) é uma linguagem padrão para **construção de projetos de sistemas**, orientados a objeto, voltada para visualização, especificação, construção e documentação de artefatos de um sistema. Independente do método de desenvolvimento utilizado. 
**Linguagem de modelagem != linguagem de desenvolvimento**

1. **Visualização:** A modelagem gráfica tende a facilitar a compreensão, permitindo sua interpretação sem ambiguidades.
2. **Especificação:** Permite a construção de modelos precisos, sem ambiguidades e completos. A UML atende a esses quesitos sob o ponto de vista da análise, projeto e implementação.
3. **Construção:** Os diagramas UML podem ser diretamente integrados a várias linguagens de programação tais como Java e C++.
4. **Documentação:** A UML abrange a documentação da arquitetura do sistema e de todos os seus detalhes. 


Os diagramas da UML são divididos em 2 grupos: **Diagramas de Estruturas e Diagramas Comportamentais.** No total, eles formam 14 diagramas.

![diagrama](../../media/modelagem_de_sistemas/aula01/img/img001.png)


[PDF - Diagramas de UML](../../media/modelagem_de_sistemas/aula01/pdf/diagramas_de_uml.pdf)

**UML como esboço:** desenvolvedores usam a UML como forma de expressar aspectos relevantes de um sistema, esboçando ideias e alternativas do que pretende fazer. Geralmente, são usados desenhos informais, sem ferramentas e cujo objetivo é a discussão de ideias visando à construção de software de forma colaborativa. O modo UML, como esboço, está mais compatível com as metodologias ágeis, que preconizam mais código e menos documentação.

**UML como projeto:** construir um projeto completo para ser codificado por programadores, valendo-se de ferramentas case para melhor entendimento dos modelos pela equipe. O modo UML, como projeto, está mais alinhado com os processos de desenvolvimento mais complexos, como processos iterativos e incrementais, como o PU (processo unificado) implementado através da ferramenta RUP (Rational Unifiec Process) prototipação.

**UML como linguagem de programação:** Onde os desenvolvedores desenham os diagramas que são compilados para o código executável e a UML se torna o código fonte. Exige ferramentas mais sofisticadas. O modo UML, como linguagem de programação, tende a ser mais usado em modelos de desenvolvimento de prototipação.

**Processos iterativos:** são processos onde o ciclo de vida do sistema é dividido em uma série de mini projetos, curtos, preferencialmente de duração fixa (por exemplo, 3 meses), denominados iterações.

Uma ferramenta **case** é um programa que auxilia aos membros da equipe de desenvolvimento no estudo, modelagem e **construção do sistema**, possibilitando que vários diagramas possam ser elaborados em conjunto, representando a estrutura e comportamento do sistema a ser desenvolvido.