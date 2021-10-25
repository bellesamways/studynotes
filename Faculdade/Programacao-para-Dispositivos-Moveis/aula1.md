# Aula 1 - Introdução à computação móvel, a plataformas de desenvolvimento e à programação móvel Android

## Introdução ao Android

Computação móvel é a capacidade de ter acesso à informação, em qualquer lugar e a qualquer hora, onde existe total mobilidade do usuário.

## Dispositivo móvel

Um dispositivo móvel (handheld) é um computador de bolso, normalmente equipado com uma pequena tela (output) e um teclado em miniatura (input). Em alguns dispositivos móveis, o teclado está incorporado à tela, no que chamamos de dispositivo touchscreen, tal como nos tablets.

Existem diversas categorias de dispositivos de computação móvel. Entre os mais comuns estão:

- Smartphone;
- Tablet;
- PDA (Personal Digital Assistant);
- Celular;
- Console portátil;
- Coletor de dados;
- GPS (Global Positioning System).

## Conceito de mobilidade

O conceito base que impulsionou o desenvolvimento dos dispositivos móveis foi a mobilidade, que pode ser definida como: **A capacidade de poder ser movido fisicamente e/ou poder ser utilizado enquanto está em movimento.**

Para isso, os dispositivos móveis possuem determinadas características essenciais:

- Pequenos;
- Leves;
- Capacidade de memória e processamento limitados;
- Baixo consumo de energia;
- Conectividade ou não, ou, ainda, conectividade limitada;
- Inicialização mais rápida;
- Armazenamento de dados local e/ou remoto;
- Sincronização de dados com outros sistemas;

## Aplicativos

Os possíveis tipos de aplicativos são:

1. Nativo:
   - Desenvolvidas especificamente para uma determinada plataforma móvel;
   - Faz uso da linguagem de programação suportada pela plataforma e seu respectivo SDK (software development kit);
   - Normalmente, são instaladas através da loja de aplicativos, como, por exemplo, App Store e Google Play.
2. WebMobile:
   - Diferente das aplicações nativas, consiste em um site com layout otimizado para plataforma móvel;
   - Faz uso de linguagens web (HTML, CSS, Javascript);
   - Pode ser usado por qualquer plataforma móvel.
3. Híbrida:

   - Consiste na combinação dos tipos nativos e WebMobile;
   - Em geral, possui um navegador de internet customizado para o site do aplicativo;
   - É desenvolvido para uma plataforma móvel específica;
   - Tem se destacado nos últimos tempos.

4. Multiplataforma:
   - Faz uso de framework para geração de aplicações móveis.

</br>

## Principais sistemas operacionais de dispositivos móveis

Merecem destaque: IOS, Android, Windows Phone, BlackBerry, Symbian.

É público e notório que o Android tornou-se o sistema operacional mais usado em dispositivos móveis.

### Sistema Operacional Android

Android é um software open-source para dispositivos móveis, baseado no sistema operacional Linux.

Foi desenvolvido por uma empresa chamada Android Inc., situada na Califórnia-EHA, e fundada por Andy Rubin, Rick Miner, Nick Sears e Chris White, inicialmente para o desenvolvimento de aplicativos para celulares.

Em 2005, foi adquirida pela Google, que manteve Andy Rubin como colaborador no desenvolvimento da plataforma Android.

Em novembro de 2007, foi criada a Open Handset Alliance(OHA), formada por várias empresas do setor e capitaneada pela Google. A OHA fortaleceu o crescimento da plataforma Android.

Finalmente, em 2008, foi lançado o primeiro dispositivo móvel, usando o sistema operacional Android, batizado de HTC T-Mobile, cuja imagem é apresentada a seguir.

### Principais características do android

![Principais características do android](/media/programacao-dispositivos-moveis/caracteristicas-android.png)

## Máquina virtual android

Assim como na linguagem Java, a plataforma android possui sua máquina virtual própria, denominada Dalvik Virtual Machine (DVM).

Otimizada para consumir menos memória, ela difere da Java Virtual Machine (JVM) porque os arquivos .class são convertidos para o formato .dex (Dalvik Executable), que corresponde à aplicação Android compilada, e compactados em um arquivo com extensão .apk (Android Package File) que representa a aplicação final.

A partir do Android 4.4, a DVM foi substituída pela Android Runtime (ART) que apresenta um desempenho muito superior em relação à DVM. Umas das principais diferenças entre a DVM e a ART é a forma de compilação.

Na DVM, o processo de compilação é baseado em JIT (Just in time). Como próprio nome diz, somente a parcela do código necessária para execução é compilada naquele momento. É importante lembrar que, devido somente uma parte do código ser compilada, esse processo consome menos memória e menos espaço físico no dispositivo.

Já na ART, ele é totalmente compilado na instalação do aplicativo e isso ocorre somente uma vez. Com isso, o código é muito mais rápido em sua execução porque não precisa ser compilado muitas vezes. Além disso, por demandar menor recursos de CPU, consome menos bateria.

## Plataforma Android

No Android, uma versão do sistema operacional é conhecida como plataforma. (LECHETA, 2015, p. 43)

Cada versão possui um código identificador (número inteiro) denominado API Level, que corresponde à versão da plataforma Android.

É importante ressaltar que o valor da API Level será usado quando forem definidos os dispositivos alvos para seu aplicativo.

## Arquitetura android

A arquitetura do android é agrupada em 3 níveis e é composta de 5 módulos:

1. Linux Kernel;
2. Libraries;
3. Android Runtime;
4. Application framework;
5. Applications.

![Arquitetura android](/media/programacao-dispositivos-moveis/arquitetura-android.png)

### Applications

É nesse módulo que se encontram os aplicativos instalados, como, por exemplo:

- Cliente email;
- Navegador;
- Contatos;
- Mapas;
- Programas para SMS.

### Application framework

Fornece vários serviços para aplicações na forma de classes Java.

Os desenvolvedores de aplicativos têm permissão para fazer uso desses serviços em suas aplicações.

Os principais serviços são:

- Activity Manager - Controla todos os aspectos do ciclo de vida da aplicação e da pilha de atividade;
- Content Provider - Permite que os aplicativos publiquem e partilhem dados com outras aplicações;
- Resource Manager - Fornece acesso a recursos, como Strings, configurações de cores e layouts de interface do usuário;
- Notifications Manager - Permite que os aplicativos exibam alertas e notificações para o usuário;

- View System - Conjunto de views destinado a criar interfaces de usuário.

### Libraries

São as bibliotecas destinadas ao desenvolvimento Android.

Dentre elas, merecem destaque:

- Android.app - Fornece acesso à aplicação;
- Android.content - Facilita o acesso ao conteúdo, publicação e mensagens entre aplicativos e componentes dos aplicativos;
- Android.database - Usado para acessar os dados publicados por provedores de conteúdo e inclui classes de gerenciamento de banco de dados SQLite;
- Android.opengl - Uma interface Java para os gráficos OpenGL;
  Android.os - Fornece acesso aos serviços do sistema operacional padrão, incluindo mensagens, serviços do sistema e comunicação entre processos;

- Android.text - Usado para processar e manipular texto em uma tela do dispositivo;

- Android.view - Construção das interfaces com o usuário do aplicativo;

- Android.widget - Uma rica coleção de componentes de interface do usuário pré-construídos, tais como botões, etiquetas, exibições de lista, gerenciadores de layout, botões de rádio etc.

### Android runtime

Módulo que fornece a Dalvik Virtual Machine, que é uma espécie de Java Virtual Machine, especialmente projetado e otimizado para o Android.

### Linux kernel

É o nível de abstração do hardware do dispositivo que proporciona o gerenciamento de memória, de energia, de processos, de segurança, dentre outros;

Possui drivers essenciais do hardware.

## Componentes de um aplicativo android

Componentes são blocos de construção essenciais a um aplicativo Android.

O arquivo AndroidManifest.xml, que é único em cada aplicação, descreve cada componente da aplicação e como eles interagem.

Nele constam todas as configurações necessárias para executar a aplicação, como, por exemplo, o nome do pacote utilizado, o nome das classes de cada activity, as permissões que o aplicativo possui, qual a versão mínima da API Android, dentre outras configurações.

Os principais componentes que podem ser utilizadas dentro de uma aplicação Android são:

### Activity

É considerado o componente base de uma aplicação Android. Por isso, é o mais utilizado.

Consiste em uma classe gerenciadora de UI (Interface do usuário). Representa uma única tela do usuário.

Tanto o fluxo da aplicação como eventos de tela são de sua responsabilidade. Isso não significa que todo aplicativo precisa ter uma interface do usuário, mas, se tiver, precisará de, pelo menos, uma Activity.

![Componente base de uma aplicação Android](/media/programacao-dispositivos-moveis/componente-base-android.png)

### Intent

Uma Intent (intenção) é uma descrição abstrata de uma operação a ser executada. Ela pode ser utilizada para iniciar uma Activity, “ativar” um broadcast, enviar uma mensagem para uma aplicação que roda em outro processo etc. Uma Intent faz parte da arquitetura do Android e é um conceito básico que deve ser dominado por todos que desejam programar para Android.

Sendo assim, em linguagem mais humana, uma Intent representaria uma "Mensagem”, um pedido que é encaminhado ao sistema operacional. O sistema pegará a mensagem, verificará qual é a “Intenção da mensagem” e tomará uma decisão que pode ser desde abrir uma página na Web (um browser abrirá e a página será exibida), fazer uma chamada telefônica ou iniciar uma Actvity.

### Service

Quando o aplicativo possuir um ciclo de vida mais longo, normalmente colocamos em um Service.

Conhecido por ser um componente de background, responsável pelo processamento em segundo plano associado a uma aplicação.

Geralmente é utilizado para realizar tarefas de sincronização, como, por exemplo, sincronização de dados em segundo plano.

![Exemplo de sincronização](/media/programacao-dispositivos-moveis/exemplo-sincronizacao.png)

### Broadcast receiver

Lidam com a comunicação entre sistema operacional e aplicativos Android. São responsáveis por tratar eventos do sistema ou de outras aplicações.

Se um aplicativo precisar receber e responder a qualquer evento global, precisa registrar-se como um BroadCast Receiver.

![Broadcast receiver](/media/programacao-dispositivos-moveis/registro-broadcast.png)

### Content provider

Responsável pela gestão de dados e banco de dados.

Além de permitir o compartilhamento de dados entre aplicações, centraliza as rotinas de armazenamento e recuperação em um único local, provendo às aplicações dados.

Em outras palavras, podemos afirmar que corresponde a uma abstração de dados para seus clientes.

É importante lembrar que o Content Provider pode acessar qualquer forma de armazenamento de dados existente na plataforma Android, entre eles arquivos, banco de dados SQLite ou até mesmo mapas hash de memória, caso não precise persistir dados.

![Content provider](/media/programacao-dispositivos-moveis/content-provider.png)

### Componentes adicionais

1. Fragments

   - Permitem a modularização da interface do usuário;

   - Representam uma parte da UI em uma atividade;

   - Assim como o activity, possuem seu próprio ciclo de vida e podem ser definidos como fragmento de um tela em um aplicativo android;

   - São uma espécie de "subatividade" que pode ser reutilizada em diferentes atividades.

2. Views
   - Elementos de interface do usuário que são desenhados na tela, como botões, quadros de texto e até mesmo gerenciadores de layouts;
   - São a classe-pai de todos os componentes visuais.
3. Layouts
   - Controlam o formato de tela e a aparência de interface do usuário, sendo possível serem criados com declaração de elementos XML ou através da programação Java.
4. Intents
   - Representam uma ação que a aplicação deseja executar. Isso se dá através de mensagem (Broadcast) enviada ao sistema operacional, que decidirá a realização ou não da ação, a partir do conteúdo dessa mensagem;
   - É importante lembrar que se constituem uma intenção, como próprio nome diz. Não há certeza de que a aplicação será executada.
5. Manifest
   - Arquivo que possui informações essenciais referentes à configuração para execução da aplicação, como, por exemplo, nome do pacote utilizado, nome das classes de cada activity e outros;
   - Deve estar na pasta raiz do projeto.

</br>

## Principais IDEs

A IDE é um ambiente integrado, que acelera o desenvolvimento de aplicativos durante a fase de programação.

1. Android Studio: https://developer.android.com/sdk/index.html

2. IntelliJ: https://www.jetbrains.com/idea/download/

3. Eclipse: https://eclipse.org/downloads/

## Revisão

Os principais componentes da plataforma de desenvolvimento android:

- Activity: é um componente de aplicativo que fornece uma tela com a qual os usuários podem interagir para fazer algo, como discar um número no telefone, tirar uma foto, enviar um e-mail ou ver um mapa. Cada atividade recebe uma janela que exibe a interface do usuário. Geralmente, a janela preenche a tela, mas pode ser menor do que a tela e flutuar sobre outras janelas.

- Intent: é um objeto de mensagem que pode ser usado para solicitar uma ação de outro componente de aplicativo.

- Service: é o componente responsável pelo processamento em segundo plano associado a uma aplicação.

- Broadcast Receiver: são componentes responsáveis por receber e tratar eventos (broadcasts) provenientes do sistema ou de outras aplicações. É sempre executada em segundo plano.

- Content Provider: são componentes responsáveis por prover às aplicações o conteúdo que elas precisam para funcionar, ou seja, os dados. Permitem o compartilhamento de dados entre aplicações, centralizam as rotinas de armazenamento e recuperam em um único local.
