# Aula 1 - Conceitos de Software e Linguagem de Programação

**O que é software?** É um conjunto integrado de programas de Computador.

**O que é um programa de computador?** É um conjunto de instruções que descreve, passo a passo, uma tarefa que deve ser realizada pelo hardware.

**Paradigma:** classificações para as linguagens de programação, avalia como as instruções são compostas e organizadas para formar o programa.

**1. Imperativo:** elementos de código em formato de blocos que se interligam através de três tipos de instrução, da chamada Programação Estruturada.

- a) **Sequência:** As instruções são organizadas de forma sequencial (tarefa 1 finaliza, entra tarefa 2).

- b) **Seleção:** Onde as instruções podem ser executados baseadas na avaliação de uma condição (IF (Condição=V) THEN Sequencia1 ELSE Sequencia2

- c) **Iteração:** Onde as instruções podem ser repetitivas até uma condição ser atingida.

**2. Orientada a Objeto (OO):** elementos de código em formato de objetos que se interligam. Um objeto é composto de atributos (dados) e métodos (ações). Os objetos são agrupados em classes.

- a) **Classe:** tipo de objeto
- b) **Atributos:** variáveis que estão dentro de cada objeto da classe
- c) **Método:** ação que a classe pode realizar

Exemplo: Classe ALUNO.

Atributos: Nome, Matricula, Telefone, endereço

Métodos: Incluir Aluno, Matricular em curso, Incluir Disciplina

## Software básico

São softwares que permitem a operação e programação de computador, como as linguagens de programação e o sistema operacional. Exemplos de sistemas operacionais: Windows, MacOs, Ios, Android

![software básico](/media/processos_dev_software/software_basico.png)

- **Monotarefa:** Executa somente um processo de cada vez.
- **Monousuário:** Somente é permitida a utilização de um usuário de cada vez.
- **Multitarefa:** Os processos são compartilhados e enfileirados a espera do processador. É distribuído de modo que pareça ser executado simultaneamente.
- **Multiprocessamento:** Distribui para mais de um processador.
- **Multiusuário:** Vários usuários utilizam ao mesmo tempo.

## Software aplicativo

O software aplicativo, como diz o nome, revela alguma utilidade (aplicativo) ao usuário, como por exemplo: editores de texto, planilhas eletrônicas, folha de pagamento, contas a pagar, aplicativos diversos de celulares e etc.

![software aplicativo](/media/processos_dev_software/software_aplicativo.png)

### Características e aplicações do software

O software pode ser classificado de acordo com a sua forma de cópia e distribuição (licença de uso). Em geral, o software pode ser:

1.  **Software gratuito ou freeware:** Programa de computador cujo uso não implica o pagamento de licença de uso. O Freeware pode ser copiado e distribuído gratuitamente. O Freeware pode ser utilizado sem pagar, mas o código fonte não é disponibilizado, logo o freeware não pode ser modificado. Assim sendo o freeware só pode ser usado da forma como é disponibilizado.
1.  **Software livre:** Programa de computador cuja utilização, cópia e distribuição não possui restrição. É comum o código fonte estar disponível para manuseá-lo, e dessa forma o software pode ser modificado, por quem desejar, sem que seja necessária a permissão ou que se pague ao autor.
1.  **Comercial:** Programa onde deve-se pagar um valor para sua aquisição e/ou uso.
1.  **Adware:** Programa de computador que executa automaticamente algum tipo de publicidade após sua instalação ou durante sua utilização.
1.  **Demo:** Fração de um programa. Funciona como material promocional para dar a oportunidade do produto ser avaliado. É restrito de suas funcionalidades apenas para teste.
1.  **Trial:** Programa semelhante ao demo, mas com funcionalidades disponíveis por tempo determinado.
1.  **Shareware:** Programa de computador que possui limitações de tempo e/ou funcionalidades. Ao final do tempo estabelecido, o programa pode requisitar o pagamento para uso do software completo ou pode continuar rodando sem todas as suas funcionalidades ou, ainda, interromper o seu uso.

#### O processo de desenvolvimento de software

![processo de desenvolvimento de software](/media/processos_dev_software/processo_desenvolvimento_software.png)

- **Concepção:** fase onde o sistema é concebido e avaliada a sua viabilidade (técnica, econômica, tempo). Caso viável o desenvolvimento segue nas fases seguintes e caso contrário é interrompido.
- **Requisitos:** Em muitos modelos de processos de desenvolvimento, a fase de requisitos pode estar junta com a de Analise, mas a finalidade é identificar as necessidades dos usuários para definir os requisitos do sistema.
- **Análise:** fase de estudo, onde é definido O QUE o sistema deve fazer, independente da tecnologia que venha a ser usada. Define-se, dentre outras coisas as funcionalidades que o sistema precisa ter.
- **Projeto:** onde define-se as tecnologias a serem usadas: linguagem de programação e banco de dados. É também a fase de definição da arquitetura do software e seus respectivos elementos. E fase do COMO fazer o software.
- **Codificação:** é a escrita de cada programa que vai compor o sistema, na linguagem de programação selecionada. Depende tecnicamente da qualidade do programador para gerar códigos inteligíveis e de fácil manutenção.
- **Testes:** Verificação de erros no sistema e apuração se o mesmo executa as ações previstas e necessárias a seus usuários. Abrange um conjunto de testes em diferentes momentos da fase de codificação. Deve-se testar, inicialmente, cada programa separadamente e depois o conjunto integrado de programas.
- **Homologação:** fase onde os usuários atestam que o software atende (ou não) as suas necessidades, liberando-os (ou não) para uso.
- **Implantação:** fase onde o sistema é posto em uso, no ambiente do usuário, o que requer instalação dos softwares , treinamento a usuários e acompanhamento do uso por um período de tempo (acordado previamente, em contrato, preferencialmente).
- **Manutenção:** uma vez implantado, o sistema precisa sobreviver ao longo dos anos, adequando-se as mudanças da empresa e do contexto onde a mesma esta inserida.

O **RUP** é um processo de desenvolvimento de software. Ele engloba as ações necessárias para transformar um conjunto de requisitos do cliente em um sistema de software. O RUP combina os ciclos de vida iterativo e incremental de forma que cada entrega do software em um ciclo agrega mais valor ao produto em relação ao ciclo anterior. A grande vantagem em desenvolver um grande sistema usando um processo incremental é a diminuição do risco, pois cada entrega pode ser avaliada e o passe seguinte alinhado com os objetivos do cliente, que nem sempre permanecem constantes durante o desenvolvimento de um projeto.

Suas fases são:

1.  Iniciação
1.  Elaboração
1.  Construção
1.  ransição

# Aula 2 - Atividades para Análise de Viabilidade


**Estudo de viabilidade**


**TÉCNICA**: Visa a atender os requisitos técnicos do produto a ser desenvolvido. O levantamento deve estar relacionado com a tecnologia existente no processo de desenvolvimento.  
**OPERACIONAL**: Visa atender os requisitos para a aceitação do produto ou problema apresentado. O levantamento deve estar relacionado com a aceitação da solução proposta, e como os agentes se sentirão em relação a ela.  
**CRONOGRAMA**: Visa a atender os requisitos de tempo para os prazos estabelecidos. O levantamento deve estar baseado na viabilidade técnica em relação ao prazo estipulado. Prazos obrigatórios são mais difíceis de serem negociados.  
**ECONÔMICA**: Visa a atender os requisitos financeiros do projeto/produto. Considerada a mais critica, consiste em julgar se o projeto será deficitário ou se os custos de sua implementação não terão os benefícios desejados.  


A Fase Econômica também é chamada **Análise de Custo-Benefício.**


**Operação**: Custos fixo e contínuos. Ex.: pessoal, manutenção, energia.    
**Desenvolvimento do projeto**: Custos que ocorrem somente uma vez. Ex: aquisição de novos softwares; instalação; atualização.


**Análise de ROI (Return On Investment)**: Percentual que mede a relação entre quanto se ganhou e quanto se investiu.     
        ROI = (total de lucro – total custo) / total de custo  
Quanto maior for a taxa, melhor será o ROI.


##### **Classificação de Requisitos**


1. **Requisito**: É uma condição ou necessidade para resolver um problema ou alcançar um objetivo. Também pode ser estar presente em um sistema a fim de satisfazer uma condição, um contrato, um padrão, ou uma especificação devida.  
2. **Requisito do usuário**: Definições sobre a função do sistema e as restrições sob os quais ele deve operar. O formato é em linguagem comum, visando ao entendimento do cliente/usuário.  
3. **Requisito do sistema**: Definição estruturada e detalhada do serviço que será feito no sistema/produto. O formato é em Contrato de Prestação de Serviço entre o cliente e o fornecedor.  
4. **Requisitos funcionais**: Descrevem as funcionalidades do sistema. Estão diretamente ligados às especificações da tecnologia envolvida, do perfil do usuário, do tipo do sistema.   
5. **Requisitos não funcionais**: Algumas propriedades e suas medições:

      1. Velocidade -> Transações / segundos
      2. Tamanho -> Mbytes
      3. Confiabilidade -> Tempo médio de falhas
      4. Facilidade de uso -> Treinamento


##### **Técnicas de elicitação de requisitos**


Podem e devem ser combinadas, de acordo com a necessidade do levantamento de dados e dos perfis de usuários.  
1. **Entrevista**: Utilização na análise de problema e na engenharia de requisitos com o objetivo de entender as perspectivas do cliente/usuário. Entender quem são os agentes e quais as necessidades, o problema e a solução.  
2. **Questionários**: Forma de utilização que faz perguntas referentes ao sistema. Utilização de hipóteses para as relevâncias. Podem ser utilizados após a entrevista. Útil quando a quantidade de pessoas a levantar dados é grande e/ou estão geograficamente distantes. Ganha contornos de destaque na medida em que a internet fomenta o uso de questionários eletrônicos e online.  
3. **Casos de uso**: Identificação dos agentes que atuam no sistema; das interfaces que o sistema/produto possuirá; validação de pré-requisitos. Representação visual ao invés de textual.  
4. **Brainstorm**: Ou tempestade de ideias, faz o levantamento de ideias, em que cada uma sugerida pode combinar na propositura de uma nova. Atividade de livre imaginação que deve ser tratada sem críticas ou debates.  

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

# Aula 4 - O desenho no processo de desenvolvimento de software


#### **Atividades da fase de Projeto ou desenho de software**


* Constrói a solução computacional, com base na especificação do problema.  
* Avalia as alternativas tecnológicas disponíveis.  
* Define as tecnologias de Linguagem de programação e SGBD (Sistema Gerenciador de Banco de dados) que serão usados no desenvolvimento
* Especifica a infra e sistema computacional necessária  
* Desenha a arquitetura do software  
* Projeta a interface do software  
* Projeta o banco de dados que o software usará  
* Mostra a relação com outros sistemas  
* Cuidados  
  * Uso de tecnologias novas: custo compensa o risco?  
  * Orçamento: soluções reais  


### **Problema vs. Solução**

**Problema**: Através do levantamento de informações na fase de análise de requisitos, define-se um problema ou meta a ser alcançado.  
**X**  
**Solução**: Após levantamento, uma solução deverá ser escolhida dentre várias possíveis, isto é o papel do arquiteto de software. A documentação do desenho explicita a solução que será tomada para resolução do problema.  


**Ambiente e Arquitetura do Software**: relação do sistema com o ambiente em que está inserido, bem como a relação entre os elementos internos.  

#### **Modelos de desenho**


**Desenho interno**: É a maneira como o sistema interage com outros produtos ou sistemas. Podem conter parte físicas, lógicas, interconexões com outros sistemas e produtos, interna ou externamente.  
**Desenho externo**: Visão que os usuários terão da solução ou produto e a forma com que eles interagirão.  

### **Nível de abstração e agregação**


**Nível estratégico ou desenho arquitetônico**: É o corpo da arquitetura do sistema a ser implementado. Com base nesse desenho, já se pode saber se o sistema atenderá aos requisitos e aos custos relacionados do projeto.  
**Nível tático ou desenho lógico**: É a aplicação das decisões tomadas no nível estratégico. A solução contemplará a reutilização, ou não, de componentes, que serão desenvolvidos para ele, buscando satisfazer os requisitos do produto.  
**Nível operacional ou desenho detalhado**: É o comportamento de cada componente. É desenvolvido em conjunto com a documentação voltada para usuários, no caso de desenho externo, ou documentação do código do programa, no caso de desenho interno.  


**Reutilização**: Nesta fase, é comum se fazer uso de processos que já foram definidos, usados e testados em outros projetos ou produtos, evitando o retrabalho.  


1. **Código**: Reutilização de parte ou todo ó código fonte de módulos do sistema. Só é possível quando na fase de construção do código aplicou-se corretamente conceitos como o de coesão, acoplamento.
2. **Reutilização de objeto**: Bibliotecas e classes fundamentais.
3. **Reutilização de plataforma**: Reutilização de Plataforma - Camada de arquitetura, consiste na colaboração de ferramentas para gerenciar e automatizar o ciclo de vida de desenvolvimento de software, com a utilização de "templates" de processos.
4. **Desenho**: Aproveitamento de ideias para solução de problemas, são comumente encontradas em padrões, frameworks e arquiteturas, abordagens que permitem a reutilização ao nível de desenho.
5. **Reutilização de classe**: Módulo de código binário, mecanismo baseado em: Composição (“tem um”) e Herança ou derivação (“é um”).

# Aula 5 - As atividades de teste no processo de desenvolvimento de software

A fase de teste tem como objetivo detectar possíveis defeitos ou erros que possam surgir na fase de implementação. Nessa fase, de testes, deve-se coletar os resultados e analisá-los e consertá-los antes de sua implantação.
Essa fase é essencial para aumentar a qualidade do produto ou sistema em que será implantado.

## Conceito de teste para o processo de desenvolvimento de software

**Principal objetivo dos testes de software:** revelar falhas para que sejam corrigidas até que o produto final atinja a qualidade desejada ou acordada.

- Testes funcionais da aplicação
- Avaliação da especificação de requisitos
- Avaliação de projeto técnico
- Verificações em outros documentos
- Testes de performance e capacidade
- Avaliação de interface
- Dentre outros

“Quanto mais cedo, defeitos forem encontrados antes da implementação do sistema, o custo de correção é menor em relação ao encontrado na fase de produção”  
**(Regra de Myers)**

**Defeito** – passo, processo ou definição de dados incorreto, por exemplo, uma instrução ou comando incorreto.  
**Engano** – ação humana, por exemplo, tomada pelo programador, que produz um resultado incorreto.  
**Erro** – diferença entre o valor obtido e o valor esperado. Qualquer resultado incorreto ou inesperado na execução do programa.  
**Falha** – produção de uma saída incorreta com relação à especificação.

**CAUSA:** Engano; Defeito; Erro.  
**CONSEQUÊNCIA:** Falha

1.  **Teste:** Processo definido com intenção de encontrar um erro.
1.  **Objetivo:** Encontrar um erro que ainda não foi descoberto. Um teste bem sucedido corresponde à descoberta de um erro não previsto.
1.  **Critério:** Definição de uma métrica que, após análise do comportamento do sistema, atenda o critério.
1.  **Procedimento:** Conjunto de instruções para a realização de testes.
1.  **“Script” de teste:** É uma representação definida de um procedimento teste.

## Processo de Teste de Software

- **Planejamento dos testes:** “Garantir que os testes sejam preparados antes do fim da implementação do produto”.
- **Execução dos Testes:** “Executar os casos e procedimentos de teste especificados e comparar os resultados esperados e obtidos, registrando esses resultados”.
- **Controle dos testes:** “Garantir que os testes planejados sejam executados corretamente e seus resultados possam ser registrados através da sua monitoração constante”.

**Teste caixa preta (teste funcional):** Neste teste <u>o objetivo é testar todas as entradas e saídas desejadas</u>, mediante uma determinada entrada definida de dados. Aqui não se está preocupado com o código, **cada saída indesejada é vista como um erro**. Os mecanismos internos do sistema não são levados em conta.

**Teste caixa branca (teste estrutural):** Neste caso o <u>objetivo principal é testar o código dos componentes do sistema, quanto a sua estrutura e construção</u>. Os mecanismos internos do sistema serão analisados e suas representações lógicas também. Este teste não exclui a necessidade do Teste Caixa Preta, uma vez que o funcionamento interno do sistema ou produto pode corresponder logicamente, podendo produzir uma saída diferente da esperada. É comum se encontrar partes do código que nunca foram testadas.

## Classificação dos testes

### Quanto à utilização do código:

**Testes estáticos:** São testes realizados pela **análise estática e visual do código fonte**. Os componentes do software são verificados **sem que o produto seja executado**. <u>O principal objetivo dessa técnica é identificar erros de programação</u>, tais como: Prática ruins de programação; Práticas ruins; Erros de sintaxe; Falhas de segurança. Todos os caminhos de execução, processamento e exibição de valores são examinados. Como consequência, erros mais comuns são descobertos mais rapidamente.

**Testes dinâmicos:** São testes baseados na **execução do código do programa**. Informações que são inseridas nas **rotinas de entrada e saída de dados**. Além disso, são verificados itens como: O tempo de resposta; A performance da aplicação; A capacidade do software se adaptar a diferentes ambientes; O comportamento funcional. <u>Permite que problemas mais sutis sejam identificados</u>. As chances de um “bug” passar por uma análise estática e uma análise dinâmica, sem ser rastreado é consideravelmente baixa. <u>O teste dinâmico consegue dar mais segurança e confiabilidade ao produto final</u>.

### Classificação quanto ao nível dos testes:

**Testes de unidade (teste unitário):** Teste em nível de módulo, componente ou classe. É o teste cujo **objetivo é um “pedaço do código”**, ou em alguns módulos definidos que representam uma única unidade. A documentação do projeto define a quantidade de módulos a serem testados. Em geral, realizado pelo próprio programador, ou pelo seu par (em caso de ser usada nas metodologias ágeis).  
**Testes de integração:** Teste utilizado para **garantir que um ou mais componentes combinados, ou unidades, não contenham erros**. Podemos dizer que um teste de integração é composto por diversos testes de unidade. A cada teste de unidade encerrado, a unidade é integrada ao sistema já pronto, formando um nova versão, que deve ser testado em conjunto. Testa-se, em geral, as interfaces entre os componentes.  
**Teste de sistemas:** Teste do sistema **como um todo ou de uma entrega parcial**, contendo todos os elementos.  
**Testes de validação:** Teste realizado **após a integração de todos os módulos ou unidades** do sistema.

![Ferramentas automação teste](/media/processos_dev_software/ferramentas_automacao_testes.png)

**Partes fundamentais de um processo de desenvolvimento de software:** Planejamento, execução e controle.

**Visão interna:** É a visão que representa os componentes do sistema, a relação entre os componentes, o funcionamento dos componentes e a interconexão com outros sistemas.

São problemas encontrados na implementação do processo de desenvolvimento de software:
**resistência a mudanças**, erro no uso de metodologias a serem adotadas, adoção de ferramentas inadequadas, **desconhecimento do escopo do projeto** e inadequação da equipe.

# Aula 6 - A Implementação no Processo de Desenvolvimento de Software

A **implementação**, é o processo que realiza a transformação do desenho em diversos tipos de componentes de código de programação.

Aquele que sem muito conhecimento do sistemas, tenta fazer a implementação de algo dentro dele, comete um **erro crasso**.

A implementação deriva do design, ou seja, no desenho foi pensado na arquitetura, nos componentes, na integração dos componentes e agora será tornado real na implementação.

**Objetivo da implementação:** escrever os programas e seus componentes em uma linguagem de programação.

**Código Fonte:** Conjunto de instruções geradas através de uma linguagem de programação, de maneira lógica e estruturada; após o processo de compilação ou interpretação, transformar-se-á em código objeto.

**Código Objeto:** Resultado da compilação do código fonte.

**Código Máquina:** Sequência binária de ações diretamente direcionadas para o processador da máquina.

**Compilador:** Programa que faz uma leitura do código fonte, desenvolvido em uma linguagem de alto nível, e transcreve para um novo tipo de linguagem chamada de baixo nível.

**Interpretador:** Programa que, além de fazer a leitura do código fonte e transformá-lo em código objeto, efetua a execução do mesmo sequencialmente.

**Linguagem de baixo nível:** Linguagem de programação que utiliza a arquitetura do processador para executar as ações. Esta linguagem é a que mais se aproxima dos códigos de execução direta do processador, ou seja, linguagem de máquina.

**Linguagem de alto nível:** Comumente chamada de linguagem de programação, esta linguagem se aproxima mais da linguagem humana, ou seja, linguagem com um padrão de entendimento humano bem definido. Para essa linguagem não é levado em consideração a arquitetura do computador, nem as características do processador e seus registradores, visto que, na fase de interpretação ou compilação, esses programas transformarão em linguagem de baixo nível ou de máquina.

### Classificações das linguagens

**Nível:** alto, médio ou baixo nível. Caracterizado pelo acesso ou não aos componentes de hardware.

**Paradigma:**
 - mperativo (sequência, atribuição, estado);
 - funcional (função, aplicação, avaliação);
 - lógico (relação, dedução);
 - orientado a objetos (objeto, estado, mensagem)
 - concorrente (processo, comunicação síncrona e assíncrona).

**Geração:**
 - 1ª geração: linguagem de máquina, binária. baixo nível. dificuldade pro homem.
 - 2ª geração: assembly. foi considerada a primeira linguagem de alto nível, visto que era de fácil entendimento e, portanto, considerada mais humana.
 - 3ª geração: Pascal, Cobol, C, C++. conceitos de programação estruturada e programação orientada a objetos.
 - 4ª geração: linguagens declarativas. SQL. É característica dessa linguagem dar suporte para execução de rotinas auxiliares a linguagens de terceira geração.
 - 5ª geração: linguagens do conhecimento, em geral aplicada em IA. Prolog, Lisp.

Uma vez que o desenho será a base da implementação, o processo de documentação de uso do produto passa a ter importância nesta fase, onde a documentação e a programação devem andar lado a lado.

# Aula 7 - A documentação do sistema de software

## **Documentação do produto**
Documento com formato adequado ao perfil do público que utilizará o sistema ou produto. A linguagem deve se clara e os termos e construções devem estar de acordo com o nível cultural e técnico do usuário final.

- **Manual de introdução:** Descreve as funcionalidades do sistema, como o usuário pode utilizar, os pré-requisitos necessários para funcionar.
- **Manual de referência:** Descreve facilidades do uso do sistema, informa os erros que podem ocorrer e como agir quando encontrá-los.
- **Documento de instalação:** Descrição de como instalar o sistema, plataformas de operação, pré-requisitos necessários.
- **Referência rápida:** Documento com um resumo das funcionalidades, atalhos de procedimentos, principais funções utilizadas, e mensagens de erros mais comuns.
- **Documentação do software:** Processo que descreve as partes do código fonte, requisitos necessários, arquitetura do sistema. Essa documentação é bastante útil para o desenvolvedor no processo de melhoria ou correção do produto.

Ciclo de vida do sistema = ciclo de desenvolvimento + ciclo de manutenção

![ciclo de vida de um sistema](/media/processos_dev_software/ciclo_vida_sistema.png)

**Manutenção do software:** Consiste em corrigir defeitos ou deficiências encontradas pelos administradores ou usuários do produto. A manutenção também pode ser considerada um processo de melhoria das funcionalidades do software.

**Refatoração:** Dentro do processo de manutenção do software existe a refatoração, que tem como objetivo melhorar um sistema de software, modificando sua estrutura interna, sem alterar o comportamento interno.

**Separação Estática:** Processo pelo qual identifica-se variáveis que apresentem algum tipo de não conformidade com o programa. O processo leva a identificação do código onde a variável afeta sua funcionalidade.

### **Documentação do processo**

- **Cronogramas:** Documentação utilizada por gerentes de projetos, executivos e gerentes funcionais, para acompanhar o andamento do projeto.
- **Comunicação:** Estabelece a forma de comunicação entre os membros do projeto.
- **Relatórios:** Documentação de acompanhamento de recursos utilizados durante o andamento do projeto.
- **Padronização de processos:** Estabelece o formato e a cadência de como o processo deve ser implementado. Essa padronização pode seguir o formato definido pela empresa, organização, ou um formato mais abrangente, como nacional ou internacional.
- **Documentos técnicos:** Descreve estratégias de como chegar ao resultado final, registram os erros, problemas e ideias que ocorrem durante o projeto, e as razões que foram utilizadas para as tomadas de decisões.

# Aula 8 - O desenvolvimento do software em cascata
O modelo em cascata, também conhecido como “water fall” ou “Top-Down” tem como característica utilizar as etapas de um modo sequencial e constantemente para frente.

**Modelo balbúrdia**
Metodologia de desenvolvimento de software em que os antigos desenvolvedores baseavam-se em suas próprias experiências para desenvolver os softwares.

Esse modelo podia ser descrito por um ciclo de duas fases:
1. Correção
2. Implementação

**Codifica - remenda**
Metodologia semelhante ao modelo balbúrdia em que, após a implementação, os erros e atualizações eram descobertos durante a sua utilização. Os ajuste que precisavam ser feitos eram programados em caráter de urgência, gerando insatisfação e pressões de usuário. Como consequência, a qualidade e a confiabilidade do sistema eram sempre postos à prova.

## Modelo cascata

**Ciclo da vida do projeto:** Conjunto de atividades descritas e ordenadas que segue um fluxo contínuo de informações e relacionamentos para auxiliar o acompanhamento de um projeto.

**Modelo de processo de cascata:** Primeiro modelo conhecido em engenharia de software. Consiste em um modelo linear em que cada atividade tem de ser completada antes de iniciar a próxima.

![modelo cascata](/media/processos_dev_software/modelo_cascata.png)

Exemplo: **Projeto** só inicia quando **Requerimento** finalizar.

![modelo cascata](/media/processos_dev_software/modelo_cascata_smart.png)

**Vantagens:** Para pequenos projetos que não necessitem de padronizações e documentações, o modelo em cascata pode ser útil, pois o ganho de tempo na fase de planejamento pode ser um diferencial no tempo total do projeto.

**Desvantagens:** O modelo em cascata visa ao encerramento de uma fase, ou etapa, para o início da outra subsequente. Durante um projeto, algumas atividades estão em constante mudança, uma delas são os próprios requisitos. Se o processo somente pode ser seguido após a finalização da etapa anterior, este nunca irá se encerrar.

## Modelo cascata com realimentação
Modelo que permite a revisão de fases anteriores e a superposição entre as fases. Esse modelo é uma variante do modelo cascata tradicional que permite a realimentação, ou seja, correções que surgirem durante outras fases do processo.
Exemplo:

![modelo cascata realinhamento](/media/processos_dev_software/modelo_cascata_realinhamento.png)

**Vantagens:** Possibilidade de correção de erros durante o processo de desenvolvimento de software.

**Desvantagens:** Dependendo da quantidade de revisões e realimentações, o processo pode se tornar difícil de gerenciar.

# Aula 9 - O processo iterativo e incremental

#### **Desenvolvimento iterativo e incremental**  
**Modelo iterativo** é aquele que o progresso vem de sucessivos refinamentos, melhorias. Caracteriza-se pela seleção de uma parte do projeto onde o grupo de desenvolvedores identifica, especifica, implementa e testa a iteração. Se esta atender às especificações, a equipe passa para a próxima iteração.  


![div_next_int](/media/processos_dev_software/div_next_int.png)  


**Modelo incremental** é entregue em pedaços. Cada pedaço representa um incremento no subconjunto de funcionalidades do sistema como um todo. Modelo que se baseia na ideia de aumento do âmbito do sistema, ou seja, na criação de novas versões para o modelo proposto.


![part_pro](/media/processos_dev_software/part_pro.png)  


Priorização do que é mais importante e que irá gerar mais valor ao cliente.



**Vantagens**: entregas parciais (possíveis mudanças mais rápidas), agregar mais valor ao produto, redução de incertezas no projeto, adequação aos softwares mais atuais, facilitação de testes.  
**Desvantagens**: mais difícil de gerenciar (prazos e etc podem sofrer mudanças com mudanças de requisitos), necessita de equipe madura, autodisciplinada e conhecedor de metodologias incrementais, muito mais complexo definir contratos com os clientes.   



Modelos **ágeis** seguem essa linha de iterativo e incremental.  


**Modelo Iterativo e Incremental**: Metodologia de desenvolvimento de software que define um subconjunto de requisitos e utiliza o modelo em cascata para sua realização. Cada porção do ciclo segue o projeto de arquitetura inicial como guia, mas com uma abordagem bem menor. Uma vez satisfeitos os requisitos e os objetivos da iteração forem completos, o desenvolvimento segue para a próxima iteração.  



**Modelo de Prototipagem**: Criação de um modelo para ser analisado e desenvolvido a partir dele. O Analista coletará informações (requisitos) para um mini projeto (protótipo), concentrando-se nas entradas e saídas do software, bem como em suas iterações entre usuário e programa. Após a criação e aceitação do protótipo, o produto final será desenvolvido.  


![spire_1](/media/processos_dev_software/spire_1.png)


**Modelo Espiral**: O Modelo espiral se assemelha com o propotipação, mas inclui um fator: a análise de risco. Funciona de forma iterativa, incremental, mas com uma etapa onde pode ser tomada a decisão de se interromper ou não o processo.



![spire_2](/media/processos_dev_software/spire_2.jpg)

# Aula 10 - O processo iterativo e incremental

### **Método Ágil**


É um conjunto de diretrizes e metodologias que cria uma estrutura conceitual para desenvolver projetos de desenvolvimento de software.


Baseado em um manifesto criado por programadores veteranos que já tinham passado por inúmeras experiências diferentes no campo de desenvolvimento de software, o Manifesto Ágil tem como foco as pessoas e não as ferramentas.  
[http://agilemanifesto.org/iso/ptbr/manifesto.html](http://agilemanifesto.org/iso/ptbr/manifesto.html)


### **Método XP**  
O modelo propõem uma série de práticas focados em pessoas, ou seja, na equipe de desenvolvimento.  
    1. Comunicação  
    2. Coragem  
    3. Feedback  
    4. Respeito  
    5. Simplicidade  


#### **Ciclo de um release em XP**  
Em XP, os requisitos são expressos em formas de cenários (chamados de histórias do usuário), que são implementados diretamente como uma série de tarefas. Os programadores trabalham em pares e desenvolvem testes para cada tarefa antes de escreverem o código. Quando o novo código é integrado ao sistema, todos os testes devem ser executados com sucesso.


![ciclo_xp](/media/processos_dev_software/ciclo_xp.png)


**Reuniões em pé**: Utilizadas para não perder o foco no assunto.  
**Programações em par**: Todo o código é implementado por uma dupla, usando o mesmo computador. Ambos com o objetivo de resolver o mesmo problema. Um terá o papel do condutor, digitando o código, e o outro o papel de navegador, com o objetivo de revisar o código de forma a evitar erros de programação ou sugerir melhores estratégicas de implementação.  
**Desenvolvimento guiado por testes**: Desenvolvimento guiado por testes: Trabalhar com teste automatizado de forma acompanhar se as funcionalidades implementadas atendem ao requisito e ao cliente. Dentre os testes podemos trabalhar com os testes de unidade e os testes de aceitação.  
**Posse coletiva**: O código fonte não pertence a ninguém, é de todos e todos podem utilizá-lo sem necessidade de permissão.  
**Pequenas versões**: Pequenas versões aceitas pelo cliente ajudam na aceitação do programa completo.  
**Ritmo sustentável**: Utilizar o tempo de trabalho dentro do especificado. Sem horas adicionais. ( 40 horas por semana ).  
**Padrão de codificação**: Após a formação da equipe, deverá ser estabelecida algumas regras, como o padrão de desenvolvimento a ser usado. A escolha de um padrão visa um rápido entendimento dos códigos uns dos outros.  


### **Método Scrum**  
Metodologia que tem como filosofia o Manifesto Ágil.  


Possui papel bem definido para as atividades durante todo o processo. Uma vez levantadas as questões a serem trabalhadas, é determinado um período de tempo para a realização de um determinado requisito.  


Durante esse intervalo, são feitas reuniões diárias para acompanhamento do andamento das atividades.


Os Três Pilares Fundamentais do Scrum  
* **Transparência**: Transparência dos processos, requisitos de entrega e status.  
* **Inspeção**: Inspeção constante de tudo o que está sendo realizado.  
* **Adaptação**: Adaptação, tanto do processo, quanto do produto às mudanças.  

![scrum_ciclo](/media/processos_dev_software/scrum_ciclo.png)

#### **Fundamentos Básicos do Scrum**


1. **Papéis**  
   1.1- Dono do Produto (Product Owner): É o responsável por gerenciar o Backlog do Produto e garantir o valor do trabalho executado pela Equipe de Desenvolvimento.  
   1.2 - Scrum Master: É a pessoa que mais conhece o Scrum dentre todos os papéis. Ele tem o papel de papel de facilitador, ajudando a equipe a resolver problemas, realizando melhorias no uso do Scrum, além de manter a equipe focada em suas tarefas. Vale ressaltar que o Scrum Master não é um gerente.  
   1.3 – Time de Desenvolvimento (Team Scrum): É a equipe (time) responsável pelo desenvolvimento do projeto. Os membros da equipe deve ser multidisciplinar e multifuncional, possuindo todo conhecimento necessário para a criar um incremento no trabalho. Geralmente o time de desenvolvimento é constituído por três a nove pessoas. Tanto o Scrum Master o Dono do Produto não estão incluídos no tamanho do Time de desenvolvimento.  


2. **Artefatos**  
   2.1 – Backlog do Produto: É um documento que contém todos os itens que devem ser desenvolvidos durante o projeto. Sendo o Dono do produto responsável por criar e manter este documento. É importante ressaltar que os itens do Backlog do Produto devem ser priorizados em função do Retorno do Investimento (ROI), onde os itens que apresentam maior valor para o negócio devem ser desenvolvidos primeiro.  
   2.2 – Backlog da Sprint: É um conjunto de itens selecionados para serem implementados durante a Sprint. Se durante o desenvolvimento da Sprint, for identifico a necessidade de novas tarefas ou a remoção de alguma tarefa, somente os membros do Time de Desenvolvimento podem realizar essa alteração no Backlog da Sprint.  
   2.3 – Incremento do Produto: Ao término de cada Sprint, o Time de Desenvolvimento entrega um incremento do produto, o qual é o resultado do que foi produzido durante a Sprint. Ao final de uma Sprint, uma funcionalidade só é considerada pronta depois de passar por todas as etapas determinadas pelo Time de Desenvolvimento. Caso a funcionalidade não tenha sido concluída, a mesma deve retornar ao Backlog do produto para que seja incluída em uma próxima sprint.  


3. **Cerimônias**  
   3.1 – Sprint: No Scrum, o trabalho é desenvolvido através de interações, denominadas Sprints. Cada Sprint tem duração de 2 a 4 semanas.  
   3.2 - Reunião de Planejamento da Sprint: Ocorre sempre no início de cada Sprint, com o objetivo de planejar o que será feito na Sprint.  
   3.3 - Reunião Diária: É uma reunião simples e importante, na qual cada membro do Time de Desenvolvimento deve responder sobre o que já fez, sobre o que pretende fazer e se há algum impedimento para a conclusão da tarefa sob sua responsabilidade. Geralmente essa reunião dura no máximo 15 minutos.  
   3.4 - Revisão da Sprint: Tem como objetivos apresentar o que a equipe fez durante a Sprint e entregar o produto ao Dono do Produto (Product Owner). Cabe ao Dono do Produto aceitar ou rejeitar a Sprint com base no que foi apresentado.  
   3.5 - Retrospectiva da Sprint: É uma reunião que tem como foco o aprimoramento do processo, analisando o que houve de bom e o que pode ser melhorado em uma Sprint. Todos os membros da equipe Scrum participa desta reunião.  



### **Processo unificado**

#### **Rup**  
Também conhecido como Rational Unified Process, é um processo que faz parte da engenharia de software.
Ele é baseado em disciplinas em que cada uma distribui tarefas e responsabilidades para os envolvidos no desenvolvimento do software.


Essas disciplinas são semelhantes às que estudamos anteriormente:  
 1. Modelagem de negócios;
 2. Implementação;
 3. Requisitos;
 4. Teste;
 5. Análise e Design;
 6. Implantação.


**Configuração e mudanças**: Acompanham mudanças, configurações e status/medições onde são armazenados e que servirão de base para o andamento do projeto.  
**Projeto**: Abrange questões como gestão de pessoas, orçamento, contratos.  
**Ambiente**: Atividades que dão suporte à equipe de desenvolvimento, como os itens de IT, servidores, ferramentas.  


Essas disciplinas têm suas responsabilidades e funções variadas, dependendo da fase que se encontra o projeto.


![rup](/media/processos_dev_software/rup.png)
