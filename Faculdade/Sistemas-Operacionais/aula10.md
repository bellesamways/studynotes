# Aula 10 - Linux

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
