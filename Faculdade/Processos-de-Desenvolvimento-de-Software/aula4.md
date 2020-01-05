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