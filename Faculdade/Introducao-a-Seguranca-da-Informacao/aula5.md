## Aula 5 - Gestão de risco 

 

Atualmente, há cada vez mais informações valiosas disponíveis no computador e na internet. Por isso, a cada dia que passa, surgem novas e mais elaboradas formas de ameaça à segurança da informação – e elas estão mais perto de nós do que imaginamos. 

Alguns elementos associados à segurança da informação são: 
- Vulnerabilidades (pontos fracos) 
- Ameaças (como vírus e cavalos de Troia) 
- Riscos (a chance de um ataque ocorrer e um dano ser causado) 


Compreender esses elementos é fundamental para que qualquer usuário aprenda a se proteger. Obter tal conhecimento se revela ainda mais importante para os estudantes de computação. 

 

Assim sendo, percebemos a importância do estudo sobre os elementos associados à segurança da informação para os envolvidos em gestão de dados e áreas afins. 

 

### Segurança da informação 

 

Pilares 

Para identificarmos a quais riscos um ativo de informação pode estar submetido, precisaremos, antes disso, estudar alguns termos e conceitos relacionados à preservação dos seguintes pilares da segurança da informação: 

![Pilares](media/introducao-a-seguranca-da-informacao/pilares.png)

Disponibilizem uma informação para pessoas, entidades ou processos não autorizados (confidencialidade). 

Afetem a exatidão e a integralidade de ativos (integridade). 

Tornem os recursos inacessíveis e inutilizáveis sob demanda (disponibilidade). 

 

Esmiuçaremos a seguir todos os elementos desta figura: 

![Impacto a organização](media/introducao-a-seguranca-da-informacao/impacto-a-organizacao.png)

Ativos 

Toda empresa possui seus ativos, ou seja, algo que possui valor para a organização. Exibiremos a seguir alguns de seus exemplos: 

 
 

1. Ativos de informação: Base de dados, arquivos, contratos e acordos; 

 
 

2. Ativos de software: Aplicativos e sistemas; 

 
 

3. Ativos físicos: Equipamentos computacionais e de comunicação; 

 
 

4. Serviços: Eletricidade e refrigeração; 

 
 

5. Pessoas: Suas qualificações, habilidades e experiências; 

 
 

6. Intangíveis: Aqueles não podemos tocar, como a reputação e a imagem da organização. 

 
 

Ameaças 

Em seu item 3.74, a norma ISO/IEC 27000:2018 define ameaça como “a causa potencial de um incidente indesejado que pode resultar em dano para um sistema ou organização por meio da quebra de segurança”. 

Nenhuma organização deseja que qualquer tipo de ativo sofra algum dano ou furto. No entanto, justamente pelo fato de possuírem uma percepção de valor, os ativos estão sujeitos a ameaças de várias naturezas. Elas podem ser: 

Físicas 

Falhas de equipamentos e instalações, como relâmpagos, terremotos, ataques a bomba, deterioração dos meios de armazenamento, fraude, roubo, invasão etc. 

Lógicas 

<i>Vulnerabilidades em softwares, como bugs, vírus, malwares etc.</i>

 

Note que o contrário de ameaça é oportunidade, cujo significado é: “Ocasião favorável; circunstância oportuna e propícia para a realização de alguma coisa; ensejo”. (MICHAELIS, 2020) 

Podemos então reescrever o conceito de oportunidade como a causa potencial de um incidente desejado que pode resultar em ganho para um sistema ou uma organização 

 

#### Medidas de proteção (controle) 

<center>Certas ameaças rondam os ativos a todo instante. </center>

Como uma organização deseja mantê-los a salvo, deve adotar medidas de proteção (controle) para esconder ou diminuir o acesso ou a exposição às vulnerabilidades deles. 

 

Segundo o item 3.14 da norma ISO/IEC 27000:2018, controle é uma medida que pode modificar o risco por meio de um processo, política, dispositivo, prática ou outras ações que modifiquem a ameaça e/ou a vulnerabilidade e, consequentemente, o risco. 

 

#### Vulnerabilidades 

 

A vulnerabilidade “é uma fragilidade de um ativo ou grupo de ativos que pode ser explorada por uma ou mais ameaças e, por consequência, comprometer a segurança de sistemas ou informações”. A identificação dela em um ativo, porém, não é um processo trivial. 

 

Desse modo, deve-se inicialmente realizar uma análise de vulnerabilidades, que é o processo de levantar falhas ou ausências em um conjunto de proteções adotadas. Em seguida, a avaliação de vulnerabilidades é feita com uma lista de ameaças no intuito de avaliar sua probabilidade de ocorrência. 

 

A tabela a seguir apresenta alguns exemplos de ameaças, vulnerabilidades e medidas de controle cabíveis: 

![Tabela de ameaças](media/introducao-a-seguranca-da-informacao/tabela-ameacas.png)

#### Incidente 

 

Nenhuma medida de proteção é infalível. Portanto, uma ameaça pode explorar uma ou mais vulnerabilidades não cobertas pelas medidas de proteção adotadas. Quando uma delas ocorre, há um incidente de segurança da informação. 

 

O conceito de incidente de segurança da informação é definido pelo item 3.31 da norma ISO/IEC 27000:2018 como um “evento ou série de eventos indesejados ou inesperados que provavelmente comprometerão as operações da empresa ou ameaçam a segurança da informação”. 

 

#### Evento 

 

Um evento de segurança da informação não implica necessariamente um incidente de segurança da informação. Com base no item 3.30 da norma ISO/IEC 27000:2018, um evento de segurança da informação significa uma “ocorrência identificada de um estado de rede, serviço ou sistema que indique uma possível falha da política de segurança ou falha das salvaguardas, ou mesmo uma situação até então desconhecida que pode se tornar relevante em termos de segurança”. 

 

Impacto 

Já sabemos que uma ameaça explora vulnerabilidade(s) de um ativo e causa um incidente de segurança da informação. Tal incidente, por sua vez, pode gerar um impacto na organização. Segundo a norma ISO/IEC 27000:2018, “ele é caracterizado como uma mudança não desejável nos objetivos de negócios”. 

Risco 

É caracterizado no item 3.61 da norma ISO/IEC 27000:2018 como a combinação das consequências de um evento (incluindo mudanças nas circunstâncias) e de sua probabilidade associada de ocorrência. 

 

### Sistemas de gestão 

 

#### Sistemas de Gestão de Riscos (SGR) 

<center>Você já ouviu falar em SGR? </center>

Trata-se do conjunto de práticas e procedimentos utilizado para gerenciar os riscos. 

Tanto a ocorrência de um incidente de segurança da informação quanto o impacto causado por seu incidente poderão ser minimizados se uma organização adotar um SGR. Sua aplicação é importante a fim de diminuir possíveis danos e prejuízos causados por eventuais incidentes para: 

![SGR](media/introducao-a-seguranca-da-informacao/sgr.png)

#### Sistema de Gestão de Segurança da Informação (SGSI) 

De acordo com a norma ABNT NBR ISO/IEC 27001, o processo de gestão de riscos de segurança da informação deve atender aos requisitos de um SGSI. 

 

### resumo dos termos e das definições relacionadas à segurança da informação. 

 

1. Controle 

(ISO/IEC 27000:2018, item 3.14) 

Medida que pode modificar o risco por meio de um processo, política, dispositivo, prática ou outras ações que modifiquem a ameaça e/ou a vulnerabilidade – e, consequentemente, o risco. 

 

2. Ameaça 

(ISO/IEC 27000:2018, item 3.74) 

Causa potencial de um incidente indesejado, podendo resultar em dano para um sistema ou uma organização por meio da quebra de segurança. 

 

3. Vulnerabilidade 

(ISO/IEC 27000:2018, item 3.77) 

Fragilidade de um ativo ou grupo de ativos que pode ser explorada por uma ou mais ameaças e, por consequência, comprometer a segurança de sistemas ou informações. 

 

4. Análise de vulnerabilidades 

Processo de levantar falhas ou ausências em um conjunto de proteções. 

 
5. Avaliação de vulnerabilidades 

Combinação da análise e de uma lista de ameaças para avaliar a probabilidade de elas ocorrerem. 

 

6. Evento de segurança da informação 

(ISO/IEC 27000:2018, item 3.30) 

Ocorrência identificada de um estado de rede, serviço ou sistema que indique uma possível falha da política de segurança ou das salvaguardas, ou mesmo uma situação até então desconhecida que pode se tornar relevante em termos de segurança. 

 

7. Incidente de segurança da informação 

(ISO/IEC 27000:2018, item 3.31) 

Evento ou série de eventos indesejados ou inesperados que provavelmente compromete as operações da empresa ou ameaça a segurança da informação. 

 

8. Risco 

(ISO/IEC 27000:2018, item 3.61) 

Combinação das consequências de um evento (incluindo mudanças nas circunstâncias) e de sua probabilidade associada de ocorrência. 

 

9. Impacto 

Mudança não desejável nos objetivos de negócios. 

 

10. Escopo de ativos 

Define o conjunto de ativos coberto pelo processo. 

 

11. Parte envolvida 

Indivíduos, grupos ou organizações afetados diretamente por um risco. 

 

12. Parte interessada 

Indivíduo ou grupo com interesse no desempenho ou sucesso de uma organização. 

### Risco a segurança da informação 

 

Antes de conhecê-los, precisamos entender como são realizados os <b>processos da gestão de riscos</b> (GR) dentro da <b>Gestão de Segurança da Informação</b> (GSI). Para isso, analisaremos um exemplo. 

  
 
<center>A organização XPTO possui um servidor que executa um banco de dados com os seguintes elementos:</center> 

 
 
<b>Escopo de ativos: </b>Servidor e banco de dados; 

 
 
<b>Vulnerabilidades identificadas:</b> Falha no software que pode ser explorada devido a outra no sistema operacional; 

 
 
<b>Ameaça:</b> Malware codificado para explorar as vulnerabilidades citadas e roubar dados do banco de dados; 

 
 
<b>Medida de controle adotada:</b> Instalação de suíte de antivírus; 

 
 
<b>Medidas de controle não adotadas:</b> Atualização de sistema operacional e software; 

 
 
<b>Possível incidente de segurança da informação:</b> Malware chega por e-mail para um usuário, que executa o arquivo anexado; 

 
 
<b>Impactos:</b> Roubo de dados sensíveis e prejuízo financeiro; 

 
 
<b>Risco:</b> Risco extremo. 

 

Um malware chamado No pain, no gain está causando pânico nas empresas ao redor do mundo justamente por explorar as vulnerabilidades identificadas nelas e roubar seus dados sensíveis. Existe, portanto, uma alta probabilidade de esse malware explorar tais vulnerabilidades, caso as medidas de controle restantes não sejam adotadas, causando, com isso, um impacto grave nos negócios dessas organizações. Para a XPTO, esse risco é relevante e foi classificado como risco extremo. 

<center>Neste caso, que medidas devem ser tomadas?</center>

O plano de tratamento definido, nesse caso, foi o seguinte: evitar a ocorrência do incidente de forma preventiva, instalando as atualizações de software necessárias. Para isso, deve ser realizada uma comunicação às partes envolvidas antes e depois das atualizações. Após a aplicação delas, o risco será monitorado para prever a ocorrência de outras possíveis vulnerabilidades. 

 

Cada organização percebe os riscos de forma diferente. Neste exemplo, a organização Ajax (concorrente da XPTO) realizou uma percepção de risco diferente da empresa XPTO. Ela utiliza outro tipo de sistema operacional e outro tipo de software de banco de dados, que não são afetados pelo malware No pain no gain. Logo, dentro de seu atual contexto, esse malware pode não fazer parte da percepção de risco. 

 

Uma vez percebido, um risco passa pelo crivo de tolerância, determinando se ele será tratado ou não. 

O nome desse processo é critério de risco (o que a organização define como tolerável). Os que sobram após o tratamento são chamados de riscos residuais: trata-se daqueles considerados pequenos ou que, apesar das respostas não implementáveis, devem ser monitorados. 

### gestão de riscos 

 

As seguintes normas relacionadas à Gestão de Riscos (GR) podem ser levadas em consideração pelos profissionais da segurança da informação: 

ABNT NBR ISO/IEC 27005 

Gestão de riscos de segurança da informação 

ABNT NBR ISO/IEC 31000 

Gestão de riscos – princípio de diretrizes 

 

Com elas, é possível entender o conceito, o funcionamento e as etapas de uma GR. 

 

Conceito 

<center>Mas, afinal, qual é o papel da GR? </center>

A Gestão de Riscos é o processo que identifica e trata os riscos de forma sistemática e contínua. Trata-se de um dos componentes mais importantes da GSI. 

Funcionamento 

Para ter sucesso, a GR deve ser permanente, mostrando-se capaz de identificar novas vulnerabilidades e ameaças que podem afetar os três pilares de segurança da informação: confidencialidade, integridade e disponibilidade (CID). 

 

É necessário criar uma estrutura adequada para essa gestão. Dessa forma, tão importante quanto a definição de funções e responsabilidades é o desenvolvimento de uma cultura de GR. Com isso, uma organização mantém seu nível de risco em patamares aceitáveis. 

 

#### Etapas da gestão de riscos 

A GR compreende as seguintes etapas: 

 
 

1. Definição do contexto 

Inicialmente, deve-se fazer a listagem e um breve resumo dos objetivos organizacionais, pois, se seus riscos não forem atingidos, eles terão de ser gerenciados. Dessa forma, é feito um levantamento de informações relevantes sobre o ambiente no qual será executada a análise de riscos. 

Deve estar claro nesse levantamento o entendimento sobre as atividades da organização e os propósitos que a levaram à GSI, como, por exemplo, suporte ao SGSI, conformidade legal, plano de continuidade de negócios e de resposta a incidentes. (BEZERRA, 2013) 

 

Bezerra (2013) ainda elenca os itens que devem constar nessa análise da organização 

- Propósito principal da organização; 
- Negócio; 
- Missão; 
- Visão de futuro; 
- Valores; 
- Estrutura organizacional; 
- Organograma; 
- Estratégias; 
- Produtos; 
- Parceiros; 
- Terceiros; 
- Instalações; 
- Funcionários. 

 

Por fim, são estabelecidos parâmetros para o gerenciamento dos riscos. 

 

Parâmetros: Escalas de probabilidade e impacto, definição do apetite a risco e nível de risco considerado aceitável. 

 

2. Processo de análise/avaliação de riscos de segurança da informação 

Esta etapa se divide em: 

![Análise de risco](media/introducao-a-seguranca-da-informacao/analise-risco.png)

A análise/avaliação de riscos consiste nas seguintes atividades: Análise de riscos (Seção 8.2) compreende: - Identificação dos riscos (Seção 8.2.1); - Estimativa dos riscos (Seção 8.2.2); - Avaliação de riscos (Seção 8.3). 

A identificação de riscos mapeia os eventos de risco que podem impedir uma empresa de atingir os objetivos desejados. A análise de riscos, por sua vez, compreende a identificação e a estimativa deles. 

Pode-se começar com uma lista dos eventos de risco associados aos objetivos institucionais, evoluindo, em seguida, para um nível maior de detalhamento. Após realizar o mapeamento e a relação desses eventos, listam-se as suas possíveis causas e consequências de cada um deles. 

Já a estimativa de riscos mede os eventos de risco por meio do cálculo do nível de risco. Deve-se iniciar tal processo realizando o cálculo do nível de risco bruto. 

Para isso, são avaliados a probabilidade e o impacto de um evento de risco antes que uma medida de controle qualquer seja implementada, conforme os exemplos das duas tabelas a seguir: 

![Estimativa de risco](media/introducao-a-seguranca-da-informacao/estimativa-risco.png)

Em seguida, é avaliada a qualidade das medidas de controle que existem para impedir o risco bruto. Obtém-se, com isso, o risco residual, ou seja, o que sobra do bruto depois de ele ser mitigado pela atividade de controle. 

Monta-se uma tabela em ordem decrescente em relação ao nível de risco residual para verificar os eventos de risco que devem ser tratados com prioridade. Para cada risco considerado prioritário, elabora-se uma matriz de impacto versus probabilidade. Observemos esta tabela: 

![Nivel de risco](media/introducao-a-seguranca-da-informacao/nivel-risco.png)

A avaliação de riscos, por sua vez, define as medidas de tratamento a serem implementadas para cada um dos eventos de risco, entre as quais destacamos:

![Eventos de risco](media/introducao-a-seguranca-da-informacao/eventos-risco.png)

Ao lado de cada evento de risco, deve ser informada a forma de tratamento a ser adotada. Isso é feito tendo como base o nível de risco residual e o apetite a risco identificado na definição do contexto. 

 
 

3. Tratamento do risco de segurança da informação 

Essa etapa estabelece como cada opção de tratamento é implementada. 

 

Toda medida de tratamento deve conter a indicação dos responsáveis por sua implementação – no caso, os gestores do risco. No tratamento do risco, são selecionadas e implementadas medidas de forma a reduzir os riscos identificados. 

Desse modo, o plano de tratamento do risco (PTR) é definido. A seguir, são feitas recomendações para que a empresa crie ou modifique os mecanismos de segurança existentes. 

Para cada forma de ameaça, deve ser definida uma ou mais medidas de proteção (controles). Tais medidas precisam ser aplicadas nos ativos, além de seus custos. 

 

<center>Os resultados serão as respostas às seguintes questões: </center>


O que deve ser protegido? 
A que custo? 
De quem proteger? 
Com que riscos? 

No custo desejado, a proteção provavelmente não dará uma segurança total. 


<center>As medidas de controle ou proteção podem ser classificadas como:</center> 

  
 
<center>Medidas de Controle ou Proteção</center> 

 
 
<b>Preventiva:</b> Evita que incidentes ocorram; 

 
<b>Desencorajadora:</b> Desencoraja a prática de ações; 

 
<b>Monitoradora:</b> Monitora o estado e o funcionamento; 

 
<b>Corretiva:</b> Corrige falhas existentes; 

 
<b>Recuperadora:</b> Repara danos causados por incidentes; 

 
<b>Reativa:</b> Reage a determinados incidentes; 

 
<b>Detectora:</b> Detecta a ocorrência de incidentes; 

 
<b>Limitadora:</b> Diminui os danos causados; 

 

4. Aceitação do risco de segurança da informação 

A decisão de aceitar os riscos residuais não basta: é necessário se responsabilizar por ela. Afinal, é responsabilidade da política de gestão de riscos oferecer suporte a essa tomada de decisão. 

 
 

5. Comunicação do risco de segurança da informação 

Recomenda-se que as informações sobre riscos sejam trocadas ou compartilhadas entre o tomador de decisão e as outras partes interessadas para haver um consenso sobre como eles devem ser administrados. 

 
 

6. Monitoramento e análise crítica de riscos de segurança da informação 

Nesta etapa, é avaliado se tudo o que foi feito saiu de acordo com o planejado. Além disso, são averiguados, dentre outros, os seguintes casos: 

 

Necessidade de atualizações; 

 
Listagem correta dos objetivos; 

 
Impossibilidade de um risco ser visto como esperado pelas atividades de controle; 

 
Cálculo correto dos níveis de risco. 


A figura a seguir ilustra uma visão do processo de gestão de risco (GR) segundo a norma ABNT NBR ISO/IEC 27005: 


![Processo de risco](media/introducao-a-seguranca-da-informacao/processo-risco.png)