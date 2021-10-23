# Aula 1 - Fundamentos de sistemas operacionais

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
