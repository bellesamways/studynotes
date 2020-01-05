# Aula 1

Sistema = conjunto de elementos inter-relacionados, cada qual desempenhando uma função, para, de forma integrada e coordenada, contribuir e garantir que o objetivo do sistema seja atingido.

![Sistema de Informação](/media/realimentação.png)

**Entrada** são os insumos de que o sistema precisa para atingir o seu objetivo.

**Processamento** é a execução dos procedimentos necessários ao bom funcionamento do sistema. Propicia a conversão da entrada bruta em forma mais útil e apropriada.

**Saída** é a apresentação do resultado ao ambiente externo gerado pelo sistema.

**Realimentação (ou feedback)** é a parte da saída do sistema que retorna ao próprio sistema com o objetivo de refinar ou corrigir os dados de entrada ou o processamento. É parte da saída produzida pelo sistema que informa sobre seu comportamento.

**Controle** refere-se ao monitoramento e avaliação do feedback, determinando se o sistema está atingindo o seu objetivo.

**Dado x Informação**

Dado: fato isolado em sua forma primária que não tem valor intrínseco.

Informação: conjunto de fatos (dados) organizados (processados) de tal forma que tenham valor agregado em si.

![Dado x Informação](/media/dados_informação.png)

## Sistema de informação

sistema cuja finalidade é PROVER INFORMAÇÃO a alguém na medida certa. Informação -> útil para quem recebe, possibilitando tomada de decisão.

**Sistemas de processamento de transação:** sistemas automatizaram os processos rotineiros,  úteis não só na redução de custos mas também em um melhor controle e eficiência das operações de rotina. Os SPTs provêm informações de cunho operacional, ajudando no melhor controle das operações.

**Sistemas de informação gerencial:** para a gestão das atividades a que se destinavam. Os SIGs provêm informações gerenciais aos supervisores, gerentes e cargos correlatos, apoiando as decisões que se fazem necessárias no dia a dia.

**Sistemas estratégicos:** visam a atender à demanda da direção das empresas (diretores, vice-presidentes e presidentes), ajudando a traçar as diretrizes estratégicas da organização.

![Sistema de informação](/media/sistema_informacao_piramide.png)
![Sistema de informação](/media/sistema_informacao_tabela.png)

## Tecnologia da informação

**Conjunto de recursos tecnológicos e computacionais para a geração e uso da informação**, ou seja, o  conjunto de recursos não humanos que desempenha uma ou mais tarefas de processamento das informações do SI tal como coletar, transmitir, armazenar, recuperar, manipular e exibir dados. Em sistemas de informação, a tecnologia da informação é fundamental, pois é o meio utilizado para alcançar os fins desejados.

    Tecnologia de informação (TI) é a infra-estrutura para os sistemas de informação (SI).

**Benefício da TI:** melhorar a qualidade e a disponibilidade de informações; aperfeiçoa ou adiciona eficiência; é um facilitador, não cria diretamente a satisfação.

**SI e TI não são sinônimos.**

## Características básicas dos SI

- Os sistemas estão inseridos em um contexto complexo; sofrem influẽncia do ambiente em que estão inseridos.

![Contexto dos SI](/media/contexto_sistemas_informacao.png)

- Os sistemas estão organizados em níveis hierárquicos. Os subsistemas são partes de um sistema maior que podem ser formados por outros subsistemas (hierarquia de níveis).

![Hierarquia dos SI](/media/hierarquia_sistemas_informacao.png)


### Teoria geral dos sistemas:

- Analisar a natureza dos sistemas e a relação entre suas partes;
- Identificar leis, propriedades e princípios característicos dos sistemas em geral;
- **Possui duas características relevantes:**
    - **Funcionalismo:** cada parte deve desempenhar uma parte da função maior
    - **Holismo:** o todo não é a simples soma das partes, o próprio sistema só pode ser explicado como um todo. Seus subsistemas e seus elementos estão inter-relacionados.

### Classificação de sistema:

- **Aberto ou fechado**
    - **Aberto:** interage com o seu ambiente; sofrem influências (positivas ou negativas) e influenciam o meio ambiente com suas ações.
    - **Fechado:** não possui interação com o ambiente.
- **Simples ou complexo**
    - **Simples:** possuem poucos componentes; relacionamento entre eles é simples e direto.
    - **Complexo:** muitos elementos altamente relacionados e interconectados.
- **Estável ou dinâmico**
    - **Estável:** mudanças no ambiente resultam em pouca ou nenhuma alteração no sistema.
    - **Dinâmico:** sofre rápidas e constantes mudanças em decorrência de mudanças no ambiente.
- **Adaptável ou não adaptável**
    - **Adaptável:** capaz de sofrer mudanças em resposta a mudanças no ambiente.
    - **Não adaptável:** não é capaz de mudar em resposta a mudanças no ambiente.
- **Permanente ou temporário**
    - **Permanente:** existe por um período de tempo relativamente longo.
    - **Temporário:** existe por um período de tempo relativamente curto.

### Propriedades fundamentais dos sistemas:
- **Entropia:** tendência de todos os sistemas fechados apresentarem, com o tempo, estado caótico ou aleatório, caminhando para a desordem e consequentemente declínio.
- **Equifinalidade:** sistemas abertos podem alcançar um estado constante de equilíbrio, de modo que não chegue a um repouso estático; certo estado final pode ser atingido de muitas maneiras e de vários pontos de partida diferentes.
- **Mecanismo de feedback:** correspondem a respostas a um descontrole externo.
- **Homeostase (autorregulação):** tendência ao equilíbrio, objetivando manter a constância durante um período de tempo.
- **Diferenciação e interação:** sistema deve ser adaptável e ser capaz de efetuar mudanças e reordenar-se, em resposta às pressões ambientais.
- **Hierarquias:** todo sistema compõe-se de sistemas de ordem inferior que fazem parte de um sistema de ordem superior.
- **Fronteiras:** separação entre o sistema e o meio ambiente e fixa o domínio em que deve ocorrer as atividades dos subsistemas. Toda organização possui fronteira, ou seja, uma determinação de seu campo de ação.
- **Inputs e outputs:** transforma um determidado tipo de entrada (input) em determinado tipo de saída (output). A ideia é definir para cada output desejado, prever o input necessário.

Principais componentes da plataforma de desenvolvimento Android:

- Activity: é um componente de aplicativo que fornece uma tela com a qual os usuários podem interagir para fazer algo, como discar um número no telefone, tirar uma foto, enviar um e-mail ou ver um mapa. Cada atividade recebe uma janela que exibe a interface do usuário. Geralmente, a janela preenche a tela, mas pode ser menor do que a tela e flutuar sobre outras janelas.

- Intent: é um objeto de mensagem que pode ser usado para solicitar uma ação de outro componente de aplicativo.

- Service: é o componente responsável pelo processamento em segundo plano associado a uma aplicação.

- Broadcast Receiver: são componentes responsáveis por receber e tratar eventos (broadcasts) provenientes do sistema ou de outras aplicações. É sempre executada em segundo plano.

- Content Provider: são componentes responsáveis por prover às aplicações o conteúdo que elas precisam para funcionar, ou seja, os dados. Permitem o compartilhamento de dados entre aplicações, centralizam as rotinas de armazenamento e recuperam em um único local.

# Aula 2

## Componentes dos sistemas de informação

![Componentes dos sistemas de informação](/media/componentes_sistemas_informação.png)

- **Recursos humanos:** pessoas que gerenciam, desenvolvem, mantêm e dão suporte aos sistemas e aos usuários. Ex: gestores, desenvolvimento e manutenção, suporte, usuários finais.
- **Hardware:** compreende os equipamentos físicos (hardware) e programas de computador (software). Entrada -> Processamento -> Saída
    - **Hardware de entrada:** equipamento que permite informar dados ao sistema. Ex: teclado, leitor de código de barras, etc.
    - **Hardware de processamento:** equipamentos responsáveis pelo processamento dos dados o sistema. Ex: CPU, memória RAM, etc.
    - **Hardware de saída:** responsável pela exibição das informações resultantes do processamento. Ex: monitor de vídeo, letreiros digitais, etc.
    - **Hardware de armazenamento:** responsável por reter os dados de entrada e/ou informações processadas de forma permanente. Ex: fitas magnéticas, HD, CD, etc.
- **Software:** compreende a parte lógica dos SI. Ex: desde planilhas eletrônicas, SO's que gerenciam o hardware, linguagens de programação até os próprios apps.
    - **Programa:** conjunto de instruções com sentido lógico e com objetivo em comum.
    - **Sistema:** conjunto de programas que, de forma integrada e organizada, realiza cada qual uma tarefa específica do sistema.
- **Recursos de (armazenamento de) dados:** meios físicos (mídias) para armazenamento, não só de dados como também do software.
- **Recursos de rede:** meios de transmissão e comunicação de dados entre computadores conectados em uma rede. Ex: internet.
- **Procedimentos:** compreendem as estratégias, os métodos, as técnicas e as regras usadas pelas pessoas para operarem o SI. Procedimentos que descrevem e orientam como os SI devem ser usados e inseridos em seus contextos de uso.

## Como ocorre a transformação de dados em informação?

Ocorre através de um processo que pode ser definido como um conjunto de tarefas logicamente relacionadas e executadas para atingir um objetivo claramente definido.

![Transformação de dados em informação](/media/transformacao_dados_informacao.png)

Requer conhecimento (regras, procedimentos e diretrizes) para selecionar, organizar e manipular os dados, gerando informações úteis dentro de um contexto.

**Informação precisa ter qualidades:**
- **Precisa:** não tem erros, exata para quem deseja.
- **Completa:** contém todos os fatos relevantes.
- **Confiável:** geralmente a confiabilidade depende da fonte da informação.
- **Relevante:** é importante para o tomador de decisão.
- **Em tempo:** enviada no momento necessário.
- **Econômica:** custo da informação não deve ser maior que os benefícios que causam aos tomadores de decisão.

![Níveis e retroalimentação entre Sistemas de Informação](/media/alimentacao_informacao_dado.png)

1. Um sistema pode estar relacionado com mais de um nível, quanto mais níveis ele abranger, maior sua integração na organização.
2. Uma informação gerada em um nível (operacional ou gerencial) pode ser dado no nível imediatamente superior (gerencial ou estratégico)

## Os diferentes tipos de sistemas de informação

Um sistema de informação integrado provê informação a todos os segmentos:

![Funções empresariais dos SI](/media/funcoes_empresariais_si.png)

### Sistemas de informação de vendas e marketing

![Sistemas de Marketing e Vendas](/media/marketing_vendas_si.png)

#### Componentes de sistemas de informação para operações dos pontos de venda (PDV).

![Exemplo de um Sistema de Informação de Vendas](/media/vendas_si.png)

![Sistemas de Apoio ao Executivo](/media/sae_si.png)

## Controle e desempenho de sistemas

Um sistema precisa ser constantemente monitorado para avaliar se o seu nível de desempenho se mantém estável ao longo do tempo em suas inúmeras execuções.

- Desempenho é medido por sua eficiência.
- Sistema eficaz é aquele que atinge seus objetivos.
- É dito eficiente se é eficaz, ou seja, se atinge seus objetivos e o faz com o menor uso de recursos possíveis.
- Um sistema deve manter de forma estável o seu nível de desempenho ou eficiência.

Problemas externos podem influenciar no nível de eficiência de um sistema:

- refrigeração
- disco rígido cheio
- nível de acesso e uso do sistema
- congestionamento na rede
- rede sem fio com sinais em flutuação
- rede elétrica com picos ou ausência de corrente
- base de dados sobrecarregada

Solução é o monitoramento frequente para identificar de forma proativa os possíveis elementos que podem influenciar a sua performance.

# Aula 3

![Evolução dos SI](/media/evolucao_si.png)

- **SIG:** pega os dados já tratados nas informações geradas pelo SPT, começa a gerar informações para o controle gerencial facilitando o nível tático.
- **SAD:** dados mais heterogêneos, permite tomar novas decisões a partir do que consegue detectar pelo próprio SIG. Auxilio na tomada de decisões, estratégicas ou táticas.
- **SIE:** especialista na produtividade, permite visão de mercado, dados heterogêneos e permite combinar dados internos e externos. É o mais heterogêneo de todos.
- **Internet:** o que era estratégico antes em nível pequeno, começou a ser em nível global.

- **Sistemas de Processamento de Transações (SPTs)** = os primeiros sistemas visavam a oferecer suporte aos processos e às operações das empresas. Tais sistemas tinham basicamente o objetivo de assegurar a eficácia (ato de alcançar a meta desejada) e a eficiência (ato de alcançar a meta desejada valendo-se do menor número possível de recursos) dos processos ora informatizados.
- **Sistemas de Informação Gerencial (SIGs)** = necessidade de organizar melhor a informação focando-a no auxílio do processo decisório (tomada de decisão) não só das pessoas que exerciam os cargos gerenciais mas também daquelas que, em qualquer nível, tomavam decisões no dia a dia.
- **Sistemas de Informações Estratégicas (SIEs)** = apoiavam a solução de questões relacionadas à obtenção de vantagem competitiva da empresa (capacidade de competir com seus concorrentes) no mercado em que atuavam.

![Tipos de SI](/media/tipos_si.png)

**Nível do Conhecimento** = trata de problemas que envolvem conhecimento e especialidade técnica que abrangem uma ampla variedade de questões:

- Onde deveriam estar localizadas as fábricas?
- Como deveria ser feito o treinamento?
- Que sistemas de informação deveriam ser empregados?

Problemas do conhecimento são pertinentes a áreas que **criam, distribuem e usam** conhecimento e informações em prol da empresa.

![Níveis e Tipos de SI](/media/niveis_si.png)

### Classificação por Nível e Área

![Classificação por Nível e Área](/media/classificacao_nivel_area_si.png)

## Os tipos de sistemas de informação
### Nível operacional

**Sistemas de Processamento de Transação (SPTs) monitoram as atividades (transações) diárias da empresa.**

O que são transações? É o registro de um evento ao qual a empresa deve responder. A transação aciona toda uma série de eventos que atualizam os registros comerciais da empresa e produzem os documentos apropriados.

- Os Sistemas administrativos básicos atendem ao nível operacional.
- Os Sistemas computadorizados realizam e registram as transações rotineiras necessárias ao funcionamento da empresa.

Existem 2 formas de processamento das transações:

**Batch (ou Lote):** As transações são coletadas e processadas juntas; ficam acumuladas por determinado período de tempo, aguardando o processamento como uma única unidade ou lote; o tempo entre o processamento dos lotes pode variar em função do tempo necessário para atender às necessidades do usuário; a característica essencial está no atraso entre a ocorrência do evento e o processamento da transação. Exemplo: Folha de pagamento.

**Online (OLTP):** A transação é processada imediatamente e por completo no ato de sua ocorrência; tão logo a entrada esteja disponível, o processamento é executado; ele atualiza os registros afetados pela transação. (Essencial para negócios que exijam rapidez e atualização frequente dos dados.) Exemplos: sistema de tráfego aéreo, sistemas PDV (ponto de venda), comércio pela internet.

### Nível gerencial

1. **Sistema de Informação Gerencial (SIG)**

- O propósito de um SIG é ajudar a empresa a alcançar suas metas, fornecendo a seus gerentes detalhes sobre as operações regulares da empresa para que possam controlar, organizar e planejar (princípios básicos da administração) com mais efetividade e com mais eficiência.
- Oferece relatórios e consultas predefinidas.

![Sistema de Informação Gerencial (SIG)](/media/sig_si.png)


2. **Sistema de Apoio à Decisão (SAD)**

- Fornece suporte (computacional) interativo e direto aos gestores durante o processo de decisão.

### Nível estratégico

- **Sistema de Informação Executiva (SIE) ou Sistema de Informação Estratégica**

    - Fornece informações condensadas em quadros de fácil visualização, relacionadas aos fatores críticos da organização.
    - Altos executivos podem acessar, de suas estações de trabalho, textos e gráficos que destaquem aspectos de relevância da empresa e da concorrência.

- **Outra classificação dos sistemas de informação**

A tabela abaixo mostra nova forma de classificar e agrupar Sistemas de Informação.

![Outra classificação dos sistemas de informação](/media/si_sao_sag.png)

- **Sistema de Controle de Processos**

Monitora e controla processos físicos. Na construção civil, é cada vez mais frequente a automação de determinados processos. Por exemplo, controle de elevadores ou de acionamento/parada de bombas de água.

- **Sistemas Colaborativos**

Visam melhorar a comunicação e a produtividade em equipes e grupos de trabalho dentro das empresas e entre elas. Por exemplo, o uso de videoconferência e de aulas telepresenciais.

- **Outros tipos de sistemas de informação**

Abaixo, alguns tipos de Sistemas de Informação que não foram citados nas classificações apresentadas.

![Outros tipos de sistemas de informação](/media/fase_caracteristicas_si.png)

# Aula 4

![E-business](/media/e-business.png)

Possibilidades dentro da internet:
- Comunicação com demais pessoas no mundo
- Colaboração em conversas, trabalhos, etc
- Acessar informações
- Fornecimento de informações
- Diversão
- Transações

## Intranet x internet x extranet

- **Intranet:** uma rede interna, local à organização, construída sob a estrutura da internet
- **Extranet:** é o acesso externo (pela internet) à intranet de uma empresa.
- **Internet:**
![Internet](/media/internet_si.png)

**Problemas estruturados** são aqueles perfeitamente definidos onde suas variáveis são conhecidas e, por isso, já existe uma metodologia para se chegar à solução.
- Apoiados pelo SIG.
- Rotina e repetição.
- Principais características: facilmente automatizados; todos os dados relevantes estão disponíveis; necessitam de pouco julgamento ou avaliação.

**Problema semiestruturado** é aquele em que parte da solução tem suas variáveis conhecidas e uma metodologia de solução definida.
- Demanda pelo SAD
- Principais características: Algumas partes podem ser automatizadas; o grau de estruturação não é a complexidade do problema, já que problemas complexos podem ser decompostos.

**Problema não estruturado** não pode ser claramente definido já que uma ou mais de suas variáveis são desconhecidas ou não podem ser determinadas com grau de confiança.
- Apoiados pelo SIE.
- Presentam sempre uma novidade. Não são problemas rotineiros e não possuem procedimento para solucioná-los.
- Principais características: alguns dados indisponíveis; necessitam julgamento humano (subjetividade e criatividade); Dificilmente automatizados.

## O processamento analítico online (OLAP)

Permite acessar e manusear, interativamente, grande quantidade de dados detalhados e consolidados a partir de uma ampla variedade de perspectivas.

O processamento OLAP ocorre em tempo real em resposta às consultas dos gestores e envolve basicamente as seguintes operações:

**Consolidação:**
- Agrupa dados.
- Considere a atuação de uma grande rede de lojas de varejo. Os dados de vendas podem ser agrupados por cidades e estas reunidas em regiões.
**Drill-down:**
- Desagrega os dados, ou seja, exibe os detalhes dos itens anteriormente agrupados (consolidados).
- Seguindo o mesmo exemplo da rede de lojas, que uma determinada região apresenta um resultado abaixo da média da empresa como um todo. A partir da operação de Drill-down, o gestor pode identificar as vendas da(s) cidade(s) que opera(m) abaixo da média.
**Slicing and Dicing:**
- Que significa “fatiar em cubos”.
- Os dados contidos em um banco de dados podem ser considerados sob diversas perspectivas
- Uma fatia do banco de dados pode mostrar as vendas por tipo de produto dentro de cada região. Uma outra fatia pode mostrar os totais de vendas por canal de venda (loja, internet, distribuidor e etc.).
- Sua principal finalidade é a análise de tendências e descobrimento de padrões essenciais na identificação do perfil dos clientes das lojas.

![SIGs x SADs](/media/sig_sad.png)

### As 4 Modelagens do SAD

![As 4 Modelagens do SAD](/media/modelagens_sad.png)

### Sistemas de Informação Geográfica

![Sistemas de Informação Geográfica](/media/sigs.png)

### Sistemas de Informações a Executivos (SIE)

Visam atender à demanda de informação do alto escalão da empresa que, preocupado com as decisões estratégicas de longo prazo, definirão o rumo da organização nos anos que se seguem.

![Sistemas de Informações a Executivos](/media/sies.png)

![Tipos de Sistemas de Informações a Executivos](/media/tipos_sies.png)

**Data Mining ou Mineração de Dados:** Analisando dados históricos e grandes volumes de dados a tecnologia de mineração tem como uma das características a busca por padrões comportamentais dos dados.

[Cinco forças de Michael Porter](https://blog.egestor.com.br/5-forcas-de-michael-porter/)

# Aula 5

O objetivo da Inteligência Artificial é fazer com que os computadores e seus respectivos sistemas aplicativos possam pensar, raciocinar, agir, ver, ouvir, falar e sentir, ou seja, fazer uso dos cinco sentidos e das qualidades cognitivas do homem (raciocinar, aprender e solucionar problemas).

- **Aplicações da IA:**  utilização de recursos computacionais baseados em conhecimentos e não mais em sistemas de informações gerenciais onde o homem estuda todas as informações e, com sua própria experiência, toma decisões. A ideia é que a decisão fique a cargo dos sistemas dotados de “inteligência”.
- **Objetivos da IA:** propiciar o desenvolvimento de ferramentas capazes de melhorar as operações empresariais e aumentar a sua vantagem competitiva.
- **Aplicações em uso:**
    - Sistemas Especialistas.
    - Processamento de linguagem natural (um dos maiores desafios !).
    - Reconhecimento de imagem (Muito utilizado pela Medicina).
    - Reconhecimento de voz, e etc.

## Domínios da IA

![Domínios da IA](/media/dominios_ia.jpg)

- **Data Warehouse (armazém de dados):** É um banco de dados que armazena dados sobre as operações da empresa (vendas, compras, etc.), extraídos de uma fonte única ou múltipla, e transforma-os em informações úteis, oferecendo um enfoque histórico para permitir um suporte efetivo à decisão.
- **Redes neurais:** montar uma rede de neurônios de forma a simular o funcionamento do cérebro humano. As redes neurais visam solucionar problemas através da simulação do cérebro humano, inclusive em seu comportamento (aprendendo, errando e fazendo descobertas).
    - A interconexão da rede neural permite o processamento em paralelo e a interação dinâmica.
    - A rede pode, então, “Aprender” a partir dos dados processados.
    - O sistema computacional aprende a reconhecer padrões e relações nos dados que processa.
    - Quanto mais dados de entrada, melhor é o aprendizado.
- **Sistemas de Lógica Difusa:** com base na teoria dos Conjuntos Nebulosos, tem se mostrado mais adequada para tratar imperfeições da informação do que a teoria das probabilidades.
- **Algoritmos genéticos:** úteis para situações nas quais milhares de soluções são possíveis e precisam ser avaliadas para a escolha de uma solução ótima. O software de algoritmo genético utiliza um conjunto de regras de processo matemático que especificam como a combinação de componentes deve ser feita.
- **Realidade virtual (VR):** As aplicações são voltadas para simular a realidade em ambientes computacionais e desenvolver interfaces homem-máquina. A RV utiliza dispositivos multissensoriais com instrumentos de entrada e saída capazes de acompanhar e monitorar os movimentos humanos de forma que os mesmos possam ser imitados ou simulados pelas máquinas.
- **Agentes inteligentes:** são programas de software que realizam tarefas específicas, repetitivas e procedurais para o ser humano: percebem o ambiente e agem sobre ele.

## Conceitos básicos de Sistemas Especialistas (SE)

São aplicações da IA, representadas por softwares que simulam o comportamento de um especialista para a solução de problemas.

![Conceitos básicos de Sistemas Especialistas](/media/conceitos_sistemas_especialistas.jpg)

### Partes de um Sistema Especialista

![Partes de um Sistema Especialista](/media/partes_sistemas_especialistas.jpg)

- **Base do Conhecimento:** contém o conhecimento do domínio. O conhecimento é armazenado sob a forma de regras.
- **Memória de Trabalho:** contém os sintomas do problema que são descobertos durante a sessão de consulta. Contém todas as informações sobre o problema que são fornecidas pelo usuário ou inferidas pelo sistema.
- **Motor de Inferência:** processador em um sistema especialista que confronta os fatos contidos na memória de trabalho com os conhecimentos de domínio contidos na base de conhecimento para tirar conclusões sobre o problema.
- **Funcionamento:**
    - O M.I. trabalha com os fatos contidos na memória de trabalho e o conhecimento de domínio contido na base de conhecimento para derivar uma nova informação. Ele procura as regras para um casamento entre as suas premissas e as informações contidas na memória de trabalho. Quando o M.I. encontra um casamento, adiciona a conclusão da regra na memória de trabalho e continua.
    - O motor de inferência é um elemento essencial para a existência de um sistema especialista. É o núcleo do sistema.
    - É por intermédio dele que os fatos, as regras e a heurística que compõem a base de conhecimento são aplicados no processo de resolução do problema.

![Conteúdo sobre Sistemas Especialistas](/media/sobre_sistemas_especialistas.png)

# Aula 6

O comércio eletrônico ou e-commerce é um tipo de transação comercial feita por um equipamento eletrônico,como um computador.

De uma maneira geral, pode-se dizer que o comércio eletrônico usa recursos de internet, extranet, intranet e redes corporativas das empresas.

Pode-se definir o Comércio Eletrônico como aquele que envolve o intercâmbio de bens físicos e não tangíveis (como informação ou um software) através de etapas que se iniciam com o marketing online e com o gerenciamento dos pedidos, do pagamento, da distribuição e dos serviços de pós-venda.

A venda de produtos pela internet não demanda apenas a tecnologia para venda ao cliente, mas toda a estrutura necessária para receber e atender ao pedido que inclui: efetivar a compra dos fornecedores, armazenar os itens comprados (para entrega imediata ou estocagem)  e toda a logística de entrega ao cliente que pode estar em qualquer local do mundo. Além da reestrutura da própria organização, foi preciso uma integração com os fornecedores no sentido de estarem alinhados para atendimento às demandas do e-commerce.

![Fase: Organização e automação dos processos básicos de negócio](/media/fase_organizacao_automacao.png)

A necessidade do setor em oferecer segurança para as transações bancárias demandou maciço investimento em tecnologias de segurança, como criptografia e transferência eletrônica de fundos.

Canais para a realização do comércio:
1. Pessoal
2. Correio
3. Telefone
4. Internet

- **e-business:** O e-business pode ser definido como “uma estratégia de inserção da empresa na Internet, visando automatizar suas atividades em diversas áreas, como as comunicações internas e externas, a transmissão de dados, os controles internos, o treinamento de pessoal, os contatos com fornecedores e clientes, etc.”, ou ainda, sistemas de informação que auxiliam os processos do negócio.
- **e-commerce**: O e-commerce ou simplesmente comércio eletrônico é parte integrante do e-business, constituindo “a atividade comercial, alavancada pela internet que faz a conexão eletrônica entre a empresa e o cliente, ou seja, qualquer forma de transação de negócios na qual as partes interagem eletronicamente, sem o contato físico direto”.

Não só de aspectos tecnológicos vive o e-commerce. É necessária uma estrutura organizacional que envolve:

- **Marketing:** As empresas precisam investir em marketing de forma que seus clientes tenham conhecimento dos produtos e serviços que elas oferecem via internet.
- **Compra:** O processo de compra dos produtos que as empresas comercializam deve estar muito bem definido e alinhado com os fornecedores. A pontualidade na entrega é um dos fatores de qualidade que deve ser preservado no comércio eletrônico.
- **Venda:** Processo de venda online deve estar muito bem estruturado e preferencialmente personalizado (pelo perfil captado de suas últimas compras) ao cliente. É fundamental que sejam usadas tecnologias para identificação de perfil e características de consumo (por exemplo, datamining).
- **Assistência:** Deve acontecer para auxílio ao cliente antes (dúvidas e entendimento do produto ou serviço) e depois da realização da venda (pós-venda), com a implementação de serviços de Fale Conosco e Chat, por exemplo.

Atualmente, o comércio varejista está reagindo ao aumento do volume de vendas e da competição acirrada online, acrescentando características importantes a seus sites de e-commerce, a fim de torná-los mais atraentes e encorajar os clientes a comprar online através:

- Da inserção de imagens 3-D para exibição de portfólio de produtos.
- Personalização de serviços, como recomendações especializadas por cliente, conforme seu perfil de compra (análise das últimas compras).
- Busca avançada de produtos e serviços.
- SAC online para atendimento às dúvidas, às reclamações, às sugestões e às solicitações de seus clientes.

![Fase final do processo](/media/fase_final.jpg)
![Comércio Colaborativo](/media/comercio_colaborativo.jpg)

De uma forma geral, a tecnologia usada no comércio eletrônico compõe-se:
- Da tecnologia usada nas redes corporativas das empresas (hardware, software, bancos de dados, etc.) que não é visível aos usuários.
- Dos canais de banda larga de internet, oferecidos pelas empresas de telecomunicações.
- De um conjunto de tecnologias de software voltado à demanda de aplicações de comércio através da internet.
- De implementações de segurança usados nas transações online que inclui recursos de hardware e software, como firewall (proteção de acessos externos a redes corporativas), criptografia, servidores seguros, certificados digitais e outras tecnologias.

- Tecnologia cliente/servidor de gerenciamento de rede.
- Sistema de Gerenciamento de banco de dados (SGBD), como MySql, Oracle e SQL Server, como sendo o mais usado.
- Linguagens de programação, como HTML, XML, Java, C#.
- Servlets e páginas de servidor com script, como Microsoft Active Server Pages, Java Server Pages.
- Protocolos de comunicação de objetos, como a Arquitetura de Intermediador de Solicitação de Objeto Comum (CORBA) desenvolvida pelo OMG, o padrão Java de Chamada de Método Remoto (RMI) ou o Modelo de Objeto Componente Distribuído (DCOM) da Microsoft Componentes, como o Microsoft ActiveX/COM.
- Frameworks de aplicativos para a Web, como o IBM WebSphere ou o Microsoft Windows DNA.

## B2B: Business-to-Business

Compreende as transações entre organizações. Uma empresa vendendo para outra empresa é B2B. Por exemplo, fábricas vendendo para distribuidores, ou empresa prestando algum tipo de serviço para outra. É o típico caso de comércio por atacado.

O B2B aplica-se às transações entre empresas, podendo ser de produtos ou serviços.

O B2B pode ser definido como a realização de transações entre companhias. Por exemplo, o comércio atacadista, a compra de serviços, as tecnologias, os equipamentos, os componentes e as transações financeiras.

Na perspectiva B2B, o Comércio Eletrônico facilita as aplicações de negócios, beneficiando o gerenciamento de fornecedores, estoque, distribuição, canal e pagamento.

## B2C: Business-to-Consumer

Corresponde às transações entre a organização e o cliente final – pessoa física.

Com a economia mundial em recessão, o foco da maioria das empresas, incluindo as de comércio eletrônico (B2C), é cortar custos. O retorno financeiro é a prioridade das empresas engajadas no comércio eletrônico. As empresas tradicionais estão investindo em projetos de comércio eletrônico apenas quando decididamente o seu retorno financeiro é garantido, ao contrário do que ocorreu no passado recente, quando até o medo de se tornarem obsoletas as fez investir cegamente em projetos de comércio eletrônico.

No B2C, o consumidor tem acesso a informações sobre produtos a partir de catálogos eletrônicos e realiza suas compras por meio de sistemas de pagamento seguro; pode interagir diretamente com diversos vendedores do mundo, negociar preços e serviços de suporte, comparar ofertas, obter informações sobre produtos e, ainda, ter acesso a produtos customizados e personalizados que melhor atendam às suas necessidades.

A fórmula do sucesso para o e-commerce do tipo B2C é oferecer produtos e serviços, com preços e condições de pagamento mais acessíveis ao cliente.

## C2C: Consumer-to-Consumer

Corresponde às transações entre consumidores, normalmente intermediado por uma empresa.

Em Wikipédia, você encontra a definição para C2C (do inglês Consumer to Consumer) como sendo uma referência ao comércio eletrônico que se desenvolve entre usuários particulares da Internet. Aqui o comércio de bens ou serviços não envolve produtores e sim consumidores finais, nas 2 (duas) pontas. Esse tipo de transação entre consumidores está associada à transação direta, com a ajuda (ou a intermediação) de alguma empresa. Um grande exemplo desse tipo de transação são os leilões online, como Ebay e o Mercado Livre. Os leilões online funcionam da seguinte forma: o consumidor coloca o seu produto para venda com um valor mínimo, e outros consumidores dão ofertas maiores para aquele produto. Quem der o maior lance, num prazo determinado, leva o produto. As empresas que facilitam essa transação geralmente ganham uma comissão em cima de cada leilão ou uma taxa única de transação. É bom lembrar que esses sites são apenas intermediários e não se envolvem na qualidade do produto ou não influenciam nos valores dos produtos.

Com a popularização das lojas virtuais, estas, além de oferecerem produtos aos clientes com acesso fácil e simples, também apresentam uma peculiaridade que é o funcionamento ininterrupto, com segurança, uma vez que suas páginas eletrônicas podem ser acessadas a qualquer horário do dia ou da noite, independentemente das diferenças de fuso horário entre cidades ou países.

Dessa forma, manter a infraestrutura computacional funcionando ininterrupta e corretamente, nesses tipos de sistemas, é um dos pré-requisitos para a sobrevivência dos negócios, visto que os usuários, no caso da inacessibilidade da página eletrônica em questão, estão “a um clique do site do concorrente”.

---

Um recurso de segurança muito popular é o Secure Socket Layer (SSL), comercializado pela Certisign, no Brasil. Esse protocolo garante a privacidade da transação, pois as informações transmitidas são criptografadas e somente o usuário e o servidor da empresa envolvidos no processo podem decodificar seu conteúdo.

No contexto do e-commerce, o **gerenciamento de fluxo de atividades** é de fundamental importância, pois é onde são controlados os  principais recursos voltados para o controle e automação do fluxo de trabalho, garantindo eficácia e eficiência ao processo como um todo.

Os **processos de notificação de eventos** desempenham um importante papel nas aplicações do comércio eletrônico, porque todos os envolvidos nesse tipo de serviço (funcionários, fornecedores, clientes, etc.) precisam ser notificados sobre a situação de cada evento que ocorre em cada processo da transação comercial.

No processo de desenho do negócio, um dos pontos cruciais é a implementação da logística de entrega. A compra é virtual, porém o produto não o é, assim como sua entrega, manuseio e uso. Da mesma forma, o processo de devolução deve ser bem definido e bem explicado, preferencialmente antes da conclusão da compra. Prever soluções para a retomada de mercadorias não é trivial e sua falha ou ineficiência pode ser custosa. O manuseio da mercadoria devolvida também é real, envolvendo uma série de procedimentos de controle e gerenciamento. É importante cadastrar a mercadoria devolvida, registrar quem a devolveu, quando e o porquê, como maneira de saber quem são os clientes mal-intencionados.

O **gerenciamento efetivo do processo de cobrança vale mais a pena para os grandes cobradores**: empresas de telecomunicações, instituições financeiras etc., uma vez que existem cuidados com segurança que não são fáceis e nem baratos de serem implementados e acompanhados.

Assim sendo, devido ao nível de complexidade envolvido, uma das estratégias é utilizar-se de serviços de provedores que disponibilizam aplicações (Application Service Provider - ASP) especializadas e preparadas para acompanhar e controlar todas as fases do processo de cobrança. Muitas vezes, o processo é gerenciado por um centro especializado no processo de cobrança.

Assim, a empresa usuária desse sistema precisa apenas incluir nas suas páginas algumas diretivas específicas que encaminharão o cliente para o provedor do serviço de cobrança que saberá como lidar com questões relativas às autenticações, à confirmação de dados comerciais, à segurança e privacidade. Normalmente, para cada cobrança efetivamente realizada, uma taxa é cobrada da empresa-cliente.
