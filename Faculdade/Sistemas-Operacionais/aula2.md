# Aula 2 - Processos

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
