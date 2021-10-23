# Aula 5 - Gerência de entrada e saída

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
