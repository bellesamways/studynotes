# Aula 3 - Atividade de análise no processo de desenvolvimento de softwares

### **Conceito de Modelagem**


**Modelagem**: Serve para verificar a qualidade dos requisitos, estudados na aula anterior, que se tornarão precisos e detalhados o suficiente para as atividades do próximo passo no processo de desenvolvimento de software.  
**Análise**: Atividade que utiliza o conceito de orientação a objeto,  utilizando a UML como notação. Tem como objetivo modelar o problema, não a solução.  
**UML**: Unified Modeling Language, linguagem de modelagem unificada, utilizada em engenharia de software para visualizar o desenho do sistema e a intercomunicação entre objetos.  
1. **Diagrama de Caso de Uso**: Representa o conjunto de comportamentos de alto nível que o sistema deve executar para um determinado ator. É o diagrama mais simples, e não há necessidade de grandes detalhamentos. Extend: ativado sob uma determinada condição. Include: obrigatoriamente será executado.  
2. **Diagrama de Classes**: Representa uma coleção de classes e seus inter-relacionamentos.  
3. **Diagrama de objetos**: Representa um retrato, em tempo de execução, dos objetos do software e seus inter-relacionamentos.  
4. **Diagrama de Colaboração**: Representa uma coleção de objetos que trabalham em conjunto para atender algum comportamento do sistema.   
5. **Diagrama de Sequência**: Representa uma perspectiva, orientada por tempo, da colaboração entre os objetos.  
6. **Diagrama de Atividades**: Representa o fluxo de tarefas que podem ser executadas pelo sistema ou por um ator.  
7. **Diagrama de Estados**: Representa um conjunto de estados que um objeto pode estar e os “gatilhos” que estimulam a transição do objeto de um estado para outro.  
8. **Diagrama de Componentes**: Representa uma coleção de componentes de software e seus inter-relacionamentos.  
9. **Diagrama de Depuração**: Representa uma coleção de componentes e mostra como esses são distribuídos em um ou vários nós de hardware.  
10. **Diagrama de Pacotes**: Representa uma coleção de outros elementos de modelagem e diagramas.  


### **Objeto e classe**

**Objeto**: Estrutura de dados encapsulada por procedimentos. Essa estrutura são os atributos e operações.  
**Classe**: Conjunto de objetos similares agrupados em que a etapa de análise está mais voltada para sua realização.  



Vejamos um exemplo para entender melhor.  
Classe: Pessoa.  
Objetos: Pessoas.  


### **Tipos de análise**

Na programação estruturada, o foco era na função.  
No paradigma OO, o foco é no objeto e seus atributos depois disso. Atributos (dados) que caracterizam o objeto. Operações que o objeto pode realizar através de métodos. Cada objeto pertence a uma classe (conjunto de objetos com as mesmas propriedades); objeto é uma instância de uma classe.    
1. **Abstração**: processo mental em que concentra o que é relevante.  
2. **Encapsulamento**: atributos de uma classe somente vão poder ser acessados pelos métodos daquela classe, porque os atributos de uma classe vão determinar o estado dela.  
![methods](/media/processos_dev_software/methods.png)
3. **Herança**: uma vez construída uma classe, eu posso herdar dessa classe tudo que foi construído e reaproveitar o que está ali.   
4. **Polimorfismo**: várias formas. Mesmo método, com classes diferentes, com funções diferentes, mas tem o mesmo nome. Permite a extensabilidade das funcionalidades.  


#### **Análise Estrutural**  


Tem como objetivo modelar aspectos estáticos de um problema, utilizando o modelo orientado a objeto. É utilizada em conjunto com detalhamento de requisitos para visualizar e fornecer base para identificar soluções para os requisitos apresentados.  


1. **Identificação de classes**: Identificar quais são as classes chaves. Fazer o levantamento com base em suas responsabilidades e colaborações. Utiliza-se em larga escala o cartão CRC (Class-Responsability-Collaborator).  
2. **Organização das classes**:   
   1. **Entidade**: Representa conceitos do domínio do problema herdada dos modelos de negócio.  
   2. **Fronteira**: Representa interfaces externas que estão dentro do produto, como interface de usuário e conexão com outros sistemas. Facilita o desenho das interfaces.  
   3. **Controle**: Organização que não pertence à entidade e nem à fronteira. Normalmente é associada a um caso de uso.  
3. **Identificação dos relacionamentos**: Ajuda a filtrar e refinar as classes.  
   1. **Associação**: Indica a relação entre duas classes em que o objeto de uma classe consegue obter informações da outra a que foi associado.  
   2. **Agregação**: Indica um associação, mas com a classe se apossando das informações de um objeto da outra.
4. **Identificação dos atributos**: A cada classe é atribuída uma característica responsável por tomar alguma ação.  
5. **Análise comportamental**: Aplicada depois que os requisitos forem detalhados, validando-os e indicando as dificuldades de implementação no plano de conceito.  
6. **Diagrama de interação**: Mensagens que são trocadas, ao longo do tempo, para execução de alguma tarefa.
    1. **Mensagens e Operações**: representam um mecanismo de interação, ou seja, um objeto só poderá receber uma mensagem invocada por uma classe.  
    2. **A mensagem** tem as seguintes partes: Receptor    Operação    Parâmetro
    3. **Interação**: como as mensagens trafegarão para a execução de uma tarefa.
    4. **Diagrama de sequência**: ordem temporal das ações que serão executadas.
7. **Identificação das operações**: Todas as mensagem devem se mapeadas para executarem alguma operação. Podem ser: Incluir, Alterar, Excluir, dentre outras.  



O processo de engenharia de requisitos é composto por quatro atividades de alto nível:  
* identificação ou levantamento;
* análise e negociação;
* especificação e documentação;
* validação.

