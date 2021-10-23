# Fundamentos de sistemas operacionais

O sistema operacional pode ser definido como o conjunto de programas que servem de interface entre o hardware e o usuário. Ele é composto por rotinas que realizam o gerenciamento dos diversos componentes do sistema (processador, memória, dispositivos de entrada e saída etc.).

**Sistema operacional**: uma camada de software que abstrai do usuário a administração do hardware.

![Sistema operacional como uma camada de abstração](/media/sistemas_operacionais/sistemaoperacional-camada-de-abstracao.png)

## Objetivos de um Sistema Operacional

Facilitar o acesso aos recursos do computador, tornando eficiente o uso do hardware, aumentando a produtividade e agilizando atividades diárias;

Garantir a segurança dos dados e sua integridade tanto no armazenamento quanto durante as atividades de processamento, bem como no acesso aos recursos físicos disponíveis.

 </br>
 
## Histórico dos sistemas operacionais

### 1ª geração 1945 - 1955

Os usuários tinham completo acesso ao hardware, e as instruções eram introduzidas manualmente, uma a uma, em linguagem de máquina (nas primeiras máquinas, a introdução das instruções era por meio de chaveamento de circuitos através de cabos, como nas mesas telefônicas mais antigas), não existindo, portanto, o conceito de Sistema Operacional.

### 2ª geração 1955 - 1965

O desenvolvimento do transistor, que tinha mais confiabilidade e um custo menor que as válvulas, mudou totalmente o quadro existente. A programação dos computadores passou a ser realizada via linguagens de alto nível como Fortran, e foi desenvolvido o sistema de processamento em batch (lote)

### 3ª geração 1965 - 1980

Surgimento dos circuitos integrados e da multiprogramação. Os sistemas operacionais desta geração passaram a utilizar várias técnicas que ainda estão presentes nos SOs atuais como:

**Alocação de Memória**: a memória do sistema era dividida em várias partições nas quais diferentes programas eram carregados de forma que vários deles pudessem utilizá-la de forma concorrente;

**Spooling**: enquanto um job (tarefa) era executado, os cartões de outros jobs eram lidos e transferidos para o disco. Isso permitia que a troca entre os diversos jobs ocorresse de forma mais rápida, já que o acesso ao disco era muito mais rápido que a leitura dos cartões;

**Time sharing (compartilhamento de tempo)**: cada programa, na memória, utilizava o processador em pequenos intervalos de tempo, isso permitia que, enquanto uma tarefa esperava alguma operação de Entrada ou Saída, outra utilizasse o processador (CPU).

Foi desenvolvido nesta época, também, o Sistema Operacional UNIX.

### 4ª geração 1980 - hoje

Esta geração marca o surgimento da integração em larga escala e dos computadores pessoais. O surgimento dos microcomputadores levou à criação de toda uma nova geração de sistemas operacionais.

Como então qualquer pessoa poderia ter um computador, o SO teve que se adaptar, fornecendo mais interatividade, evoluindo das interfaces em texto, como o DOS, para as interfaces gráficas como o Windows.

 </br>

## Tipos de Sistemas Operacionais

 </br>

### Sistema Monoprogramado ou Monotarefa

O sistema computacional fica totalmente dedicado a um único programa, ou seja, todos os recursos de memória, processamento e entrada e saída ficam todo o tempo disponíveis ao programa que está sendo executado, mesmo que o dispositivo não esteja sendo utilizado.

Esta era a configuração típica dos primeiros SO;

Este tipo de SO pode atender a apenas um único usuário de cada vez;

Este tipo de SO é relativamente simples de ser implementado.

</br>

### Sistemas Multiprogramáveis ou Multitarefas

Os diversos recursos computacionais são compartilhados pelas várias tarefas ou programas.  
O SO deve gerenciar a alocação dinâmica dos recursos do computador às diversas demandas geradas pelas tarefas.  
O sistema operacional terá que gerenciar o acesso concorrente aos componentes do sistema, protegendo os dados de cada programa e evitando que as ações de uma tarefa prejudiquem as outras.
Este tipo de SO aumenta a produtividade e reduz os custos de utilização, pois enquanto um programa realiza uma operação de entrada e saída outro pode utilizar o processador.

**Sistemas Batch**: não necessita de interação do usuário, já que o programa é executado sequencialmente após a sua carga que era realizada a partir de fitas ou discos.

**Sistemas de tempo compartilhado (time sharing)**: tempo de uso do processador é dividido em pequenas fatias atribuídas a cada programa, permitindo que várias tarefas sejam executadas.

**Sistemas de tempo real**: suas aplicações possuem um tempo máximo aceitável para produzir a resposta.

Define-se um sistema operacional multitarefa como sendo aquele que possui a capacidade de manter vários programas na memória simultaneamente.

Em um sistema multiprogramável, um processo ativo pode estar nos estados espera, pronto ou execução.

</br>

### Sistemas multiprocessados

Caracterizam-se por possuírem vários processadores que trabalham em conjunto e compartilham dados. Desta forma permitem que vários programas sejam, verdadeiramente, executados simultaneamente, sendo assim multiusuários.

Vantagens:

Escalabilidade: ampliar a capacidade computacional adicionando mais processadores.

Disponibilidade: se um processador falhar, os outros podem manter o sistema ativo.

Balanceamento de carga: distribuir as tarefas entre os vários processadores a partir da carga de trabalho de cada um, ocupando a capacidade ociosa e melhorando o desempenho total do sistema.

**Fortemente acoplados**: Os múltiplos processadores compartilham uma única memória e são controlados pelo mesmo SO. Como exemplo, podemos citar os modernos computadores com vários chips de processadores ou os chips com vários núcleos como os I3, I5 e I7 da Intel.

**Fracamente acoplados**: Os processadores não estão em um único computador, mas espelhados em máquinas diferentes, cada uma com o seu SO. Estes computadores são ligados por uma linha de comunicação. Como exemplo, temos os servidores e os clientes de uma rede de computadores.

</br>

## Estrutura do Sistema Operacional

O Sistema Operacional proporciona o ambiente no qual os programas são executados e é composto por um conjunto de rotinas, conhecido como o núcleo.

A interface entre o Sistema Operacional e os programas dos usuários é definida por um conjunto de instruções denominado chamadas de sistema (system calls).

O Sistema Operacional não funciona de forma linear, com início, meio e fim. Ele reage às chamadas de sistemas e executa os seus procedimentos de forma concorrente, sem seguir uma ordem estabelecida, com base em eventos assíncronos.

Principais funções de um SO:

Gerenciamento de processos e processador

Gerenciamento de memória

Gerenciamento dos dispositivos de entrada e saída

Gerenciamento de arquivos

Proteção e segurança

Em sistemas operacionais, o conceito de compilador é um programa de computador que transforma o código fonte escrito em uma linguagem compilada em um programa semanticamente equivalente em código objeto.

_Um compilador é um programa de sistema que traduz um programa descrito em uma linguagem de alto nível para um programa equivalente em código de máquina para um processador. Em geral, um compilador não produz diretamente o código de máquina mas sim um programa em linguagem simbólica (assembly) semanticamente equivalente ao programa em linguagem de alto nível. Para cada arquivo de código fonte é gerado um arquivo com código objeto, que posteriormente é "ligado" aos outros, através de um linker, resultando num arquivo executável ou biblioteca._

## Conceito de processo

De forma simplificada, podemos definir processo como um programa em execução.

Com a introdução desse conceito foi possível **isolar e especificar** muitas das funções primitivas dos SOs. Cada atividade de um SO consiste na execução de um ou mais programas que são chamados toda vez que a respectiva função é requerida.

Assim, um processo pode ser considerado como sendo a **sequência de ações realizadas pela execução de instruções (um programa) cujo resultado final fornece uma das funções do sistema**.

A execução de um programa de um usuário é também um processo.

Um processo pode envolver a execução de mais de um programa;

Um mesmo programa pode ser requerido por mais de um processo.

Processo -> dinâmico

Programa -> estático

Na realização das funções de um SO, algumas vezes é conveniente forçar o **paralelismo** de algumas atividades. As razões para o paralelismo são: **disponibilidade de agentes (para levar a cabo a atividade) e reduzir o tempo de execução da tarefa**.

</br>

## Estados do processo

Quando um processo **muda de estado** dizemos que ele sofreu uma **transição**.

### Sistema Monotarefas

Cada programa é carregado do disco para a memória e executado até sua conclusão.

Os dados são carregados na memória juntamente com o código executável e os resultados obtidos no processamento salvos no disco após a conclusão da tarefa.

![Processamento de disco](/media/sistemas_operacionais/processamento-de-disco.jpeg)

**Novo**: o processo está sendo criado, o código e os dados necessários para sua execução estão sendo carregados na memória.

**Executando**: as instruções do programa estão sendo executadas no processador.

**Terminado**: o programa foi totalmente processado, produziu os resultados e pode ser removido da memória do sistema.

</br>

### Sistema Multitarefas

Vários programas podem ser executados ao mesmo tempo.

**Pseudoparalelismo** quando os programas apenas **parecem** ser executados ao mesmo tempo, como ocorre em sistemas monoprocessados;

**Paralelismo real** quando eles efetivamente **são processados** ao mesmo tempo, cada um em processador ou core diferente.

![Sistema multitarefas](/media/sistemas_operacionais/sistema-multitarefas.jpeg)

**Novo**: O processo está sendo criado, o código e os dados necessários para sua execução estão sendo carregados na memória, e as estruturas de dados do núcleo estão sendo atualizadas para permitir o controle de sua execução. Após o término de sua criação, ele passa ao estado de **pronto**.

**Pronto**: O processo é colocado em uma **fila de prontos**, ou seja, ele está preparado para executar (ou para continuar sua execução), apenas aguardando a disponibilidade do processador. O Algoritmo de Escalonamento escolhe um processo para “ganhar” a CPU, passando este, então, ao estado de **executando**.

**Executando**: As instruções do programa estão sendo executadas no processador.

O processo solicita uma operação de entrada/saída — o processo passa a **bloqueado**;

O processo chegou ao seu final ou ocorreu um erro que o impede de prosseguir – passa ao estado de **terminado**;

Ocorre uma interrupção – processo passa ao estado de **pronto**.

**Bloqueado**: O processo não pode ser executado porque depende de dados externos ainda não disponíveis (do disco ou da rede, por exemplo) necessitando de uma operação de entrada/saída ou aguarda algum tipo evento ocorrer. Ao terminar a operação de E/S ou ocorrendo o evento aguardado, o processo passa ao estado de **pronto**.

**Terminado**: O programa foi totalmente processado, produziu os resultados e pode ser removido da memória do sistema e as estruturas de controle podem ser apagadas.

![Sistema multitarefas](/media/sistemas_operacionais/multitarefas-processo.gif)

</br>

## Bloco de controle de processo

Cada processo é representado por um descritor (bloco de controle ou BCP), que é uma área de memória contendo todas as informações relevantes do processo.

![Bloco de controle de processo](/media/sistemas_operacionais/bloco-de-controle.jpeg)

No BCP, controlamos uma série de dados incluindo:

**Informações de escalonamento de UCP**: incluem prioridade de processo, ponteiros para filas de escalonamento e quaisquer outros parâmetros de escalonamento.

**Estado do processo**: pronto, executando ou bloqueado.

**Número do processo**: constitui o seu identificador dentro do Sistema Operacional.

**Contador do programa**: indica o endereço da próxima instrução a ser executada para esse processo.

**Registradores de UCP**: correspondem ao conteúdo dos registradores da CPU no momento em que o programa saiu do estado de **executando** para **bloqueado** ou **pronto**. Juntamente com o contador do programa, essas informações de estado devem ser salvas para permitir que o processo continue corretamente depois.

**Informações de gerência de memória**: podem incluir dados como o valor dos registradores de base e limite, as tabelas de páginas ou tabelas de segmentos, dependendo do sistema de memória usado pelo sistema operacional.

**Informações de contabilização**: incluem a quantidade de UCP e o tempo real usados, limites de tempo, números de contas, números de jobs ou processos, etc.

**Informações de status de E/S**: incluem a lista de dispositivos de E/S alocados para este processo, uma lista de arquivos abertos e outras informações.

As informações do BCP podem ser agrupadas em **contexto de hardware** e em **contexto de software** do processo. Informações que precisam ser salvas quando o processo perde o controle de um processador, de maneira a possibilitar o reinicio da execução quando o processo passar novamente a executar.

**Contexto de hardware**: constituído basicamente dos **valores dos registradores/flags** da máquina antes do bloqueio.

**Contexto de software**: constituído da **identificação do processo**, seus **limites em termos de recursos** (número máximo de arquivos, tamanho de memória permitido, número de subprocessos permitidos etc.) e **nível hierárquico do processo** (que determina o que o processo pode ou não fazer em termos de operações protegidas do sistema).

Os estados dos processos incluem ainda _novo_ e _terminado_. Porém, estes estados não são representados no BCP, pois **não correspondem a processos ativos**. No caso de _novo_ o BCP está sendo **criado**, e no de _terminado_, sendo **destruído**.

</br>

## Troca de contexto

Quando ocorre a preempção ou um processo solicita E/S um novo processo é escalonado. Para que o processo interrompido possa voltar a ser executado corretamente no futuro, o seu contexto deve ser salvo no BCP, e o novo processo e o que irá iniciar a execução, ter o seu contexto lido no BCP.

![Troca de contexto](/media/sistemas_operacionais/troca-de-contexto.jpeg)

</br>

## Criação de processos

Um processo, durante sua execução, pode ativar outros processos através de uma chamada de sistema para criar o que se chamam processos filhos, formando uma árvore de processos.

![Criação de Processos](/media/sistemas_operacionais/criacao-de-processos.png)

Esses processos têm as mesmas prerrogativas do processo pai, possuindo espaço no endereçamento e contextos de hardware e software. Para gerenciar esses processos, o SO filho adota os mesmos critérios que os processos pais.

</br>

## Tipos de processo

### CPU-bound (ligado à CPU)

Passa a maior parte do tempo no estado de _execução_, ou seja, utilizando o processador. Esse tipo de processo realiza poucas operações de E/S.

### I/O-bound (ligado à E/S)

Passa a maior parte do tempo no estado de _bloqueado_, pois realiza um elevado número de operações E/S.

</br>

## Threads

Não possui todas as prerrogativas de um processo, mas também permite algum tipo de paralelismo das funções.

Threads são fluxos de execução (linha de controle) que rodam dentro de um processo. Em processos tradicionais, há uma única linha de controle e um único contador de programa. Porém, alguns Sistemas Operacionais fornecem suporte para múltiplas linhas de controle dentro de um processo (sistemas multi thread).

Multithread num sistema operacional é uma forma de um único processo pode estar associado a vários fluxos de execução (threads).

![Multithread](/media/sistemas_operacionais/multithread.png)

Benefícios do uso de _thread_:

**Capacidade de resposta**: Ao se utilizar várias threads, em uma aplicação interativa, podemos permitir que parte de um programa continue executando, como, por exemplo, a interface do usuário, enquanto outra parte esteja bloqueada, realizando, por exemplo, uma operação de entrada/saída.

**Compartilhamento de recursos**: As threads compartilham o código, os dados e os arquivos do processo ao qual pertencem, o que permite que uma aplicação possua várias threads de atividades dentro do mesmo espaço de endereçamento.

**Economia**: A alocação de memória e recursos para a criação de processos é dispendiosa. Como as threads compartilham estes recursos do processo, é muito mais rápido criá-las e permutar seus contextos.

**Escalabilidade**: Em sistemas multiprocessados, a utilização de threads permite que várias atividades, do mesmo processo, sejam realizadas em paralelo nos diversos núcleos.

Exemplo de uso de thread:

![Multithread](/media/sistemas_operacionais/beneficios-thread.jpeg)

## Gerência de processador

É a parte de um SO em que são definidos a ordem e os critérios para executar os processos em uma máquina.

O procedimento de determinar qual processo será executado, por quanto tempo, em que ordem, dentre os diversos processos que estejam na fila de prontos é chamado escalonamento.

</br>

### Escalonamento preemptivo e não preemptivo

**Preemptivo**: uma tarefa pode perder o processador caso termine seu quantum de tempo, execute uma chamada de sistema ou caso ocorra uma interrupção que acorde uma tarefa prioritária. A cada interrupção, exceção ou chamada de sistema, o escalonador pode reavaliar todas as tarefas da fila de prontas e decidir se mantém ou substitui a tarefa atualmente em execução.

**Não preemptivo**: também chamado de cooperativo, a tarefa em execução permanece no processador tanto quanto possível, só abandonando-o caso termine de executar, solicite uma operação de e/s ou libere explicitamente o processador, voltando à fila de tarefas prontas. Esses sistemas são chamados de cooperativos por exigir a cooperação das tarefas entre si na gestão do processador, para que todas possam executar.

**\*Quantum**: é o tempo máximo que um processo pode executar a cada vez que passa ao estado de executando. Após esse tempo ele é interrompido e colocado no fim da fila de prontos.

A maioria dos sistemas operacionais, de uso geral atuais, é preemptiva. Sistemas mais antigos, como o Windows 3.\*, PalmOS 3 e MacOS 8 e 9 operavam de forma cooperativa.

</br>

### Tipos de ciclo

A execução de um processo é uma sucessão de ciclos de execução de instruções (CPU burst) e espera pelo término da operação de entrada e saída (E/S burst).

A execução começa com um CPU burst, seguido de um E/S burst e novamente um CPU burst:

![Sistema operacional como uma camada de abstração](/media/sistemas_operacionais/tipos-de-ciclo.jpeg)

</br>

### Critérios de escalonamento

**Justiça**: o algoritmo de escalonamento deve ser justo com todos os processos, onde cada um deve ter uma chance de usar o processador.

**Utilização da CPU**: mede o percentual de uso, que deve ser o maior possível.

**Through put**: número de processos que foram completados por unidade de tempo.

**Tempo turn around**: é a soma dos tempos gastos pelo processo esperando para obter a CPU (fila de prontos), esperando por memória, executando na CPU e esperando por E/S.

**Tempo de espera**: soma dos períodos de tempo gastos esperando na fila de prontos.

**Tempo de resposta**: tempo decorrido entre a submissão de um processo até que a primeira resposta seja obtida. Não é considerado o tempo gasto com a efetiva saída do pedido, uma vez que este depende da velocidade do dispositivo de saída.

</br>

### Políticas de escalonamento não preemptivas

**Escalonamento First Come First Served (FCFS)**: Trata-se do algoritmo de escalonamento de implementação mais simples. Com este algoritmo de escalonamento, o primeiro processo que solicita a CPU é o primeiro a ser alocado.

Nesta política de escalonamento, o tempo médio de espera é, com frequência, um tanto longo. Outro ponto é que processos importantes podem ser obrigados a esperar devido à execução de outros processos menos importantes dado que o escalonamento FCFS não considera qualquer mecanismo de distinção entre processos.

**Política FIFO**: First in First out, ou seja, o primeiro a entrar é o primeiro a sair.

**Escalonamento Shortest Job First (SJF)**: o processo que tem o menor ciclo de processamento (tempo de execução) será selecionado para usar o processador.

Esta política é considerada ótima, mas impossível de implementar na prática já que não há modo de saber o tempo de duração do processo.

Existe uma variante preemptiva deste algoritmo onde o escalonamento é realizado não com base no tempo total de execução do processo, mas no tempo previsto para a duração de seu próximo CPU burst.

</br>

### Políticas de escalonamento preemptivas

**Escalonamento por prioridade**: A cada processo é associada uma prioridade e a CPU é alocada para o processo com a mais alta prioridade. Processos com prioridades iguais são escalados segundo a política FCFS.

A prioridade de um processo pode ser de dois tipos:

**Prioridade estática**: não muda durante a vida do processo;

**Prioridade dinâmica**: prioridade ajustada de acordo com o tipo de processamento e/ou carga do sistema.

Este escalonamento pode ser tanto preemptivo quanto não preemptivo.

O maior problema deste escalonamento é o _Starvation_ (processo de baixa prioridade ser indefinidamente postergado). Um método para prevenir “starvation” é o “aging”. Consiste em ir aumentando gradualmente a prioridade de um processo, à medida que ele fica esperando.

**Escalonamento Round Robin ou circular**: Cada processo ganha um tempo limite para sua execução. Após esse tempo ele é interrompido e colocado no fim da fila de prontos. Este tempo é chamado de fatia de tempo, “time-slice” ou quantum. Geralmente se situa entre 100 e 300 ms.

O tempo médio de espera é geralmente longo. O desempenho do algoritmo depende bastante da escolha do quantum. A troca de contexto (alternar entre um processo e outro) requer certa quantidade de tempo para ser realizada. Sendo assim, se o quantum definido for muito pequeno, ocasiona uma grande quantidade de trocas de processos e a eficiência da CPU é reduzida; de forma análoga, a definição do quantum muito grande pode tornar a política Round Robin numa FCFS comum.

**Escalonamento por múltiplas filas**: Implementa diversas filas de processos no estado de pronto, uma para cada prioridade. Os processos devem ser classificados previamente em função do tipo de escalonamento para poderem ser corretamente alocados. Cada fila separada tem seu próprio algoritmo de escalonamento. Note que a prioridade é da fila não do processo.

**Escalonamento por múltiplas filas com realimentação**: Este escalonamento permite a troca entre as filas. O sistema tenta identificar dinamicamente o comportamento de cada processo, ajustando suas prioridades de execução e mecanismos de escalonamento. Este esquema é dito **mecanismo adaptativo**.

Quando o processo é criado, é posto na fila 1 (de mais alta prioridade). Se ele esgota seu quantum, é posto uma fila abaixo e recebe um novo quantum (maior). Se também esgota esse quantum, vai descendo sucessivamente de fila, até atingir a de menor prioridade, onde o escalonamento é circular. Neste esquema, os processos “I/O bound” ficam por mais tempo nas filas de alta prioridade, enquanto os “CPU bound” gastam seu tempo e passam para filas de menor prioridade.

**Escalonamento com múltiplos processadores**: É usado quando existem vários processadores.

Compartilhamento de carga: fornece uma fila separada para cada processador.

Problema: um processador pode estar ocioso enquanto o outro está sobrecarregado.

Solução: colocar uma só fila de prontos e deixar o escalonador decidir na hora da execução.

Existem 3 formas para esse tipo de escalonamento:

**Forma 1**: Uma maneira de escalonar é o processador ser autoescalonável, ou seja, **cada processador vai à fila e seleciona um processo**. Cuidados a serem tomados: não permitir que um processo seja escolhido por mais de um processador; não permitir que um processo não seja escolhido por nenhum processador.

**Forma 2**: Outra maneira é usar um processador como escalonador de processos para os outros processadores, criando uma estrutura mestre-escravo.

**Forma 3**: A terceira possibilidade é o multiprocessamento assimétrico, onde um processador é responsável por todas as decisões de escalonamento, processamento de E/S etc. Os demais processadores só executam código do usuário.

Para sistemas de tempo real, é importante definir alguns conceitos críticos:

**Tempo de chaveamento**: é aquele gasto pelo sistema para chavear o processamento entre dois processos independentes, ativos e de prioridade igual. Ocorre, por exemplo, no chaveamento por "time slice".

**Tempo de preempção**: é aquele que um processo de maior prioridade leva para tomar o controle de um, de menor prioridade, por ocasião da ocorrência de um determinado evento externo de interrupção.

**Tempo de latência de interrupção**: é aquele entre o recebimento de um pedido de interrupção pela CPU e a execução da primeira instrução da rotina de serviço da interrupção.

**Escalonamento de tempo real**: podemos definir em dois tipos de sistemas

**Sistemas de tempo real hard**: como as tarefas têm que terminar em tempos definidos, o SO tem que admitir o processo somente quando ele poderá terminar na hora certa; caso contrário, o SO deve rejeitar o pedido como impossível. Isto é conhecido como “Reserva de recurso”.

**Sistema de tempo real soft**: os processos de tempo real devem ter a mais alta prioridade. Essa prioridade não deve ser degradada com o tempo. Para esses processos não deve haver _time sharing_. O tempo de latência deve ser pequeno para que o processo possa começar a executar o mais rapidamente possível.

A gerência de memória possui duas grandes abordagens:

Manter os processos na memória principal durante toda a sua execução;

Mover os processos entre a memória principal e secundária (tipicamente disco), utilizando técnicas de swapping (permuta) ou de paginação.

Hierarquia de memória:

cache: pequena memória e muito rápida que trabalha em conjunto com o processador pra aumentar o seu desempenho

memória ram: onde são armazenados os processos em execução

HDD/SSD: onde armazenamos arquivos para serem acessados posteriormente.

**Memória lógica** é a manipulada e invisível pelos programas, sempre que uma aplicação necessita de memória, esse recurso é utilizado.

**Memória física** são circuitos eletrônicos que irão realmente armazenar os dados.

![Alocação Contínua](/media/sistemas_operacionais/alocacao-continua.jpeg)

## Gerenciamento sem permuta

### Alocação Contígua

Os primeiros sistemas implementaram uma técnica muito simples onde a memória principal disponível é dividida entre o **Sistema Operacional e o programa em execução**. Como este esquema de gerenciamento é utilizado em sistemas **monoprogramáveis**, temos apenas um processo em execução por vez. Nesta técnica, o tamanho máximo dos programas é limitado à **memória principal disponível**. Para superar esta limitação foi desenvolvido o conceito de **overlay**.

### Overlay

A técnica de overlay utiliza o conceito de **sobreposição**, ou seja, a mesma região da memória será ocupada por módulos diferentes do processo.

A técnica de overlay foi o primeiro uso do conceito de mover partes do processo, entre o disco e a memória principal, que acabaria por gerar as modernas técnicas de gerenciamento de memória onde a divisão dos módulos é totalmente transparente para o usuário.

Esse gerenciamento é de responsabilidade do usuário e, geralmente, é oferecido como um **recurso da linguagem**.

_Em um programa com estrutura de overlay, um módulo fica sempre residente (Módulo Raiz) e os demais são estruturados como em uma árvore hierárquica de módulos mutuamente exclusivos, em relação a sua execução, colocados lado a lado, em um mesmo nível da árvore, de modo que o mesmo espaço possa ser alocado para mais de um módulo, os quais permanecem no disco e serão executados um de cada vez por meio de comandos de chamada (call). Um módulo residente faz chamadas a um módulo de overlay em disco e este é carregado no espaço de overlay sobre outro módulo do mesmo nível que lá estava (daí a necessidade de serem mutuamente exclusivos)._

</br>

![Processo Overlay](/media/sistemas_operacionais/processo-overlay.gif)

</br>

## Alocação Particionada Fixa

Com os sistemas multitarefas surgiu a necessidade de manter mais de um processo de usuário, na memória, ao **mesmo tempo**. A forma mais simples de se conseguir isso consiste em dividir a memória em _n_ partições (possivelmente diferentes) e _alocar_ os diferentes processos em cada uma delas.

Nos primeiros sistemas, estas partições eram estabelecidas na **configuração do sistema operacional** e seu **tamanho** e sua **localização** somente podiam ser alterados realizando um **novo boot**.

Quando um processo inicia, este deve ser alocado em uma partição com tamanho suficiente para acomodá-lo. Duas estratégias podem ser adotadas para alocar o processo:

uma única fila de entrada: Todos os processos ficam na mesma fila e vão sendo alocados na menor partição livre que os possa acomodar.

uma fila por partição: Os processos são divididos em várias filas de acordo com o seu tamanho e alocados quando a partição atendida pela fila está disponível.

</br>

![Alocacao Particionada Fixa](/media/sistemas_operacionais/alocacao-particionada-fixa.jpeg)

</br>

Este método de gerência de memória baseado em partições fixas, de uma forma ou de outra, gera um grande **desperdício de memória**, posto que, um processo ao ser carregado em uma partição, se ele não ocupa todo o seu espaço, o restante não poderá ser utilizado por nenhum outro processo.

</br>

## Alocação com Partições Variáveis

A memória principal não é particionada em blocos de tamanhos predeterminados. Inicialmente apenas uma partição existe e ocupa toda a memória disponível para usuários. À medida que os processos vão sendo alocados, essa partição vai diminuindo até que não caibam mais processos no espaço restante, resultando em um único fragmento.

Quando um processo termina e deixa a memória, o espaço ocupado por ele se torna uma partição livre que o gerente de memória utilizará para alocar outro processo da fila por memória. Uma lista de partições livres é mantida com ponteiros indicando os buracos disponíveis para alocação.

</br>

![Alocacao Particionada Variavel](/media/sistemas_operacionais/alocacao-particionada-variavel.jpeg)
A escolha da partição para o próximo job da fila deverá ser feita de acordo com uma das seguintes políticas:

![Politicas Partição Variavel](/media/sistemas_operacionais/politicas-particao-variavel.gif)

</br>

**First-fit**: Procura alocar o job na primeira partição onde ele couber(a busca termina assim que a primeira região é encontrada). É a mais rápida. Justificativa: **probabilisticamente agrupa os jobs pequenos separando-os dos grandes**.

**Best-fit**: Aloca o job na partição disponível de tamanho mais próximo ao seu (a lista de áreas livres de memória tem que ser totalmente pesquisada). Produz a menor região resto. Justificativa: **busca deixar fragmentos livres menores**.

**Worst-fit**: Procura alocar o job na maior partição disponível onde ele couber (a lista de áreas livres de memória tem que ser totalmente pesquisada). Produz a maior região resto, é a pior das três. Justificativa: **Intuitivamente sempre caberá mais um job pequeno no espaço resultante**.

</br>

## Realocação e Proteção

As políticas de alocação de partição introduzem dois problemas essenciais que devem ser resolvidos: **realocação e proteção**.

**Módulo está em Imagem de Memória ou está com Endereçamento Absoluto** é quando um módulo foi link-editado e seus endereços já estão associados às posições físicas do espaço de memória onde ele será alocado.

Ao conjunto de endereços que um processo faz referências, sejam eles de dados ou de instruções, chamamos de Espaço de Endereçamento. Assim, definimos por _Espaço Lógico de Endereçamento_ ao **conjunto de objetos ou endereços lógicos por ele referenciados** e por _Espaço Físico de Endereçamento_ ao **conjunto de endereços físicos correspondentes**.

Para que um processo possa ser alocado, em qualquer posição da memória, ele **não pode estar com endereçamento absoluto** e, nesse caso, um **mapeamento de endereços deverá ser feito** entre os endereços dos objetos referenciados pelo processo (endereços lógicos) e os endereços absolutos (físicos) no espaço que eles estarão ocupando na memória principal.

Supondo “N” o espaço de endereços lógicos e “M” o espaço de endereços físicos, então o mapeamento de endereços pode ser denotado por uma função do tipo: f: N → M

</br>

### Relocação de memória

É a função que mapeia os endereços lógicos em endereços físicos.

Quando ela é feita pelo link-editor, durante a resolução das referências em aberto, na geração do módulo de carga, os **endereços são resolvidos em relação a uma base inicial e o processo só poderá ser alocado a partir dessa base**, ou seja, _sempre rodará no mesmo lugar da memória_.

Alguns sistemas deixam essa tarefa de relocação para o carregador (loader) ou ligador-carregador (link-loader) que faz a resolução das referências externas e a relocação de endereços no instante de carregar o processo na memória para sua execução.

No primeiro caso (**link-editor**), a carga em imagem de memória sempre **roda no mesmo lugar da memória**, enquanto que, no segundo caso, **pode rodar em qualquer lugar**. Assim, a relocação poderá ser:

**Estática**: Quando o mapeamento de endereços é feito antes do carregamento do módulo, a relocação é dita **estática**.

</br>

**Dinâmica**: Para que a tradução dinâmica de endereços possa ser efetuada é preciso que toda referência seja lógica, isto é, nenhum endereço no programa poderá estar representando uma posição física, pois será mapeado pelo hardware. Esse processo é chamado de **Relocação dinâmica** de endereços.

![Relocação de Memoria](/media/sistemas_operacionais/relocacao-de-memoria.jpeg)

</br>

### Registradores Base e Limite

Quando um processo é carregado na memória, o endereço “inicial” é colocado em um registrador base e todos os endereços de programa são interpretados como sendo relativos ao endereço contido no registrador base. **O mecanismo de transformação, neste caso, consiste em adicionar ao endereço do programa o endereço base, o que produz a localização da palavra de memória correspondente.**

![Registradores Base e Limite](/media/sistemas_operacionais/registradores-base-limite.png)

Consegue-se relocação dinâmica facilmente: **basta mover o programa e corrigir o conteúdo do registrador base**. Proteção pode ser obtida com a _inclusão de um segundo registrador_ (registrador limite) contendo o endereço da última posição de memória que o processo pode acessar.

O mapeamento de endereço realizado pelo mecanismo (por “hardware”) de transformação é assim:

![Mapeamento](/media/sistemas_operacionais/mapeamento.png)

O espaço de endereço mapeado é linear, seu tamanho é a diferença entre o registrador limite e o base. Esse tamanho é necessariamente menor ou igual do que o espaço de memória disponível na configuração da maquina.

![Espaço de endereçamento linear](/media/sistemas_operacionais/enderecamento-linear.png)

Para reduzir o tempo de mapeamento, é conveniente que os registradores base e limite sejam de processo rápido. O custo dos registradores pode ser reduzido e a velocidade aumentada se os bits menos significativos desses registradores forem removidos. Se tal ocorrer, então o espaço de endereços deve ser múltiplo de **2n**, onde **n** é igual ao número de bits removidos.

</br>

## Gerenciamento com permuta

### Swap de memória

Denominamos **swapping** a política de remover um processo da memória toda vez que ele fica bloqueado. Assim que sua condição estiver satisfeita e ele retornar à fila de prontos ele é novamente carregado na memória.

Naturalmente que, para fazer swap, é necessário haver relocação dinâmica durante a carga dos jobs.

O swap de memória possui algumas vantagens e desvantagens. São elas:

VANTAGENS:

Maior compartilhamento da memória (maior throughput de tarefas);

Menor fragmentação de memória;

Boa técnica para ambientes com processos pequenos e poucos usuários.

DESVANTAGENS:

Custo alto para fazer o swap, por ser uma operação com memória auxiliar (disco)

### Memória virtual

O espaço de endereçamento lógico de um programa tem que ser mapeado em um espaço de endereçamento físico de memória.

Essa correspondência pode ser deixada totalmente a cargo do S.O., de forma que o programa não tenha nenhuma responsabilidade em se ater a um determinado tamanho de memória física disponível.

O conjunto de endereços que um programa pode endereçar, pode ser muito maior que a memória física disponível para o processo, em um determinado momento, ou mesmo que o total de memória fisicamente disponível na máquina. A esse conjunto de endereço chamamos de _espaço de endereçamento virtual_. Ao conjunto de **endereços reais de memória** chamamos _espaço de endereçamento real_.

Como os programas podem ser maiores que a memória física, somente uma parte de cada programa pode estar na memória durante a execução. As partes que não são necessárias em um determinado instante, ficam em disco e só são carregadas quando se tornarem necessárias. Todo o processo é transparente para o usuário e mesmo para os compiladores e link-editores, pois estes trabalham apenas com o espaço de endereçamento virtual. Apenas o S.O. se incube de carregar ou descarregar as partes necessárias e mapeá-las no espaço de endereçamento real durante a execução.

![Alocação com permuta](/media/sistemas_operacionais/permuta.png)

Como consequência desse mapeamento o programa não precisa estar nem mesmo em regiões contíguas de memória. O nível de fracionamento do programa deve ser escolhido de forma a **não comprometer o desempenho**, à medida que a tarefa de mapeamento é feita pelo S.O., juntamente com recursos de hardware. A memória (tanto virtual como real) é dividida em blocos e o S.O. mantém tabelas de mapeamento para cada processo, que relacionam os blocos da memória virtual do processo com os blocos da memória real da máquina.

</br>

### Paginação

O espaço de endereços é dividido em blocos de igual tamanho que chamamos de páginas. A memória principal também é dividida em blocos de mesmo tamanho (igual ao tamanho da página) denominados molduras.

Esses blocos de memória real são compartilhados pelos processos, de forma que a qualquer momento, um determinado processo terá algumas páginas residentes na memória principal (as páginas ativas), as restantes na memória secundária (as páginas inativas). O mecanismo da paginação possui duas atribuições:

Executar a operação de mapeamento, isto é, determinar qual página referenciada e em que bloco de memória (se for o caso) ela se encontra.

Transferir páginas da memória secundária para os blocos da memória principal (quando for requerido) e guardá-las de volta na memória secundária quando elas não estiverem em uso.

Com o objetivo de determinar qual a página referenciada por um endereço de programa, interpreta-se os bits mais significativos do endereço virtual como sendo o número da página dentro de uma tabela de páginas que é mantida pelo S.O. para cada processo ativo. Já os bits menos significativos indicam a localização da palavra na página selecionada:

![Paginação](/media/sistemas_operacionais/paginacao.png)

Se o tamanho da página é **2^n** palavras, então, os **n** bits menos significativos do endereço de programa representam o deslocamento, e os bits restantes indicam o número da página. O número total de bits do endereço de programa é suficiente para endereçar inteiramente a memória virtual.

A divisão de um endereço de programa no par (número de página, deslocamento) é feita pelo hardware e é completamente transparente ao programador.

![Mapeamento paginação](/media/sistemas_operacionais/mapeamento-paginacao.jpeg)

Se chamarmos de Z o tamanho da página, então: “p” é o quociente e “d” o resto da divisão de “a” por Z.

EXEMPLO:

Páginas com 16 endereços, logo, 4 bits de endereçamento;

Endereços virtuais de até 10 bits, logo, 1024 endereços;

Memória física de 256 endereços.

Então, se quiséssemos acessar o endereço binário 0010010111 a composição, pelo esquema acima, seria:

Os quatro últimos bits (0111) são o deslocamento d dentro da página;

Os seis primeiros bits (001001) são o número da página.

Como temos 1024 endereços e páginas de 16 endereços, então temos 1024/16= 64 páginas na tabela de páginas.

Como temos 256 endereços reais, então temos 256/16 = 16 blocos físicos de memória (blocos de 0 a 15).

![Exemplo mapeamento paginado](/media/sistemas_operacionais/exemplo-mapeamento-paginado.jpeg)

</br>

### Page fault

Normalmente, o número de blocos alocados a um processo é menor do que o número de páginas que ele usa. Por isso é possível que um endereço de programa referencie uma **página ausente**. Nesse caso, a entrada (da tabela) correspondente estará “vazia” e uma interrupção do tipo **falta de página (page fault)** é gerada sempre que uma página inativa é requerida.

_Uma interrupção é um evento externo que faz o processador parar a execução do programa corrente e desviar a execução para um bloco de código chamado rotina de interrupção. Ao terminar o tratamento de interrupção o controle retorna ao programa interrompido, exatamente, no mesmo estado em que estava quando ocorreu a interrupção._

![Page Fault](/media/sistemas_operacionais/page-fault.jpeg)

A interrupção faz com que o mecanismo da paginação inicie a transferência da página ausente da memória secundária para um dos blocos da memória principal e atualize a tabela de páginas.

O processo muda de estado, ficando bloqueado até que a transferência chegue ao fim.

As páginas são transferidas da memória secundária para a principal apenas quando são referenciadas, isso é chamado de **paginação por demanda**.

O sistema tenta prever quais páginas serão referenciadas pelo programa, trazendo-as para a memória antecipadamente, evitando assim a ocorrência do page fault, isso é **paginação antecipada**.

A posição ocupada por uma página na memória secundária é guardada em uma tabela separada ou na própria tabela de páginas. No último caso, é necessário um “bit de presença” para cada entrada da tabela de páginas, indicando se a página está ativa (está na memória física) ou não.

Se não houver nenhum bloco de memória disponível então é necessário desocupar um dos blocos para a página cuja presença está sendo solicitada. A escolha do bloco é função do **algoritmo de troca**. A transformação de endereços é função do hardware, enquanto que o algoritmo de troca é feito pelo software.

![Desoculpação de blocos](/media/sistemas_operacionais/desoculpacao-blocos.jpeg)

</br>

### Políticas de paginação

Para minimizar a ocorrência de page faults surgiu o conceito de working set.

Working set é o conjunto de páginas mais acessadas por um determinado processo.

Quando um programa começa a executar, a possibilidade de que ele requisite páginas que não estão na memória é muito grande. Entretanto, à medida que mais páginas vão sendo carregadas, a ocorrência de page faults vai diminuindo, devido ao princípio da localidade dos programas, já explicado quando falamos de memória cache.

**Capacidade**: quanto mais páginas no working set menos processos podem estar carregados ao mesmo tempo.

**Velocidade**: quanto mais páginas no working set menos page fault ocorrem, logo, melhor desempenho.

Definido o working set, resta definir qual deve ser a página a retirar da memória quando ocorre um page fault e uma página precisa ser carregada.

Antes de descartar qualquer página, o S.O. precisa saber se houve alguma alteração na página enquanto ela esteve na memória. Se houve, então ela precisa ser salva em disco antes de ser descartada, para que nenhum dado se perca. O S.O. mantém um bit na tabela de páginas chamado bit de modificação. Caso o bit indique que houve mudança, a página é salva em um arquivo de paginação, onde poderá ser futuramente resgatada.

As políticas de liberação de páginas são:

**Página aleatória**: escolhe-se simplesmente qualquer página. A desvantagem é que pode se escolher uma página que seja muito acessada.

**First-in-first-out**: retira-se a página carregada há mais tempo. A desvantagem é que pode retirar páginas que são acessas periodicamente.

**Least-recently-used**: retira-se a página utilizada pela última vez há mais tempo. A desvantagem é o overhead causado pela necessidade a cada acesso de atualização do momento em que a página foi acessada.

**Not-recently-used**: a página não utilizada nos últimos **k** acessos é substituída. A desvantagem também é o overhead causado pela necessidade, a cada acesso, de atualizar um contador de acessos à página.

**Least-frequently-used**: escolhe-se a página que tenha o menor número de acessos descritos em um contador de acessos. A ideia é manter, na memória, as páginas que são muito acessadas, entretanto, o problema é que páginas recém-carregadas no working set terão baixo número de acessos e serão indesejavelmente cotadas para serem retiradas.

VANTAGENS:

aumenta o espaço de endereçamento do processo;

admite código reentrante e compartilhamento de código pelos processos.

DESVANTAGENS:

overhead devido ao excesso de page faults tratados pelo sistema;

ocupa um arquivo só pra E/S de páginas;

ocupa muita memória do SO para as tabelas de páginas dos processos.

</br>

## Administração de Memória por Segmentação

A segmentação surgiu como uma alternativa de gerência de memória onde o programa agora não mais é dividido em blocos de comprimentos fixos (as páginas), mais sim, em segmentos de comprimentos variados, mas com um sentido lógico, isto é, **a paginação procedia a uma divisão física do programa e, às vezes, isso leva a um número muito grande de page faults por não observar suas características lógicas**.

A segmentação busca aproveitar exatamente essas características, agrupando em um segmento partes do programa que se referenciam mutuamente e que quando trazidas à memória estarão todas juntas não causando, o que nesse caso é chamado de **segment faults**, com tanta frequência.

O espaço de endereços torna-se bidimensional: endereços de programa são denotados pelo par (nome do segmento, endereço dentro do segmento). Para facilitar a implementação do mecanismo de transformação de endereços, o S.O. troca o nome do segmento por um nº, quando o segmento é referenciado pela primeira vez.

Considerando o par (s,d) como sendo um endereço de programa generalizado, onde s = número do segmento e d = endereço dentro do segmento, então o esquema de geração seria:

![Administração de Memória por Segmentação](/media/sistemas_operacionais/segmentacao.png)

A transformação de endereço é realizada por intermédio de uma **tabela de segmentos (uma tabela para cada processo)**. A s-ésima entrada da tabela contém o tamanho (l) e a posição inicial (a) da memória, onde o s-ésimo segmento foi carregado. As entradas da tabela são chamadas de “descritores de segmento”. O algoritmo de mapeamento é:

`extrair endereço de programa (s,d);`

`usar “s” para indexar tabela de segmentos;`

`retirar o endereço inicial do segmento (a);`

`se d < 0 ou d > l então “violação de memória”;`

`a + d é o endereço requerido.`

A busca de espaços para um segmento a ser trazido à memória nos leva novamente aos problemas de gerência por partições variáveis. A diferença aqui é que o espaço contíguo só é necessário para o segmento e não para todo o processo.

VANTAGENS:

reduz o número de page faults dentro de um segmento;

aproveita as características lógicas do processo;

dispensa uso de arquivo de paginação (ou segmentação)

DESVANTAGENS:

a soma de s + d, na tradução de endereços é mais lenta que a concatenação **p** e **d** na paginação;

a administração das áreas livres de memória é mais complicada (partições variáveis) e, portanto mais lenta;

as page faults (tratadas mais rapidamente, pois as páginas eram menores) são substituídas por segment faults que são maiores em comprimento.

</br>

### DIFERENÇA ENTRE SEGMENTAÇÃO E PAGINAÇÃO

A diferença principal entre a segmentação e a paginação é que a primeira busca uma divisão lógica do espaço de endereçamento do processo enquanto que a segunda busca uma divisão física desse espaço, ambas para implementação de uma política de memória virtual de um único nível.

Páginas têm seu tamanho determinado pelo tamanho da palavra, enquanto que segmentos têm seu tamanho determinado pelo tamanho da memória disponível.

</br>

## Administração por Segmentação com Paginação

Nem sempre é possível manter todos os segmentos na memória principal. Segmentos muito grandes poderiam, eventualmente, ultrapassar a memória disponível da máquina.

![Administração por Segmentação com Paginação](/media/sistemas_operacionais/administracao-por-pagina.png)

Em tempo de execução, alguns trechos de um segmento estariam na memória principal e outros não. A entrada da tabela de segmentos, isto é, o descritor de um segmento, apontaria para uma tabela de páginas (do segmento) ou então estaria vazia.

Vantagens do uso de paginação de implementação da segmentação:

não é necessário manter todas as páginas de um segmento na memória - apenas aquelas usadas correntemente.

as páginas de um segmento não precisam ser carregadas em áreas contíguas, isto é, podem ser dispersadas pela memória.

# Gerência de entrada e saída

Este nível é composto por processos servidores de E/S (gerentes de dispositivos e drivers) que também são processos do S.O. e também competem pelos seus recursos.

**Entrada** é toda instrução de envio de dados ao mundo exterior.

comandos de indicação de endereços dos dados

comandos de verificação do estado do dispositivo

**Saída** é toda instrução de recepção de dados do mundo exterior.

comandos de ação do dispositivo

comandos de atribuição de dados para a operação

As instruções de E/S são sempre do tipo:

sai comando

saem dados

entram dados

entra estado do dispositivo

Toda operação do tipo E/S pode ser subdividida no tempo em três etapas distintas:

início da E/S

transferência de dados

finalização da operação

</br>

## Técnicas empregadas em operações de Entrada e Saída

### Buffering

Esta técnica armazena temporariamente, em uma região de memória física do computador, chamada buffer, os dados enquanto eles são movidos entre processos ou dispositivos.

São utilizados quando existe uma grande diferença de velocidade entre a origem e o destino.

### Spooling

A técnica de spooling consiste em armazenar os dados em uma memória auxiliar. Ela permite que um dispositivo lento não provoque ociosidade na CPU.

### Buffering x Spooling

A técnica de buffering permite que uma tarefa utilize um buffer concorrentemente com um dispositivo de entrada e saída. O spooling, basicamente, utiliza o disco como um grande buffer, permitindo que dados sejam lidos e gravados em disco, enquanto outras tarefas são processadas.

O Gerenciamento de Entrada e Saída engloba o estudo dos princípios de hardware de software.

![Gerenciamento de Entrada e Saída](/media/sistemas_operacionais/principios-software-hardware.png)

## Software de E/S de nível de usuário

A visão dos dispositivos de E/S para o usuário consiste de bibliotecas vinculadas em programas de usuários. Essas bibliotecas são fornecidas pelas linguagens de programação e podem ser utilizadas pelos usuários e ligadas com seus programas para compor o arquivo executável.

As funções de entrada e saída são dependentes e específicas de cada linguagem de programação. As bibliotecas de entrada e saída não fazem parte do núcleo do Sistema Operacional. Elas são associadas às várias linguagens de programação.

</br>

## Software de E/S Independente de Dispositivo

A principal função do software de E/S independente de dispositivo é executar funções que são comuns para vários dispositivos, e oferecer uma interface uniforme para o software de nível de usuário.

**Nomeação do dispositivo**: Cada dispositivo deve receber um nome lógico e ser identificado a partir dele;

**Buferização**: Buffer é uma zona de memória temporária utilizada para armazenar dados enquanto eles estão sendo transferidos entre as diferentes camadas do software de E/S;

**Cache de dados**: Armazenar, na memória, um conjunto de dados que estão sendo frequentemente utilizados.

**Alocação e liberação**: Devido a alguns dispositivos admitirem, no máximo, um usuário por vez, o software de E/S deve gerenciar a alocação, a liberação e o uso destes dispositivos;

**Tratamento de erros**: O software de E/S deve fornecer mecanismos de manipulação de erros, informando à camada superior o sucesso ou o fracasso de uma operação.

</br>

### Drivers de Dispositivos

O driver de dispositivo (device driver) é composto de um conjunto de módulos de software cada um implementado para fornecer mecanismos de acesso a um dispositivo de entrada e saída específico. Assim, cada driver de dispositivo trata de um tipo de dispositivo ou de uma classe de dispositivos correlacionados.

De modo geral, um driver é responsável por aceitar uma solicitação abstrata (por exemplo, ler alguma informação) e cuidar para que esta solicitação seja atendida. Assim o driver de um dispositivo tem o conhecimento de como funciona a controladora.

</br>

### Interrupção

É um sinal informando que um evento ocorreu. Vários eventos podem gerar uma interrupção como, por exemplo, o fim de uma operação de E/S, erros de programa como divisão por zero ou acesso inválido à memória entre outros.

Cada interrupção é identificada com um número.

![Controle de Interrupção](/media/sistemas_operacionais/controle-de-interrupcao.png)

Quando ocorre uma interrupção o programa em execução passa ao estado de pronto e é iniciada a rotina de tratamento de interrupção.

Para cada interrupção, uma rotina de serviço é designada para tratar a interrupção.

![Rotinha de Interrupção](/media/sistemas_operacionais/rotina-de-interrupcao.png)

No decorrer da execução das instruções de um programa é solicitada uma operação de E/S, por exemplo, um determinado trecho deve ser copiado, do disco para memória principal, para que o fluxo de execução deste programa continue;

Como a velocidade de acesso aos dispositivos de E/S é menor que a velocidade de processamento das instruções por parte do processador, o processador desvia o fluxo de execução de instruções para outro programa e o solicitado passa a bloqueado;

O pedido de interrupção, normalmente, é gerado através da ativação de um sinal conectado ao processador (1). Ao ocorrer o pedido de interrupção, o processador interromperá a execução do programa, salvará o valor atual dos seus registradores (contexto) (3), identificará a origem do pedido de interrupção e em seguida, executará a rotina associada ao tratamento da situação que levou à ocorrência do pedido de interrupção (4);

Essas rotinas de tratamento são parte do S.O. e encontram-se carregadas na memória principal. O endereço de cada rotina é obtido em uma tabela, chamada vetor de interrupções.

![Processo de rotina de Interrupção](/media/sistemas_operacionais/processo-rotina.gif)

</br>

## Princípios de hardware

Um sistema de computação de uso geral moderno consiste de uma CPU e em uma série de controladoras de dispositivos conectadas por um barramento comum que fornece acesso à memória compartilhada.

Cada controladora de dispositivo está encarregada de um tipo específico de dispositivo (por exemplo, unidades de disco, dispositivos de áudio e monitores de vídeo). A CPU e as controladoras de dispositivo podem executar de modo concorrente, competindo pelos ciclos de memória.

![Princípios de hardware](/media/sistemas_operacionais/principios-de-hardware.jpeg)

</br>

### Dispositivos de E/S

É o mecanismo utilizado como interface entre o mundo exterior e o computador.

Existe uma enorme diversidade de dispositivos que são classificados quanto a fluxo de dados da seguinte forma:

**Dispositivos de entrada**: caracterizados por conter um fluxo de informações do dispositivo para o sistema, ou seja, responsáveis por inserir, no sistema, informações do mundo externo, como, por exemplo, teclado e mouse.

**Dispositivos de saída**: caracterizados pelo fluxo de informações do sistema para o mundo externo, ou seja, responsáveis por disponibilizar respostas ao mundo externo como, por exemplo, uma impressora.

**Dispositivos de entrada e saída**: contemplam os dois fluxos como, por exemplo, uma placa de rede.

</br>

## Controladoras de Dispositivos

Os dispositivos são ligados ao computador através de um componente de hardware chamado de interface. Devido à diversidade de tipos de dispositivos, que abstrai diferentes formas de operações e complexidade, as interfaces empregam, no seu projeto, outro componente de hardware conhecido como controlador de dispositivo.

A controladora de dispositivo (chamada também de adaptador de dispositivo) trata-se de um componente eletrônico, comumente na forma de uma placa de circuito impresso, que pode ser inserida na placa mãe do computador.

O dispositivo em si trata-se de um componente mecânico. Uma controladora pode manipular mais de um dispositivo e, quando padronizadas, podem ser fabricadas por diversas empresas. Como exemplo, temos as controladoras de disco IDE ou SCSI.

![Controladoras de Dispositivos](/media/sistemas_operacionais/tipos-controladora.png)

A distinção entre dispositivo e controladora deve ser ressaltada, já que o sistema operacional vê a controladora, não o dispositivo.

Cada controladora possui registradores que são utilizados para comunicação com a CPU. A operação de E/S é realizada quando o S.O. escreve os comandos nestes registradores. Quando o comando é aceito a CPU pode atender a outra tarefa, pois, a partir deste ponto, a controladora executa o comando dado e efetiva a operação solicitada.

Ao final da operação a controladora provoca uma interrupção visando permitir que o S.O. assuma a CPU e teste o resultado da operação. A CPU obtém o resultado e o status do dispositivo pela leitura de um ou mais bytes de informação nos registradores da controladora.

</br>

## Acesso Direto à Memória (DMA)

Muitas controladoras, como, por exemplo, as dos HDs modernos suportam DMA.

Uma controladora comum (sem acesso direto à memória) armazena os dados em seu buffer e verifica possíveis erros. A seguir, gera uma interrupção. O Sistema Operacional passa a executar e realiza a leitura do buffer da controladora, cada byte por vez, e armazena-os na memória principal. Esta operação, naturalmente, exige desperdício de CPU.

O DMA foi projetado para liberar a CPU do trabalho de cópia dos dados da controladora para a memória. O controlador DMA é conectado ao barramento de dados e de endereços do computador, para ter a capacidade de acessar diretamente endereços de memória. Desta forma, após os dados terem sido lidos do dispositivo, a controladora se encarrega de copiá-los para a memória, sem interferência da CPU. Após terminar a transferência dos dados para a memória principal, a controladora DMA gera uma interrupção para o Sistema Operacional, que ao ser iniciado já encontra o dado em memória principal.

A transferência via DMA é processada sem intervenção da CPU, conforme nos mostra o exemplo abaixo:

![Acesso Direto à Memória](/media/sistemas_operacionais/acesso-memoria.png)

## Gerência de arquivos

Um arquivo pode ser entendido como um conjunto de dados armazenados em um dispositivo físico não volátil, com um nome ou outra referência que permita sua localização posterior.

Do ponto de vista do usuário e das aplicações, o arquivo é a unidade básica de armazenamento de informação em um dispositivo não volátil, pois para eles não há forma mais simples de armazenamento persistente de dados.

Como um dispositivo de armazenamento pode conter milhões de arquivos, estes são organizados em estruturas hierárquicas denominadas diretórios.

![Gerência de arquivos](/media/sistemas_operacionais/diretorio-armazenamento.png)

O Sistema de Arquivos pode ser entendido então como a organização física e lógica dos dados armazenados de forma persistente em um dispositivo físico não volátil.

Existem vários sistemas de arquivos nos Ss.Os. dentre os quais podemos citar FAT e NTFS do Windows.

</br>

### Atributos

Como vimos, um arquivo é uma unidade de armazenamento de informações que podem ser dados, código executável etc. Cada arquivo é descrito por atributos, cujo conjunto varia de acordo com o sistema e arquivos utilizado. Os atributos mais usuais são:

**Nome**: String de caracteres que identifica o arquivo para o usuário, como “foto1.jpg”, “relatório.pdf”, “hello.c” etc.

**Tipo**: Indicação do formato dos dados contidos no arquivo, como áudio, vídeo, imagem, texto etc. Muitos sistemas operacionais usam parte do nome do arquivo para identificar o tipo de seu conteúdo, na forma de uma extensão:“.doc”,“.jpg”,“.mp3”, etc.

**Tamanho**: Indicação do tamanho do conteúdo do arquivo, em bytes ou registros.

**Datas**: Para fins de gerência, é importante manter as datas mais importantes relacionadas ao arquivo, como suas datas de criação, de último acesso e de última modificação do conteúdo.

**Proprietário**: Em sistemas multiusuários, cada arquivo tem um proprietário, que deve estar corretamente identificado.

**Permissões de acesso**: Indicam que usuários têm acesso àquele arquivo e que formas de acesso são permitidas (leitura, escrita, remoção etc.).

**Localização**: Indicação do dispositivo físico onde o arquivo se encontra e da posição do arquivo dentro do mesmo.

**Outros atributos**: Vários outros atributos podem ser associados a um arquivo, por exemplo, para indicar se é um arquivo de sistema, se está visível aos usuários, se tem conteúdo binário ou textual etc. Cada sistema de arquivos normalmente define seus próprios atributos específicos, além dos atributos usuais.

</br>

![Extensão de arquivos](/media/sistemas_operacionais/tipos-de-extensao.png)

## Operações

As aplicações e o sistema operacional utilizam um conjunto de operações para manipular arquivos.

As operações básicas, envolvendo arquivos, são:

**Criar**: a criação de um novo arquivo implica em alocar espaço para ele no dispositivo de armazenamento e definir seus atributos (nome, localização, proprietário, permissões de acesso, etc).

**Abrir**: antes que uma aplicação possa ler ou escrever dados em um arquivo, ela deve solicitar ao sistema operacional a "abertura" desse arquivo. O sistema irá então verificar se o arquivo existe, verificar se as permissões associadas ao arquivo permitem aquele acesso, localizar seu conteúdo no dispositivo de armazenamento e criar uma referência pra ele na memória da aplicação.

**Ler**: permite transferir dados presentes no arquivo para uma área de memória da aplicação.

**Escrever**: permite transferir dados na memória da aplicação para o arquivo no dispositivo físico, os novos dados podem ser adicionados no final do arquivo ou sobrescrever dados já existentes.

**Mudar atributos**: para modificar outras características do arquivo, como nome, localização, proprietário, permissões, etc.

**Fechar**: ao concluir o uso do arquivo, a aplicação deve informar ao sistema operacional que o mesmo não é mais necessário, a fim de liberar as estruturas de gerência do arquivo na memória do núcleo.

**Remover**: para eliminar o arquivo do dispositivo, descartando seus dados e liberando o espaço ocupado por ele.

</br>

### Organização Sequencial

Neste tipo de arquivo, os registros são acessados, quer para leitura quer para escrita, de forma sequencial, isto é, a escrita de um registro só é feita após o último registro escrito e a leitura de um registro só é possível após todos os registros anteriores terem sido lidos.

Existe um ponteiro “invisível” que assinala para o registro corrente e que é incrementado de forma automática após cada leitura ou escrita. Dizemos que o ponteiro é invisível porque **não é necessário lidar com ele no algoritmo**. O sistema de arquivos da linguagem que se utilizar (e que oferecer organização sequencial de arquivos) lida com o ponteiro automaticamente a cada operação de abertura, leitura ou escrita do arquivo. Quando abrimos um arquivo, devemos informar se desejamos ler ou escrever e, a partir de então, só podemos realizar esse tipo de operação (leitura ou escrita) até o fechamento do arquivo.

O esquema mostrado, a seguir, ilustra o funcionamento das operações de leitura em um arquivo sequencial chamado Agenda:

![Funcionamento das operações de leitura](/media/sistemas_operacionais/operacao-de-leitura-sequencial.png)

Na escrita, o ponteiro pode ser posto no início do arquivo (se for um arquivo novo) ou no final do arquivo (se quisermos acrescentar registros aos já existentes). A diferenciação é feita no comando de abertura. Veja:

![Funcionamento das operações de escrita](/media/sistemas_operacionais/operacao-de-escrita-sequencial.png)

Para lidar com arquivos sequenciais, existe uma função lógica (Verdadeiro/Falso) indicando se o ponteiro chegou ao fim do arquivo (na leitura). Chamamos essa função de EOF (_end of file_).

![Função de EOF (*end of file*)](/media/sistemas_operacionais/end-of-file.png)

Essa função é usada como critério de parada em repetições para testar se já atingimos o fim do arquivo sequencial.

### Organização Direta

Neste tipo de arquivo, podemos acessar um determinado registro no meio do arquivo pelo seu número (posição do registro dentro do arquivo). O arquivo, uma vez aberto, aceita tanto operações de leitura quanto de escrita.

### Organização Indexada

Neste tipo de arquivo, existe um local do registro chamado **campo chave** que permite o acesso a um registro determinado. Agora não temos mais um índice necessariamente numérico, como nos arquivos diretos.

Para podermos utilizar qualquer campo como índice (campo chave), o sistema de gerenciamento de arquivos da linguagem (que é transparente para o usuário) utiliza outro arquivo, chamado **arquivo de índice**, que é **ordenado** pelo campo chave. Esse arquivo de índice, possui um campo com a chave e outro com o número do registro correspondente àquela chave no arquivo principal.

Por exemplo, suponha que temos um arquivo com nome, endereço e telefone, e o campo chave é nome. Observe como seria a organização para os dados:

![Exemplo de organização de dados](/media/sistemas_operacionais/organizacao-indexada.png)

Note que o arquivo de índice é ordenado. Assim, quando precisa localizar um registro no arquivo principal, o sistema de arquivos percorre primeiro o de índice, procurando pelo nome chave. Após encontrar a chave, pega o índice (que representa a posição) do registro completo referente àquela chave no arquivo principal.

</br>

### Organização lógica

O sistema de arquivos é quebrado em **partições** conhecidas como _volumes_.

Existe pelo menos uma partição e é nessa estrutura de mais baixo nível que os arquivos efetivamente residem. Um mesmo dispositivo físico (uma unidade de disco magnético, por exemplo) pode conter mais de uma partição, cada uma delas tratada como um dispositivo virtual.

Informações sobre os arquivos são guardadas em entradas no **diretório** de dispositivos ou tabela de volumes. O diretório de dispositivos, também conhecido simplesmente como _diretório_, pode ser visto como uma estrutura de dados contendo informações sobre os arquivos tais como localização física, nome, atributos e demais informações que o sistema queira guardar sobre os arquivos. Veja um exemplo de disco com duas partições:

![Disco com duas partições](/media/sistemas_operacionais/disco-com-duas-particoes.png)

Nas organizações de diretórios mais antigas, todos os arquivos estavam contidos em um só diretório. Isso introduzia limitações no número de arquivos e, principalmente, na nomeação dos arquivos, já que o nome deve ser único dentro do diretório. Assim, os diretórios evoluíram para estruturas com diversos níveis.

Esses diretórios são, normalmente, implementados como estruturas de árvores. Na estrutura principal ou Master File Directory (MFD), existem ponteiros para os diretórios de cada usuário ou User File Directories (UFDs) que, por sua vez, possuem apontadores para os demais subdiretórios, que podem ser criados por cada usuário e assim por diante, em uma estrutura que culmina pela referenciação dos arquivos físicos propriamente ditos.

![Estrutura de árvore](/media/sistemas_operacionais/estrutura-de-arvore.png)

</br>

### Diretórios compartilhados

São estruturas que permitem que subdiretórios comuns sejam compartilhados. Um arquivo compartilhado existe no sistema em dois lugares, mas não como uma cópia, ou seja, só existe um arquivo físico. Assim, **mudanças realizadas por um usuário são visualizadas por outro**. Arquivos e subdiretórios compartilhados podem ser implementados de duas formas: **grupos de acesso ou listas de controle**.

Em ambos os mecanismos, é necessário estabelecer níveis de proteção diferentes para os diferentes usuários. Direitos de leitura, escrita, execução, criação e remoção de arquivos ou diretórios devem ser estabelecidos para cada usuário.

**Grupos de acesso**: no esquema de _listas de controle_, cada arquivo ou diretório a ser compartilhado possui uma lista associada, onde são relacionados os usuários e as operações que cada um desses usuários pode fazer. As desvantagens são o tamanho dessa estrutura que pode ser grande se o arquivo ou diretório for compartilhado por muitos usuários. Além disso, há o problema do acesso sequencial à lista de compartilhamento, que também é lento.

**Listas de controle**: no esquema de grupos de usuários, os usuários que queiram compartilhar arquivos devem pertencer a um mesmo grupo. Quando da criação do arquivo é adicionada uma estrutura que descreve quais os níveis de proteção para: o dono (_owner_), o grupo (_group_) e todos (_all_).

![Grupo de usuários](/media/sistemas_operacionais/grupo-de-usuarios.png)

</br>

### Organização Física

Os sistemas precisam manter o controle da localização física dos arquivos nos dispositivos. Os dispositivos físicos são, normalmente, divididos em blocos e a estrutura de gerência de arquivos deve mapear em quais blocos físicos se encontra um determinado arquivo. Para saber quais blocos estão livres, é preciso manter um registro de blocos livres. Esse registro pode ser feito de três formas. São elas:

**Mapa de bits**: uma forma de fazer esse registro é manter um mapa de bits, um bit para cada bloco, que indique em quais blocos estão livres. A desvantagem é a quantidade de memória empregada.

**Lista encadeada**: a segunda forma é manter uma lista encadeada de blocos livres no disco. A desvantagem é ser necessário guardar ponteiros nos próprios blocos, para o bloco seguinte, além de se percorrer sequencialmente a estrutura para encontrar os blocos.

**Tabela de blocos**: a terceira forma é, considerando-se que a maioria dos blocos são alocados em conjunto, manter uma tabela de blocos livres contíguos com localização e tamanho de cada conjunto de blocos.

![Tabela de Conjuntos Livres Contínuos](/media/sistemas_operacionais/tabela-conjuntos-livre.jpeg)

Para alocar espaço para um arquivo no disco, os primeiros sistemas procuravam por um espaço contíguo de blocos, de forma que só era necessário guardar o bloco inicial e o tamanho em blocos que o arquivo ocupava.

Naturalmente, isso é bastante ineficiente porque demanda escolher um bloco que tenha tamanho satisfatório para o arquivo (políticas de First-fit, Best-fit ou Worst-fit, como visto para partições de memória), além dos tradicionais problemas de fragmentação que ocorrem em longo prazo (depois de muitos arquivos terem sido criados e apagados). A solução foi criar esquemas de alocação não contígua.

Uma saída é a alocação encadeada, onde toda entrada de arquivo no diretório possui um apontador para um bloco inicial do disco que, por sua vez, aponta para o próximo bloco do arquivo e assim por diante. A desvantagem é, novamente, a obrigatoriedade do acesso sequencial.

Outra solução é o acesso indexado, em que um determinado bloco, chamado **bloco de índice**, contém os ponteiros para os demais blocos do arquivo no disco.

![bloco de índice](/media/sistemas_operacionais/bloco-de-indice.jpeg)

## Sistema de arquivos FAT e NTFS

FAT (File Allocation Table) é o principal sistema de arquivos de computadores para vários sistemas operacionais, na maior parte do DOS, incluindo o DR-DOS, OpenDOS, FreeDOS, MS-DOS, Microsoft Windows (até e incluindo o XP).

FAT é usado também para flash drives e cartões de memória removíveis.

Sistema de arquivos é o método para armazenar e organizar arquivos de computador e os dados que eles contêm para torná-los fácil de encontrar e acessá-los. A tabela a seguir mostra em que sistema de arquivo FAT um flash drive ou cartão de memória deve ser formatado:

![Sistema de arquivos](/media/sistemas_operacionais/sistemas-de-arquivo.png)

NTFS é o sistema de arquivos padrão do Windows Server 2008 e do Windows 10.

NTFS é destinado ao uso em unidades do sistema Windows (discos rígidos e drives de estado sólido).

NTFS tem várias melhorias em relação ao FAT, como suporte melhorado para metadados e o uso de estruturas de dados avançados de confiabilidade, e utilização de espaço em disco, além de extensões adicionais, tais como listas de segurança de controle de acesso e sistema de arquivos jornalístico.

## Estrutura de armazenamento de massa

![Armazenamento de massa](/media/sistemas_operacionais/armazenamento-de-massa.png)

## Discos Magnéticos

Discos magnéticos são dispositivos para armazenamento não volátil de dados.

Os atuais discos magnéticos ou discos rígidos incorporam eletrônica de controle, motor para girar o disco, cabeças de leitura / gravação e o mecanismo para o posicionamento das cabeças.

\*Armazenamento não volátil: Tipo de armazenamento que independe de alimentação de energia para manter seu conteúdo e, portanto permanece gravado mesmo após ser desligado o computador, mas que pode, a critério do usuário, ser apagado ou alterado.

![Disco magnetico](/media/sistemas_operacionais/disco-magnetico.png)

Os discos possuem um formato circular. Suas duas superfícies são cobertas com um material magnético.

![Formato disco magnetico](/media/sistemas_operacionais/formato-disco-magnetico.png)

Durante a formatação, cada superfície é dividida em trilhas e cada trilha é dividida em setores (também chamados de bloco do disco), onde são armazenadas as informações.

\*Formatação: O processo de marcação magnética das trilhas e dos setores, em um disco, faz parte da "formatação" do disco. Esta formatação é dependente do sistema operacional que usará o disco.

![Trilha disco magnetico](/media/sistemas_operacionais/trilha-disco-magnetico.png)

As informações são lidas ou escritas através de uma cabeça de leitura/gravação.

## Tempo de acesso ao disco

É definido como o período decorrido entre a ordem de acesso e o final da transferência dos dados. Ele não é constante e varia em função da localização dos bancos no disco. O tempo de acesso pode ser definido com a seguinte fórmula:

![Formula tempo de acesso](/media/sistemas_operacionais/formula-tempo-de-acesso.png)

Os discos rígidos atuais são construídos com muitas superfícies de gravação, montadas em torno de um eixo comum. Os braços atuadores responsáveis pelo posicionamento das cabeças de leitura/gravação são montados em uma única estrutura, de forma que eles se movam solidariamente.

![Formula tempo de acesso](/media/sistemas_operacionais/funcionamento-disco-magnetico.png)

Observe que quando uma determinada cabeça é posicionada sobre uma trilha, as demais cabeças estarão também posicionadas sobre as trilhas das outras superfícies localizadas à mesma distância do eixo central e, portanto, todas as trilhas (localizadas a uma mesma distância do eixo central do disco) poderão ser acessadas simultaneamente por todas as cabeças.

Surge, neste caso, o conceito de cilindro: O conjunto de trilhas localizado a uma mesma distância do eixo central. Desta forma, em um disco de quatro cabeças (quatro faces) o cilindro 10 seria composto por todos os setores localizados na trilha 10 da face 1, na trilha 10 da face 2, na trilha 10 da face 3 e na trilha 10 da face 4.

Os dados gravados no mesmo cilindro (na mesma trilha, porém em superfícies diferentes) podem ser acessados (lidos ou gravados) sem que o braço atuador das cabeças de leitura/gravação tenha que ser movido.

</br>

## Gerenciamento de espaço livre em disco

### Mapa de bits

Cada bloco é representado por 1 bit, se o bloco está livre o bit é 0, se não é 1.

### Lista de blocos livres

Mantém todos os blocos livres ligados por uma lista, e guardar a cabeça (endereço inicial da lista) da lista. Aproveita os próprios blocos livres para armazenar os endereços da lista. Não é possível ter uma visão geral sobre a situação de um conjunto de setores, deve-se ler um a um, para saber se o setor está disponível ou não.

![Lista de blocos livres](/media/sistemas_operacionais/lista-de-blocos-livres.png)

### Bloco de Endereços

Utiliza-se o primeiro bloco livre, como bloco de endereços, para armazenar o endereço dos próximos "n" blocos livres, sendo que o bloco número "n", é outro bloco de endereços.

Guarda-se o endereço do primeiro bloco de endereços. Este método também permite, em uma única leitura (do bloco de endereços), saber sobre a situação de vários blocos, incluindo os endereços.

![Lista de blocos endereços livres](/media/sistemas_operacionais/bloco-de-enderecos.png)

</br>

### Lista de Blocos Livres contíguos

Aproveita a ideia de que sempre existem vários blocos livres contíguos. Mantém uma tabela de blocos livres, onde cada entrada, na tabela, contém o endereço do 1º bloco de um grupo de blocos contíguos e o tamanho do grupo.

![Lista de Blocos Livres contíguos](/media/sistemas_operacionais/bloco-de-enderecos.png)

## Alocação de espaço em disco

Uma das preocupações do sistema de arquivos é como alocar os espaços livres do disco para os arquivos, de forma que o disco seja mais bem utilizado e os arquivos possam ser acessados mais rapidamente.

Os três principais métodos de alocação de espaço do disco são:

### 1º alocação contígua

Este método procura identificar uma sequência contínua de blocos que apresente um tamanho suficiente para armazenar todas as informações relativas ao arquivo, ou seja, caso um arquivo precise de N blocos para o seu armazenamento, o sistema operacional procurará identificar uma sequência contínua de N blocos livres do disco.

Nesta técnica, o espaço só será alocado se for contíguo, caso contrário, o arquivo não poderá ser armazenado ou estendido. Se, por acaso, existir mais de uma possibilidade, então poderá ser utilizada uma técnica para selecionar uma opção.

As técnicas que podem ser utilizadas são: Worst-Fit, Best-Fit e First-Fit.

A alocação contígua de um arquivo é definida pelo endereço do primeiro bloco e seu comprimento, e, dessa forma, é colocada no diretório.

![Alocação contígua de arquivos](/media/sistemas_operacionais/alocacao-continua-arquivo.png)

### 2ª alocação ligada

Nesta técnica, os blocos alocados para um arquivo são encadeados em uma lista, não importando a contiguidade. Assim, seria armazenado no diretório o nome do arquivo e duas variáveis, isto é, os identificadores do primeiro e do último bloco do arquivo.

Em cada um dos blocos utilizados pelo arquivo, seria reservado um espaço para conter o endereço do próximo bloco da lista.

![Segunda alocação ligada](/media/sistemas_operacionais/segunda-alocacao-ligada.png)

### 3ª alocação indexada

Neste método, cada arquivo possui seu próprio bloco de índice, que é um vetor de endereços. A i- ésima entrada no bloco de índice aponta para o i-ésimo bloco do arquivo.

![Terceira alocação ligada](/media/sistemas_operacionais/terceira-alocacao-ligada.png)

## RAID

É a sigla para Redundant Array of Independent Disks ou, em tradução livre, algo como "Matriz Redundante de Discos Independentes". Trata-se, basicamente, de uma solução computacional combinando vários discos rígidos (HDs) para formar uma única unidade lógica de armazenamento de dados.

![RAID](/media/sistemas_operacionais/raid.png)

### Níveis de RAID

Para que um sistema RAID seja criado, é necessário utilizar pelo menos dois HDs (ou SSDs). Mas não é só isso: é necessário também definir o nível de RAID do sistema. Cada nível possui características distintas justamente para atender às mais variadas necessidades.

**RAID 0 (zero)**

Também conhecido como _striping_ (fracionamento), é aquele onde os dados são divididos em pequenos segmentos e distribuídos entre os discos.

Trata-se de um nível que não oferece proteção contra falhas, já que nele não existe redundância. Isto significa que uma falha, em qualquer um dos discos, pode ocasionar perda de informações para o sistema todo, especialmente porque "pedaços" do mesmo arquivo podem ficar armazenados em discos diferentes.

O foco do RAID 0 acaba sendo o desempenho, uma vez que o sistema praticamente soma a velocidade de transmissão de dados de cada unidade. Assim, pelo menos teoricamente, quanto mais discos houver no sistema, maior é a sua taxa de transferência.

![RAID control](/media/sistemas_operacionais/raid-control.png)

</br>

**RAID 1**

O RAID 1 é, provavelmente, o modelo mais conhecido. Nele, uma unidade "duplica" a outra, isto é, faz uma "cópia" da primeira, razão pela qual o nível também é conhecido como _mirroring_ (espelhamento).

Com isso, se o disco principal falhar, os dados podem ser recuperados imediatamente porque existem cópias no outro.

Perceba que, por conta desta característica, sistemas RAID 1 devem funcionar em pares, de maneira que uma unidade sempre tenha um "clone".

O nível RAID 1 é claramente objetivado na proteção dos dados, ou seja, não torna o acesso mais rápido. Na verdade, pode até ocorrer uma ligeira perda de desempenho, uma vez que o processo de gravação acaba tendo que acontecer duas vezes, uma em cada unidade.

![RAID control por unidade](/media/sistemas_operacionais/raid-control-unidade.png)

**RAID 0+1 e RAID 10**

Tal como você já deve ter imaginado, o nível RAID 0+1 é um sistema "híbrido" (hybrid RAID), ou seja, que combina RAID 0 com RAID 1. Para isso, o sistema precisa ter pelo menos quatro unidades de armazenamento, duas para cada nível. Assim, tem-se uma solução RAID que considera tanto o aspecto do desempenho quanto o da redundância.

![RAID control hibrido](/media/sistemas_operacionais/raid-control-hybrid.gif)

Há uma variação chamada RAID 10 (ou RAID 1+0) de funcionamento semelhante. A diferença essencial é que, no RAID 0+1, o sistema se transforma em RAID 0 em caso de falha; no RAID 1+0, o sistema assume o nível RAID 1.

![RAID com variação](/media/sistemas_operacionais/variacao-raid.gif)

**RAID 5**

É outro nível bastante conhecido. Nele, o aspecto da redundância também é considerado, mas de maneira diferente: em vez de existir uma unidade de armazenamento inteira como réplica, os próprios discos servem de proteção. Deste modo, pode-se inclusive montar o sistema com quantidade ímpar de unidades. Mas, como isso é possível? Com o uso de um esquema de paridade.

Neste método de proteção, os dados são divididos em pequenos blocos. Cada um deles recebe um bit adicional — o bit de paridade — de acordo com a seguinte regra: se a quantidade de bits '1' do bloco for par, seu bit de paridade é '0'; se a quantidade de bits '1' for ímpar, o bit de paridade é '1'.

![Bloco de RAID](/media/sistemas_operacionais/blocos-de-raid.png)

As informações de paridade — assim como os próprios dados — são distribuídas entre todos os discos do sistema. Via de regra, o espaço destinado à paridade é equivalente ao tamanho de um dos discos.

A partir daí, se em uma tarefa de verificação o sistema constatar, por exemplo, que o bit de paridade de um bloco é '1', mas ali há uma quantidade par de bits, percebe que há um erro.

Se houver apenas um bit com problema e se o sistema conseguir identificá-lo, conseguirá substituí-lo imediatamente. A restauração dos dados poderá ser feita inclusive depois de o HD ter sido trocado.

![Troca de bit](/media/sistemas_operacionais/troca-de-bit.png)

Como exemplo, imagine um bloco de dados com os bits '110X' e paridade '1'. O X indica um bit perdido, mas será que ele é '0' ou '1'? Como a paridade é '1', significa que o bloco é composto por quantidade ímpar de bits '1'. Logo, se X fosse '0', a paridade também deveria ser '0', pois ali existiria quantidade par de bits '1'. Isso significa que o bit X só pode ser '1'.

![Raid Controller](/media/sistemas_operacionais/raid-controller.gif)

### Implementação de RAID

Antigamente, montar sistemas RAID não era uma tarefa das mais simples e seu uso normalmente se limitava a servidores. Hoje, no entanto, é possível implementá-los até mesmo em computadores pessoais, mesmo porque praticamente qualquer sistema operacional moderno (Windows, Linux, Mac OS X, entre outros) suporta este recurso.

A maneira mais fácil de fazer isso é adquirindo uma placa-mãe contando com uma controladora RAID. Em poucas palavras, este dispositivo, que pode funcionar com interfaces PATA, SATA ou SCSI, identifica as unidades de armazenamento conectadas e as fazem trabalhar como um sistema RAID. Sua configuração geralmente é feita a partir do setup do BIOS, embora algum software de controle possa ser fornecido para funcionar no sistema operacional.

Se a placa-mãe não possuir controladora RAID, é possível adicionar placas que acrescentam esta função. Estes dispositivos, normalmente, podem ser encontrados utilizando interface PCI ou PCI Express.

## Estrutura de armazenamento de massa

Um SO fornece serviços como:

Gerenciamento do uso do processador

alocação dos processos (programas em execução) na memória principal

Controle do acesso aos dispositivos de entrada e saída

alocação de informações nos dispositivos de armazenamento (gerenciamento do sistema de arquivos) etc.

Este tipo de SO é denominado **Sistema Operacional Local (SOL)**.

Os computadores que antes funcionavam stand alone, tinham seu acesso ao hardware bem resolvido, e novos serviços causavam pouca perturbação neste ambiente.

![Estrutura de armazenamento de massa](/media/sistemas_operacionais/estrutura-armazenamento-massa.png)

Chamamos stand alone, ou stand-alone (literalmente "ficam em pé por si só") os sistema que rodam de forma isolada, sem interagir com outros computadores.

Nas redes de computadores, um sistema de comunicação interliga os equipamentos terminais (estações de trabalho).

Do ponto de vista do hardware dos computadores, a modificação foi a introdução de um dispositivo de entrada e saída responsável pela interface do computador com o sistema de comunicação: a placa de interface de rede. Até este ponto, a modificação não seria grande, apenas mais um tipo de hardware e seus drivers.

A grande dificuldade surge a partir do fato que agora o usuário pode acessar recursos na máquina local ou em outra máquina, dita remota.

Para atender a esta necessidade surgiram os Sistemas Operacionais de Redes (SORs), como extensão dos Sistemas Operacionais Locais (SOLs), complementando-os com o conjunto de funções básicas, e de uso geral, necessárias à operação das estações, de forma a tornar transparentes o uso dos recursos compartilhados.

![Sistemas operacionais de redes](/media/sistemas_operacionais/sistemas-operacionais-redes.png)

## Redirecionador

Os SORs devem atuar para que os usuários utilizem os recursos de outras estações da rede como se estivessem operando localmente.

A solução para estender o SO das estações de rede, sem modificar a operação local, foi a introdução de um módulo redirecionador. Ele funciona interceptando as chamadas das aplicações ao sistema operacional.

**Chamada a recurso local**

![Chamada a recurso local](/media/sistemas_operacionais/chamando-recurso-local.png)

**Chamada a recurso remoto**

![Chamada a recurso remoto](/media/sistemas_operacionais/chamando-recurso-remoto.png)

A interface utilizada pelas aplicações para ter acesso aos recursos permanece inalterada. O que o usuário nota é o surgimento de novos recursos (virtuais) em sua estação.

O redirecionador foi o mecanismo sobre o qual se desenvolveram os Sistemas Operacionais de Rede.

## Arquiteturas peer-to-peer e cliente-servidor

A interface entre as aplicações e o sistema operacional baseia-se em interações solicitação/resposta. A aplicação solicita um serviço, através de uma chamada ao SO que executa o serviço solicitado e responde, informando o status da operação e transferindo os dados resultantes da execução para a aplicação, quando for o caso.

Em uma rede, esta interação denomina-se modelo cliente-servidor e se constitui no modo básico de operação dos SORs.

O modelo funciona da seguinte maneira:

![Exemplo de SORs](/media/sistemas_operacionais/sorc-exemplo.png)

Para este esquema funcionar, os módulos de um SOR, instalados nas estações, podem ser do tipo SORC ou SORS.

**SORC**: É o **módulo cliente** do sistema operacional. Instalado nas **estações clientes**. No módulo cliente, o SOR restringe-se praticamente a fornecer serviços de comunicação de pedidos para o servidor e a entregar as respostas às aplicações.

**SORS**: É o **módulo servidor** do sistema operacional. Instalado nas **estações servidoras**. No módulo servidor, além das funções de comunicação, vários outros serviços são executados. Um desses serviços é o controle do acesso aos recursos compartilhados por vários usuários através da rede, para evitar, por exemplo, que um usuário não autorizado apague arquivos que não lhe pertençam.

### Arquitetura peer-to-peer

Em todas as estações, o sistema operacional de redes possui os dois módulos: SORC e SORS. \*_Todas as estações são clientes e servidoras_

![Arquitetura peer-to-peer](/media/sistemas_operacionais/peer-to-peer.png)

Este é o tipo de arquitetura que encontramos em nossas casas quando realizamos o compartilhamento de recursos na rede. Também é chamada de Rede do Grupo de Trabalho, Rede Par a Par ou Rede Ponto a Ponto.

</br>

### Arquitetura cliente servidor

As estações da rede dividem-se em estações clientes, que só possuem as funções do módulo cliente acopladas ao seu sistema operacional local, e em estações servidoras (possuem as funções do módulo servidor e podem, opcionalmente, possuir, também, as funções do módulo cliente).

Atualmente, é o tipo de arquitetura mais indicado quando se precisa de permissões, controle e integridade. Podemos dizer que, em um lado da “ponta” da rede, está o servidor que fornece os recursos (arquivos, banco de dados, dns etc.) e do outro lado da “ponta” está o cliente que utiliza os recursos do servidor.

Nesta arquitetura, nós temos duas divisões:

**Cliente com servidor dedicado**: O cliente com servidor dedicado é usado, geralmente, quando se utiliza um serviço por vários clientes em tempo integral, e que precise ser seguro e confiável. Nessa arquitetura, as estações servidoras não permitem usuários locais. Elas são integralmente dedicadas ao atendimento de pedidos enviados pelas estações clientes através da rede. Neste tipo de arquitetura, os servidores possuem apenas o módulo servidor.

![Cliente com servidor dedicado](/media/sistemas_operacionais/servidor-dedicado.png)

**Cliente com servidor não dedicado**: Na arquitetura cliente-servidor, com servidor não dedicado, as estações servidoras possuem sistema operacional local, que é estendido por um módulo SOR e um módulo SORC.

O módulo SORC pode ser usado tanto pelo SORS, quanto pelas aplicações dos usuários locais da estação servidora. Assim, os recursos locais das estações servidoras são compartilhados tanto pelos usuários atendidos pelo sistema operacional local (que também podem ter acesso a serviços de outros servidores) quanto pelos usuários remotos que fazem pedidos ao SOR através da rede.

![Cliente com servidor nao dedicado](/media/sistemas_operacionais/servidor-nao-dedicado.png)

## Servidores

### Servidores de arquivos

Têm como funções oferecer a seus clientes:

• os serviços de armazenamento e acesso a informações;
• os serviços de compartilhamentos de discos;
• o controle de unidades de discos ou de outras unidades de armazenamento;
• a aceitação de pedidos de transações das estações clientes e o atendimento utilizando seus dispositivos de armazenamento de massa;
• o gerenciamento de um sistema de arquivos que pode ser utilizado pelo usuário em substituição ou em edição ao sistema de arquivos existente na própria estação.

### Servidores de banco de dados

As aplicações baseadas no acesso a banco de dados podem utilizar um sistema de gerenciamento de banco de dados (SGBD) executado no cliente — que usa um servidor de arquivos para armazenar os arquivos dos bancos de dados ou utiliza um servidor de banco de dados —; o SGBD local primeiramente codifica o pedido do usuário, por exemplo, em uma consulta em SQL (Structured Query Language), com o critério de seleção definido pela aplicação.

Em seguida, envia a consulta para o SGBD servidor. O servidor de banco de dados, ao receber o pedido, processa a consulta lendo todos os registros do banco de dados, localmente, selecionando-os de acordo com o critério definido.

Depois de selecionados os registros relevantes, o SGBD servidor os envia ao SGBD cliente, que os entrega à aplicação.

![Servidores de banco de dados](/media/sistemas_operacionais/servidores-db.png)

### Servidores de impressão

Têm como finalidade gerenciar e oferecer serviços de impressão a seus clientes, possuindo um ou mais tipos de impressores acoplados, adequados à qualidade ou rapidez de uma aplicação em particular.

### Servidor de comunicação

Muitas vezes, é interessante podermos ligar dispositivos sem inteligência às redes, ou mesmo livrar o dispositivo a ser ligado dos procedimentos de acesso à rede. Nos dois casos, é necessária uma estação especial de frente que será responsável pela realização de todos os procedimentos de acesso à rede, bem como da interface com os dispositivos dos usuários, agindo como um concentrador.

As funções realizadas por essa estação especial definem o que chamamos de comunicação.

### Servidores de gerenciamento de rede

O monitoramento do tráfego, da disponibilidade e do desempenho de uma estação da rede, assim como o monitoramento do meio de transmissão e de outros indicadores, fazem parte do processo de gerenciamento da rede, de forma a possibilitar a detecção de erros, diagnoses e resoluções de problemas, tais como falhas, diminuição do desempenho etc.

## Os sistemas operacionais de redes e as arquiteturas de redes

Um sistema operacional de rede engloba:

![Sistema operacional de rede ](/media/sistemas_operacionais/sor-engloba.png)

A relação entre os componentes de um sistema operacional de rede e o RM-OSI:

![Relação entre os componentes de um sistema operacional de rede e o RM-OSI](/media/sistemas_operacionais/relacao-componentes.png)

## Placa de interface de rede

A placa de interface de rede (Network Interface Card — NIC) é responsável pela conexão do hardware da estação ao meio físico de transmissão. Na placa de rede estão as funções dos níveis físico e de controle do acesso ao meio (subcamada MAC na arquitetura IEEE 802).

## Drivers de placa de rede

O driver de dispositivo, normalmente fornecido junto com a placa de rede, lida com os aspectos específicos da operação da placa de rede e fornece um conjunto de chamadas mais fáceis de usar e menos dependentes da tecnologia das placas de rede.

## Drivers de protocolo

Contém o código de várias opções de protocolos de comunicação disponíveis na estação; definem a interface usada pelas aplicações distribuídas para intercâmbio de dados.

## TCP/IP

Um driver TCP/IP constitui-se de uma implementação do protocolo de nível de rede IP, e do protocolo de nível de transporte TCP, ambos definidos na arquitetura internet.

# Windows

## Comandos de redes do windows

HOSTNAME: retorna o nome do computador local

IPCONFIG: retorna as configurações da rede local em protocolo TCP/IP e faz a atualização dos protocolos DHCP e DNS

GETMAC: procura pelo endereço MAC e faz a listagem das redes associadas na máquina local ou em toda rede

PATHPING: fusão dos comandos TRACERT e PING, fazendo assim uma identificação em algum problema no routes ou em algum link da rede

NSLOOKUP: retorna informações sobre o DNS de um determinado número IP ou número do host

NETSTAT: retorna as ligações ativas no protocolo TCP

NETSH: dentro deste comando é possível modificar configurações de uma rede local ou em uma máquina remota. Para ver uma lista das suas funções, digite dentro do comando NETSH o comando /?

NET: retorna uma lista completa de opções para ser usada no comando NET

PING: envia pacotes ICMP para um determinado endereço IP e verifica os níveis de conectividade e o tempo de resposta

ROUTE: lista vários parâmetros que junto com o comando route, você tem a possibilidade de modificar entradas na tabela de IP

TRACERT: lista o caminho para um determinado IP e o tempo que irá levar a cada salto

ARP: resolução dos endereços IP em endereços MAC. Exibe e modifica as tabelas de traduções dos endereços IP em endereços físicos utilizados pelo protocolo de resolução de endereços ARP.

## Windows 2012 Server

![Windows 2012 Server](/media/sistemas_operacionais/windows-server-2012.png)

### Ferramentas

AD DS: O AD DS (Serviços de Domínio Active Directory) é a forma padrão de gerenciamento de rede no Windows Server 2012, ele permite a implantação de controladores de domínio, facilita a auditoria e o controle de autorização de acesso a arquivos, e também a execução de tarefas administrativas tanto localmente como remotamente.

ACTIVE DIRECTORY RIGHTS MANAGEMENT SERVICES (AD RMS): O Active Directory Rights Management Services (AD RMS) é a função de servidor que oferece as ferramentas de gerenciamento e desenvolvimento com as tecnologias de segurança do setor (incluindo a criptografia, os certificados e a autenticação) a fim de ajudar as organizações a criarem soluções confiáveis para proteção de informações.

BITLOCKER: O BitLocker criptografa o disco rígido do computador para fornecer melhor proteção contra roubo de dados ou exposição em computadores e unidades removíveis que sejam perdidos ou roubados.

CLUSTER DE FAILOVER: Os clusters de failover oferecem alta disponibilidade e escalabilidade para várias cargas de trabalho de servidor. Eles incluem armazenamento de compartilhamento de arquivos para aplicativos de servidor como Hyper-V e Microsoft SQL Server e aplicativos de servidor que são executados em servidores físicos ou em máquinas virtuais.

GERENCIADOR DE RECURSOS DE SERVIDOR: O Gerenciador de Recursos de Servidor de Arquivos fornece um conjunto de recursos que permite gerenciar e classificar os dados armazenados em servidores de arquivos.

POLÍTICA DE GRUPO: Política de Grupo é uma infraestrutura que permite a você especificar configurações gerenciadas para usuários e computadores por meio de configurações de Política de Grupo e de Preferências de Política de Grupo.

HYPER-V: A função do Hyper-V permite criar e gerenciar um ambiente virtualizado, usando a tecnologia de virtualização que é integrada no Windows Server 2012. O Hyper-V virtualiza o hardware para proporcionar um ambiente no qual você pode executar vários sistemas operacionais ao mesmo tempo, em um único computador físico, executando cada SO em sua própria máquina virtual.

IPAM (GERENCIAMENTO DE ENDEREÇO IP): O IPAM (Gerenciamento de Endereço IP) oferece funcionalidades de administração e monitoramento altamente personalizáveis para a infraestrutura de endereços IP em uma rede corporativa.

GERENCIADOR DO SERVIDOR: O Gerenciador do Servidor, no Windows Server 2012, permite que os administradores gerenciem o servidor local ou vários servidores remotos que estão executando o Windows Server 2012, o Windows Server 2008 R2, o Windows Server 2008 ou o Windows Server 2003.

WINDOWS POWERSHELL 3.0: O Windows PowerShell 3.0 inclui muitos novos recursos e melhorias na experiência de scripts e automação, como:

• o Fluxo de Trabalho do Windows PowerShell;
• vários novos recursos no ISE do Windows PowerShell para agilizar e facilitar scripts e depuração;
• ajuda atualizável;
• Windows PowerShell Web Access;
• mais de 2.200 novos cmdlets e funções.

PROTOCOLO DHCP: O protocolo DHCP é um padrão IETF (Internet Engineering Task Force) desenvolvido para reduzir o custo indireto de administração e a complexidade de configuração de hosts, em uma rede baseada em TCP/IP, como uma intranet particular.

SERVIÇOS DNS (SISTEMA DE NOMES DE DOMÍNIO): Os serviços DNS (Sistema de Nomes de Domínio), no Windows Server 2012, são usados em redes TCP/IP para nomear computadores e serviços de rede. A nomeação DNS localiza computadores e serviços por meio de nomes amigáveis.

# Linux

O Linux é um Sistema Operacional, assim como o Windows e Mac OS. Sua maior diferença reside no fato de ser um sistema totalmente gratuito, estável, seguro e de código aberto. Você é livre para copiar, modificar, distribuir e instalar o Linux quantas vezes quiser.

Na verdade, o kernel Linux é gratuito. Porém, podem existir distribuições pagas.

Quando falamos Linux, na verdade, queremos dizer GNU/Linux. O “Linux” por si só não é um Sistema Operacional, é apenas um kernel (núcleo).

Um Sistema Operacional Linux consiste na combinação de uma versão do kernel Linux e um conjunto de ferramentas GNU que nos permitem interagir com o kernel.

O kernel Linux foi desenvolvido por Linus Torvalds e hoje é mantido por uma comunidade sob sua supervisão. Já as ferramentas GNU foram desenvolvidas pelo projeto GNU, idealizado por Richard Stallman.

Outro detalhe importante que você precisa saber é que dificilmente alguém usa o GNU/Linux puramente.

## Distribuições de GNU/Linux

Basicamente, uma Distribuição Linux (ou simplesmente distro) é composta do kernel Linux, ferramentas GNU e um conjunto variável de software, dependendo de seus propósitos.

Existem distribuições mantidas por indivíduos, como no caso da Slackware e do seu criador Patrick Volkerding. Outras mantidas por organizações, como no caso das distribuições Red Hat, a SuSE, a Mandriva e o Ubuntu (esta última criada e mantida pela Canonical), bem como distros mantidas por grupos ou comunidades, como o Debian e o Gentoo.

Uma coisa interessante de se saber é que, embora existam várias distribuições, podemos agrupá-las em três grandes famílias cujos pais são:

![Grupos de distribuição GNU/Linux](/media/sistemas_operacionais/grupos-de-distribuicao-linux.png)

Elas estão entre as distribuições mais antigas, e ainda possuem muitos usuários adeptos pelo mundo. Se você aprender a usá-las, ficará bem fácil usar qualquer uma de suas descendentes.

Agora, observe no esquema abaixo as três distribuições tradicionais e alguns de seus principais descendentes.

![Três distribuições tradicionais](/media/sistemas_operacionais/principais-descendentes.png)

### Ubuntu

Ubuntu é uma distribuição baseada no Debian patrocinada pela Canonical Ltd. Diferencia-se do Debian por:

• Ter versões lançadas semestralmente;
• Disponibilizar suporte técnico nos nove meses seguintes ao lançamento de cada versão (as versões LTS – Long Term Support – para desktop e servidor recebem cinco anos de suporte); e
• Sua filosofia em torno de sua concepção.

A proposta do Ubuntu é oferecer um sistema que qualquer pessoa possa utilizar sem dificuldades, independentemente da nacionalidade, nível de conhecimento ou limitações físicas. O sistema deve ser constituído principalmente por Software Livre e ser isento de qualquer taxa.

## Interface gráfica Unity

Um grande diferencial do Ubuntu em relação às outras distribuições de GNU/Linux é a sua interface gráfica Unity.

O Unity foi desenvolvido pela comunidade Ayatana e adaptado pela Canonical Ltd. Sua primeira aparição foi na versão 10.10 para netbooks.

Ele foi desenhado inicialmente para fazer um uso mais eficiente do espaço das telas limitadas dos netbooks. Devido ao seu sucesso, tornou-se padrão na versão 11.04, que ainda incluía o GNOME como opção.

Diferente do GNOME, KDE, XFCE e LXDE, o Unity não inclui aplicações, já que foi feito para usar programas GTK+ já existentes. A partir da versão 11.10 do Ubuntu, o Unity passou a ser a única interface padrão.

## Virtualização

A virtualização consiste na emulação de ambientes isolados, capazes de rodar diferentes sistemas operacionais dentro de uma mesma máquina, aproveitando ao máximo a capacidade do hardware, que muitas vezes fica ociosa em determinados períodos do dia, da semana ou do mês.

Esse aproveitamento é maior devido à possibilidade de fornecer ambientes de execução independentes a diferentes usuários em um mesmo equipamento físico, concomitantemente.

Essa técnica, muito empregada em servidores, ainda tem como vantagem oferecer uma camada de abstração dos verdadeiros recursos de uma máquina, provendo um hardware virtual para cada sistema, tornando-se também uma excelente alternativa para migração de sistemas.

Veja, a seguir, os tipos de virtualização:

### Virtualização de hardware

É a técnica que imita a máquina real. A máquina virtual executa em cima de um sistema operacional e outros sistemas operacionais podem ser executados em cima dela.

O sistema abaixo da máquina pode ser um Monitor de Máquina Virtual ou um sistema operacional real.

Os exemplos de sua utilização são VMware e Virtual Box.

### Virtualização de sistema operacional

É a técnica que cria a simulação de um sistema operacional, mas é implementada em cima de outro sistema.

Serve para resolver, sem muitos outros ganhos significativos, a necessidade de execução de aplicações em sistemas operacionais incompatíveis.

O FreeBsd Jail e o User-mode Linux representam essa categoria.

### Virtualização de linguagens de programação

Com ela, é possível fingir que o computador se comporta diferente, ou seja, com outras instruções.

A máquina virtual é responsável por executar o programa de acordo com esse comportamento fictício, do jeito que o usuário definir. Fica encarregada, portanto, de traduzir essas ações em ações do sistema operacional abaixo.

Java e Smalltalk atuam nesse sentido.

![Virtualização de linguagens de programação](/media/sistemas_operacionais/virtualizacao-linguagens.png)

### Virtualização de serviços internet

A internet é representada através de uma abstração que define níveis que implementam serviços e se comunicam com outros níveis. Isso cria a sensação de isolamento entre as tarefas, de forma que a alteração de uma delas possa não prejudicar as demais. Isso reforça o conceito de “um servidor por serviço”, o que traz alguns incômodos.

As máquinas geram um alto custo que inclui manutenção, energia elétrica, entre outros. Gerenciar diversas máquinas também não é fácil e isso gera ainda mais custos. Além disso, projetar servidores para executarem um único tipo de serviço os torna em grande parte ociosos. A virtualização surge, então, para suavizar esse problema.

Como as máquinas virtuais hóspedes podem executar serviços independentes e isolados, em sistemas operacionais diferentes e na mesma máquina, o desejo de “um servidor por serviço” é mantido. Todos os serviços, porém, são empregados no mesmo hardware, o que aproveita todo o poder dos servidores. Isso é chamado consolidação de servidores e gera interessantes cortes no custo do serviço.

![Virtualização de serviços internet](/media/sistemas_operacionais/vm.png)

## Usuário root

Cada pessoa que utiliza o sistema necessita ter uma conta de usuário. Essa conta indica um nome e a senha que devem ser usados para se conectar no sistema.

Um superusuário ou usuário "root" é aquele que tem acesso irrestrito ao sistema. Que pode efetuar qualquer operação no Linux, como apagar ou modificar arquivos importantes, alterar configuração do sistema etc.

É importante não se conectar como root, a não ser que haja alguma tarefa que só possa ser feita dessa maneira. A senha do root deve ser muito bem guardada, pois alguém, se a descobrir, poderá destruir o sistema.

Portanto, para usar o Linux no dia a dia, conecte-se com uma conta de usuário comum. Dessa forma, haverá menor risco de danos.

### Modo usuário

Indica quem está usando a máquina:

`$` - modo usuário

`#` - modo superusuário

## Terminal

O aplicativo terminal serve para entrar com comandos de administração do sistema, instalar programas e pacotes e outras atividades.

Nos dias atuais, a administração dos sistemas operacionais baseados em Unix está cada vez mais longe do terminal. Isso porque a cada dia que passa, novas facilidades vão sendo incorporadas aos sistemas através da interface gráfica. Entretanto, algumas vezes teremos de recorrer ao uso do terminal, mas não se preocupe e não tenha medo dele.

## Sudo: quem é e o que faz?

O usuário comum do LINUX pode acessar a internet, escrever e-mails, digitar textos e mexer nas suas fotos. Entretanto, por si só não tem autonomia para fazer modificações no sistema, como deletar pastas do sistema ou instalar pacotes de programas.

Para fazer essas tarefas, terá que se identificar para o Ubuntu como superusuário através do comando sudo + o que você quer.

Para continuar com a tarefa que você quer que o sistema realize como sudo, o Ubuntu irá lhe solicitar uma senha (autenticação de usuário), que normalmente é criada na instalação do sistema. Só, então, ele começará a realizar a tarefa que você pediu.

## Comandos básicos de terminal

### Comandos de arquivos e diretórios

`cd diretorio` - abre um diretório.

Por exemplo, para abrir a pasta /mnt, basta digitar `cd /mnt`.

Para ir ao diretório raiz a partir de qualquer outro, digite apenas `cd`.

Para este comando existem abreviações, tais como:

`.` (ponto) => Diretório atual
`..` (dois pontos) => Diretório anterior
`~` (til) => Diretório HOME do utilizador
`/` (barra) => Diretório Raiz
`-` (hífen) => Último diretório
`ls [-al]` => listagem do diretório
`cp [-ir]` => copiar arquivos
`mv [-i]` => mover ou renomear arquivos
`rm [--]` => deletar arquivos
`mkdir/rmdir` => cria/deleta diretórios
`ln -s path link` => cria links simbólicos (symlinks) para arquivos ou diretórios
`pwd` => exibe o nome do diretório atual
`tar` => armazena e extrai arquivos de um arquivo tar
`type` => exibe o tipo de um arquivo
`unzip arquivo.zip` => descompacta arquivos zipados

### Comandos de permissões

As permissões dos arquivos são definidas através dos comandos **chmod, chown e chgrp**.

Estrutura do comando: `chmod`

Ao listar as informações de um arquivo ou diretório, o formato é o seguinte: `drwxrwxrwx`

Respectivamente: Diretório (d), permissão do dono (read/write/execute), do grupo (read/write/execute) e de outros (read/write/execute).

Por exemplo, para transformar um arquivo em executável:

`chmod +x nome_do_arquivo` (executável para todos)
`chmod g+x nome_do_arquivo` (executável para o grupo)

Para alterar o usuário e o grupo de um arquivo ou diretório: `chown root.root /sbin/firewall.sh` (-R: recursivamente)

Outros exemplos:
`chmod 755` (executável): -rwxr-xr-x
`chmod 4700` (suid) set user id

Para programas que precisam rodar com permissão de root: `-rws------`

Para calcular o valor numérico das permissões, basta considerar o valor do **executável como 1**, de **escrita como 2** e de **leitura como 4**, que seria o equivalente decimal aos bits:

`rwx` = 111 (todos bits ligados) = 2**2 + 2**1 + 2\*\*0 = 7

Dessa forma, uma permissão de leitura e escrita (4+2) para o owner e de leitura apenas para os outros teria o valor 644.

Para calcular a **umask**, que seria a máscara de permissão aplicada na criação de um novo arquivo, basta então subtrair 666 (ou 777 para diretórios), resultando em umask 022.

### Comandos de usuário

`w`: informações gerais sobre usuários logados e seus processos

`who`: informações dos usuários atuais (do utmp)

`last`: listagem do histórico de logins (/var/log/wtmp)

`lastlog`: retorna informações sobre últimos logins

`passwd nome_do_usuário`: cria ou modifica a senha do usuário

`su`: passa para o superusuário (o prompt $ será substituído pelo #)

`sudo`: executa um comando, usando os privilégios de outro usuário

`useradd nome_do_novo_usuário`: cria uma nova conta usuário

`userdel -r nome_do_usuário`: remove usuário e seus respectivos arquivos do sistema

`usermod`: modifica uma conta de usuário do sistema

`users`: mostra os usuários que estão atualmente conectados ao sistema

### Comandos de sistema

`df –h`: espaço livre e ocupado nos discos

`du -sh(x)`: espaço ocupado pelo diretório e seus subdiretórios

`ps`: exibe informações sobre os processos em execução

`shutdown`: desliga o sistema

`shutdown -r now`: reinicia o sistema

### Rede

Listando processos listening na porta 80 e seus PIDs.

`lsof -n -i:80`: -i4: ipv4 e -n: sem resolver hostnames

`fuser -v 80/tcp`: lista processos que escutam na porta tcp 80 em modo ps-like

`netconfig`: configurações de rede

**Mais comandos em linux**:

http://www.comandoslinux.com/

http://www.devin.com.br/comandos_linux/

https://pt.wikipedia.org/wiki/Utilit%C3%A1rios_Unix

## Comando Route

Manipula a tabela de rotas do kernel. Seu uso primário é para adicionar ou apagar rotas estáticas para as máquinas ou redes específicas. Se for usado sem nenhuma opção, ele exibe a tabela de rotas.
