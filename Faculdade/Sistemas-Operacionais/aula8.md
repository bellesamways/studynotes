# Aula 8 – Sistemas Operacionais em Redes

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
