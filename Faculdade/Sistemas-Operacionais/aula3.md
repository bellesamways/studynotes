# Aula 3 - Gerência de processador

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
