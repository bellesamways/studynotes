# Aula 2 - Modelos de Ciclo de Vida de Software 

É necessário conhecer as características do projeto a ser desenvolvido para escolhermos o melhor ciclo de vida e os recursos humanos empregados no projeto. 

 

Esses devem ser reconhecidamente capazes de enfrentar os desafios que se apresentam diante das dificuldades inerentes de todo e qualquer projeto de software. 

 

Principais modelos de ciclo de vida de software: 

- Cascata; 

- Modelo em V; 

- Modelo incremental; 

- Evolutivo; 

- Iterativo e incremental; 

- RAD; 

- Prototipagem; 

- Espiral; 

- Modelo de ciclo de vida associado ao RUP. 

 

## Cascata 

 

O modelo cascata, ou sequencial linear, é considerado o mais antigo e o mais usado na engenharia de software em todo o mundo. Este é o grande mérito deste modelo. 

 

Seu nome foi atribuído devido à sequência com que cada fase do desenvolvimento dependia do término da fase anterior, ou seja, o resultado de uma fase era utilizado com a entrada para a fase seguinte. 

 

Nesse modelo, a ênfase maior ficava por conta das fases de análise e projeto antes de iniciar a implementação (codificação). 


![imagem](../../media/qualidade-e-teste-de-software/image-004.png)


É possível retornar a uma etapa anterior; entretanto deve-se analisar muito bem em relação às áreas técnica e financeira, sem prejuízo das partes envolvidas. 

 

**Vantagens do modelo cascata**: 

- A fase de análise de requisitos (única) leva ao projeto do sistema e, por sua vez, antes da fase de codificação; 

- Ao final de cada fase e antes de iniciar a seguinte, devem ser feitas revisões com a participação do usuário; 

- Cada etapa (fase) deve passar por aprovação e documentação, visando o passo seguinte. 

 

**Desvantagens do modelo cascata**: 

- O fluxo sequencial proposto pelo modelo geralmente não é seguido; 

- O modelo cascata exige que os requisitos sejam claramente definidos e completos, pois são estabelecidos na fase inicial do projeto; 

- O módulo executável para testes somente fica disponível ao final do projeto, isto é, na etapa avançada do desenvolvimento, exigindo um grande esforço. 

 

## Modelo em V 

 

Este modelo é uma variação do cascata, ajustando as atividades de testes com as fases de análise e projeto. 

 

Da mesma forma que no cascata, o modelo em V é sequencial, o que significa que cada fase necessita ser concluída antes do início da fase seguinte. 


![imagem](../../media/qualidade-e-teste-de-software/image-005.png)


Como podemos observar, no modelo em V os procedimentos de testes são planejados em praticamente todas as fases do desenvolvimento, diferentemente do que ocorre no modelo em cascata. 

 

**Vantagens do modelo em V**: 

- Maior chance de sucesso quando comparado com o modelo cascata, devido ao desenvolvimento de planos de teste desde as fases iniciais; 

- Funciona bem para projetos pequenos, nos quais os requisitos são facilmente entendidos. 

 

**Desvantagens do modelo em V**: 

- Tão rígido quanto o modelo cascata; 

- Requisitos devem ser estabelecidos corretamente e de forma clara no início do projeto. 

 

## Incremental 

 

No modelo incremental, as novas funcionalidades ou necessidades do usuário são integradas de forma segmentada e em série até a conclusão do produto final. 

 

Este modelo se propõe a aumentar pouco a pouco o software, conforme as necessidades surgem. 


![imagem](../../media/qualidade-e-teste-de-software/image-006.png)


O modelo incremental deve ser adotado quando os requisitos são claramente conhecidos na fase inicial do desenvolvimento e há a necessidade de entrega de um módulo ou funcionalidade do software em curto espaço de tempo. 

 

**É importante notar que, a cada incremento, uma nova versão do software é produzida.** 


![imagem](../../media/qualidade-e-teste-de-software/image-007.png)


 

**Vantagens do modelo incremental**: 

- A entrega da primeira versão apresenta um menor custo e menos tempo se comparado com os modelos em cascata e em V; 

- Poucos riscos associados ao desenvolvimento dos incrementos devido ao seu tamanho reduzido. 

 

**Desvantagens do modelo incremental**: 

No caso de requisitos mal definidos ou incompletos, alguns incrementos podem ser retrabalhados, o que gera custos e atrasos. 

 

## Modelo evolutivo 

 

O modelo evolutivo obedece a um processo que visa o desenvolvimento do software a partir de requisitos de protótipos iniciais. 

 

Neste modelo, as versões parciais são desenvolvidas para atender aos requisitos levantados inicialmente. Assim, a primeira versão é usada para refinar os requisitos visando uma segunda versão e, a partir do conhecimento obtido com o uso, o desenvolvimento prossegue, evoluindo, então, o produto. 

**Vantagens do modelo evolutivo**: 

- É usado quando os requisitos se apresentam incompletos no início do desenvolvimento; 

- Com o uso do sistema, o conhecimento sobre o produto vai aumentando e, consequentemente, melhorando os requisitos. 

 

**Desvantagens do modelo evolutivo:** 

- É necessário um rígido controle sobre os custos, grande preocupação com o cronograma e com a configuração do software; 

- Usuários precisam estar preparados quanto aos resultados iniciais, que podem parecer insatisfatórios. 

 

## Iterativo e incremental 

 

**O processo de desenvolvimento em cascata apresenta uma série de vantagens, porém tem também alguns pontos fracos. Para solucionar este impasse, estudiosos de TI criaram o modelo de desenvolvimento iterativo e incremental.** 

 

Esse modelo trouxe bastante agilidade e flexibilidade nos processos de desenvolvimento de software, o que permitiu uma maior capacidade de lidar com as demandas do mercado e, assim, atingir melhores resultados em médio e longo prazo. 

 

Basicamente, este modelo divide o desenvolvimento do software em pequenos ciclos ou módulos ou novas funcionalidades. Cada funcionalidade deve corresponder a uma necessidade do usuário à medida que for necessária à sua construção. 

 

Para o desenvolvimento de cada funcionalidade, é utilizado um pequeno modelo em cascata, objetivando, assim, atender às necessidades sempre que se fizer necessário. 

 

Precisamos, então, identificar as necessidades dos usuários e definir uma escala de prioridades para cada uma dessas funcionalidades. 



![imagem](../../media/qualidade-e-teste-de-software/image-008.png)


## RAD (Rapid Application Development) 

 

**O modelo RAD é um modelo de desenvolvimento de software incremental que enfatiza um ciclo de desenvolvimento curto e se apresenta de forma sequencial linear.** 

 

A rapidez ou velocidade com que o software é desenvolvido se deve pelo fato de várias equipes trabalharem em paralelo, quando o produto pode ser dividido em módulos. Um projeto de software que utiliza o RAD consome em média de 60 a 90 dias. 

 

O uso deste modelo exige requisitos bem definidos e estabilizados, além de escopo restrito e com possibilidade de ser dividido em módulos. 


![imagem](../../media/qualidade-e-teste-de-software/image-009.png)


**Vantagens do modelo RAD**: 

- O ciclo de desenvolvimento é extremamente curto se comparado com os demais modelos; 

- Distribuição de tarefas é facilitada entre as equipes de desenvolvimento. 

 

**Desvantagens do modelo RAD**: 

- Requer equipes de desenvolvimento adequadas para atender à demanda de projetos grandes e escaláveis; 

- Não é apropriado quando os riscos são grandes; 

- Não é apropriado quando o sistema precisa interagir com outros sistemas. 

 

## Prototipagem 

 

O modelo prototipagem é utilizado quando é definido um conjunto de objetivos gerais para o software, mas os detalhes não estão claramente definidos como requisitos de entrada, processamento ou saída. 

 

O ciclo do modelo prototipagem começa com a comunicação entre o engenheiro de software e o cliente, quando são definidos os objetivos gerais do software, identificando as necessidades conhecidas e são verificadas as áreas que necessitam de mais definição. 

 

Os usuários podem fazer simulações com o protótipo, identificando mais detalhadamente funcionalidades que deverão ser disponibilizadas futuramente. 

 

A versão inicial do software ajuda a determinar a viabilidade técnica, custos e prazo do projeto. 

 

É importante haver uma forte interação com o usuário para que rapidamente o protótipo seja implementado de acordo com as etapas: 


![imagem](../../media/qualidade-e-teste-de-software/image-010.png)


**Vantagens do modelo prototipagem**: 

- O protótipo deve ser avaliado pelo usuário; 

- A interação do usuário com o protótipo é fundamental para ajustar as necessidades funcionais. 

 

**Desvantagens do modelo prototipagem**: 

- O usuário pode pensar que a maior parte do software está pronta; 

- O protótipo pode crescer de maneira não planejada, com risco de se tornar um incremento funcional; 

- O protótipo pode confundir o usuário iludido por um desempenho melhor do que um incremento funcional; 

- O fato de o protótipo não implementar toda a funcionalidade pode causar frustação para o usuário quando o sistema completo é entregue. 

 

## Modelo espiral 

 

O modelo espiral se divide em duas etapas principais: análise de riscos e prototipagem. A cada novo ciclo, esse modelo testa constantemente erros que podem vir a acontecer. 

 

A cada iteração, a volta da espiral pode ser baseada em um modelo diferente e pode ter diferentes atividades. Ou seja, a cada repetição é refeita a análise de a prototipação até que não existam grandes riscos no desenvolvimento. 

 

No modelo espiral, em cada repetição do ciclo devem ocorrer no projeto: 

1. Determinação de objetivos. 

2. Avaliação e redução de riscos. 

3. Desenvolvimento e validação. 

4. Planejamento da próxima iteração. 

 

Os riscos são considerados à medida que cada evolução é realizada. 

 

A primeira atividade se dá com o desenvolvimento de uma especificação de produto, as próximas passagens podem ser usadas para desenvolver um protótipo e assim sucessivamente. 


![imagem](../../media/qualidade-e-teste-de-software/image-011.png)


Cada passagem pela fase do planejamento, por exemplo, resulta em ajustes no planejamento do projeto. O custo e o cronograma são sempre ajustados de acordo com o feedback obtido do usuário após uma entrega. 

 

Na imagem, cada loop representa uma fase de desenvolvimento do software. 

 

**Vantagens do modelo espiral**: 

- Muita análise de riscos; 

- Bom para projetos grandes e críticos; 

- Software é produzido cedo no ciclo de vida. 

 

 

**Desvantagens do modelo prototipagem**: 

- Pode ser custoso; 

- Análise de riscos requer experiência; 

- Não se aplica bem a projetos menores. 

 

## RUP (Rational Unified Process) 

 

O RUP foi desenvolvido em 1999 por Jacobson, Booch e Rumbaugh depois de terem definido a UML. É um processo que integra ciclos, fases e disciplinas, visando a qualidade no gerenciamento de projetos. 

 

O ciclo de vida do desenvolvimento do software é dividido nas seguintes fases: 

1. **Concepção**: Define o escopo do projeto. 

2. **Elaboração**: Planeja o projeto, define e valida a arquitetura. 

3. **Construção**: Construção do software. 

4. **Transição**: Implantação do software. 

 

As disciplinas requisitos, análise, projeto, implementação, testes e implantação vão estar presentes em cada uma dessas fases, com maior ou menor ênfase, conforma mostra a figura: 

![imagem](../../media/qualidade-e-teste-de-software/image-012.png)