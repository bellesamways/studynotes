# Aula 9 – Windows

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
