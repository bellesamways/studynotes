# Aula 5 - Introdução a HTML

## HTML

A grande reviravolta na Internet aconteceu quando, em 1989, Tim Berbers-Lee desenvolveu uma linguagem capaz de publicar e organizar conteúdos na Internet. Nascia, aí, a linguagem **HTML (Hypertext Markup Language)** que permitiria aos pesquisadores do laboratório CERN publicarem suas informações de maneira rápida, padronizada e fácil. Esta facilidade ganhou atenção mundial e tornou-se o maior hit da Internet até hoje. Já são milhões de sites e aplicações baseadas nesta linguagem que vem explorando, a cada dia, mais e mais recursos, trazendo inovação e informação para qualquer pessoa em qualquer parte do mundo onde haja uma conexão com a Internet.

As 3 principais facilidades da linguagem HTML são:

Princípio da não linearidade da informação, permitindo ao usuário navegar pelas informações utilizando o princípio do hipertexto.

Permite a formatação do texto, utilizando marcações para estilizá-lo, podendo ser interpretável por todo e qualquer navegador Web desde que sejam respeitadas as marcações padrão do W3C.

Flexibilidade de uso. Esta linguagem permite fácil adequação aos mais diferentes propósitos.

## Estrutura

Todos os documentos HTML são chamados de páginas e contém elementos dentro de padrões estruturais. Cada elemento é chamado de tag. Sua sintaxe permite, ainda, a definição de parâmetros o que foi fundamental para o avanço da linguagem.

Cada elemento, quando utilizado, pode trabalhar em par com a abertura e o fechamento desta tag. Neste caso, fecha-se a tag utilizando o caracter \ dentro dos sinais de <> da mesma.

Sintaxe:

**<tag> </tag>** - abertura e fechamento ou para tags sem elementos adicionais **<tag>**

Uma tag é formada por:

comandos

atributos: modificam os resultados da mesma

valores: caracterizam essa mudança

Toda as tags devem ser descritas dentro da estrutura maior de uma página HTML, que nada mais é que um arquivo texto, cujos elementos estruturais são também descritos por tags como, por exemplo:

<HTML><BODY></BODY></HTML>

Cada comando tem seus atributos possíveis e seus valores. Um exemplo é o atributo **size** que pode ser usado com o comando FONT, com o HR, mas que não pode ser usado com o comando BODY.

De uma maneira geral, o HTML é um poderoso recurso, sendo uma linguagem de marcação muito simples e acessível, voltada para a produção e compartilhamento de documentos e imagens.

## Documento HTML

Os documentos em HTML são arquivos de texto simples que podem ser criados e editados em qualquer editor de textos comum. Você poderá salvá- lo com a extensão html ou htm.

As tags básicas de HTML que você normalmente encontrará nas páginas da Internet são:

<HTML>: Esta tag irá definir o início de um documento HTML ao navegador web.

<HEAD>: Nesta tag estão as definições de cabeçalho do documento. Podem ser postos aqui: chamadas Javascript, CSS, tags META entre outras.

<BODY>: Em um documento HTML faz-se necessário indicar o corpo do documento. A partir desta tag até o fechamento da mesma, todos os elementos aqui descritos serão apresentados como conteúdos na página em seu navegador.

## Comandos em HTML

Dentro do cabeçalho de um documento em HTML podemos encontrar os seguintes comandos:

<TITLE>: O conteúdo definido dentro desta tag será exibido na barra de título do seu navegador.

<STYLE>: Quando trabalharmos com Folhas de Estilos, definimos aqui os estilos carregados. 

<SCRIPT>: Utilizada para definir a carga de um script do tipo Javascript, por exemplo, do lado do cliente. 

<LINK>: Utilizada para definir ligações entre a página e arquivos externos como, por exemplo, arquivo de folhas de estilos. XHTML esta tag deve ser obrigatoriamente fechada. 

<META>: Esta tag é uma das mais utilizadas para dar aos robôs de busca informações a respeito de sua página e site. Ela define as propriedades da página. Desta forma, ferramentas de indexação de conteúdos podem, ao ler as informações contidas nestas tags, catalogar sites e suas informações, tais  como descrição da página,autor,palavras chave, etc. O atributo content é obrigatório, pois especifica o conteúdo da meta informação. Os demais atributos são opcionais.  

 

 

## Tags para web 

 
 

Algumas tags são importantes para o desenvolvimento da página Web  como, por exemplo, as tags de corpo, quebra de linhas e centralizações de elementos. 

 
 

### Tags de Corpo 

 
 

**Comentários**: Tag: <!- - > 

 
 

Esta tag é utilizada para aplicar comentários ao código HTML. Não se esqueça que ela deve ser fechada por dois sinais de menos e um sinal de maior para limitar o tamanho do comentário. Caso contrário, todo o conteúdo ficará escondido do usuário. 

 
 

**Âncora**: Tag: <a> 

 
 

Esta tag define uma âncora dentro ou fora da página. Através dela, é possível fazer uma ligação com outro documento ou ainda saltar para um ponto específico do documento sem a necessidade da ação de paginação feita pelo usuário. 

 

 

### Caracteres e seus Controles 

 
 

**Negrito Tag**: <b> 

 
 

Através desta tag, podemos indicar ao navegador que negrite o texto. 

 

 

**Itálico Tag**: <i> 

 
 

Para aplicar o efeito itálico no caracter, basta utilizar a tag <i>, não se esquecendo de fechá-la, pois, caso isto não ocorra, todos os elementos textuais ganharão este estilo. 

 
 

**Tag**: <big> 

 
 

Esta tag enfatiza o conjunto de caracteres ligados a ela não só aumentando seu tamanho em letra como também a espessura do corpo de letra. 

 
 

**Tag**: <em> 

 
 

Outra forma de enfatizar o texto. A diferença é que, neste caso, o texto ficará em itálico. 

 
 

**Tag**: <strong> 

 
 

Esta tag é semelhante a tag <b>. 

 
 

**Tag**:<small> 

 
 

Publica o texto de forma diminuta.  

 
 

Em HTML, esta tag faz com que o texto seja apresentado em uma fonte pequena e estreita. 

 
 

**Tag**: <strike> 

 
 

Esta tag é utilizada quando queremos apresentar um texto todo ele riscado na horizontal. 

 
 

É como se tudo aquilo que estivesse escrito fosse eliminado, porém desejamos que fosse visto. 

 
 

**A tag <strike> foi descontinuado no HTML 4.0.1 e não é suportada pelo DTD Strict do XHTML 1.0** 

 

 

**Tag**: <font> 

 
 

O HTML é rico em recursos e nos permite definir as características das fontes a serem apresentadas no navegador Web do usuário. Existem muitas fontes a serem utilizadas. Tenha cuidado, pois nem todas estão disponíveis nas máquinas dos usuários na Internet. Prefira fontes mais conhecidas, tais como Arial, Helvetica, Times New Roman, Verdana e Courier New. Elas estão disponíveis na maioria dos ambientes gráficos dos sistemas operacionais Gnu/Linux, MacOS e Windows. **O elemento font foi descontinuado no HTML 4.0.1 e não é suportado pelo DTD do Strict do XHTML 1.0**. 

 

 

### Controle de Caracteres 

 
 

**Quebra de linha**:  

 
 

<br> 

 
 

Quando desejarmos quebrar uma linha, tal como fazemos em nosso editor de texto, basta utilizar a tag <br>.  

 

 

<p> 

 
 

Já esta tag representa um salto maior. Ela simboliza a quebra de parágrafo feita no editor de textos. 

 
 

**Centralização de Elementos**: <center> 

 
 

Para centralizarmos um texto ou elemento na tela do seu navegador, basta utilizarmos a tag <center>. Ela permite a centralização de forma independente da resolução gráfica apresentada em seu monitor. 

 
 

## Tags para web - listas 

 
 

Ao utilizarmos uma lista, precisamos definir seu começo e fim e seus itens. Para isso, deveremos trabalhar com algumas tags em bloco, tais como <dd>,<dl> e <dt>. 

 
 

### Tags: <dl>, <dd>, <dt> 

 
 

Quando necessitamos elencar itens em uma lista.  

 
 

Esta tag deve ser utilizada juntamente com a tag <dl> e <dt>.   

 
 

Exemplo: 

```html 

<dl> 

 <dt>Graduação em Análise de Sistemas</dt> 

   <dd><a href="http://www.estacio.br/curso1.html">Confira</a></dd> 

 <dt>Graduação em Desenvolvimento Web</dt> 

   <dd><a href="http://www.estacio.br/curso2.html">Confira</a></dd> 

</dl> 

``` 

 
 

### Listas ordenadas 

 
 

Tag: <ol> 

  

Para a apresentação de itens ordenados utilizando marcadores numéricos, você deve utilizar a tag <ol> para apresentar uma lista ordenada. Cada item da lista deve ser indicado pela tag <li>, traduzido livremente para lista de itens. 

 
 

```html 

<p>Lista Ordenada:</p> 

<ol> 

 <li>Gás</li> 

 <li>Luz</li> 

 <li>Telefone</li> 

</ol> 

``` 

 
 

### Listas não ordenadas 

 
 

Tag: <ul> 

 
 

A lista não ordenada somente apresenta marcadores junto ao item. 

Não há como verificar ordenação dos dados. 

 
 

```html 

<p>Lista Não Ordenada:</p> 

<ul> 

 <li>Gás</li> 

 <li>Luz</li> 

 <li>Telefone</li> 

</ul> 

``` 

 
 

Tag: <option> 

 
 

Existe uma maneira interessante de se exibir uma lista não ordenada economizando bastante espaço na tela. Para isso, devemos utilizar a tag <option>, comumente empregada em formulários cujo objetivo é armazenar grandes listas e poupar espaço na apresentação no navegador do usuário. 

 
 

## Embarcando objeto em sua página (Tag: <embed>) 

 
 

A tag <embed> permite que você acople objetos externos a sua página como um plug-in. Hoje temos vários sites que oferecem seus objetos codificados nesta tag. Temos o Youtube, Google Video entre outros. 

 
 

Atributos: 

height – altura  em pixels do objeto 

src – origem do objeto 

type – tipo do objeto 

width – largura em pixels 

 
 

## CABEÇALHOS (Tag: <h1>,<h2>,<h3>,<h4>,<h5>,<h6>) 

 
 

As tags de h1-h6 foram muito utilizadas no passado para dar ênfase ao tamanho dos textos utilizados em cabeçalhos. O valor 1 indica o maior e o 6 o menor tamanho das letras utilizadas nos cabeçalhos. Para um melhor entendimento, pense que o cabeçalho se assemelha ao Estilo utilizado pelos editores de texto. Eles não só alteram o tamanho como a aparência da letra, grifando-a. 

 
 

## Outras tags 

 
 

### LINHA HORIZONTAL 

 
 

Tag: <hr>  

 
 

Em HTML é fácil criarmos uma linha horizontal que ocupe toda a extensão da página sem nos preocuparmos com a definição do tamanho. 

 
 

Basta que usemos a tag <hr>, que em uma tradução livre significa linha horizontal. 

 
 

Este recurso facilita a divisão visual de elementos no corpo da página.  

 
 

### Imagem 

 
 

Tag: <img> 

 
 

Esta tag possui os atributos src, onde indicaremos a fonte da imagem, o atributo alt, que facilita a identificação com um texto alternativo no caso da não visualização da mesma. 

 
 

### MAP 

 
 

Tag: <map> 

 
 

Esta tag é utilizada para criarmos regiões clicáveis em uma imagem do lado do cliente. Através dela, podemos mapear pontos sensíveis de uma imagem que redirecionam o usuário de acordo com o contexto clicado dentro da imagem. 

 
 

Atributos: 

name  - nome do mapa 

area  - define uma área clicável 

shape – define o formato da região clicável 

coords – define as coordenadas x_min, y_min,x_max,y_max 

alt – informação alternativa 

 
 

### Frames 

 
 

Tags: <frameset> e <frame> 

 
 

A tecnologia do frame foi criada com o intuito de dividir a página apresentada ao usuário em segmentos distintos, como se fossem janelas, possibilitando a cada um o carregamento independente do conteúdo a ser apresentado.  Cada frame está contido em um frameset (conjunto de frames) e cada um pode ter atributos diferentes, tais como tamanho, paginação entre outros. Em uma tradução livre, frame que dizer moldura. 

 
 

### Iframes 

 
 

Tag: <iframe> 

 
 

Atributos: 

align  - alinhamento – left, right, top, bottom, middle. Descontinuado 

frameborder – tamanho da borda – 1 e 0 

height –- estabelece a altura do iframe em pixels  

widht – estabelece a largura do iframe em pixels 

longdesc – aponta para um arquivo que contém informações adicionais a respeito daquele iframe 

marginheight – especifica as margens superior e inferior em pixels 

marginwidht – especifica a margem a direita e a esquerda do iframe 

name – nome do iframe 

scrolling – habilita ou não a barra de scroll 

src – indica a URL com o caminho do documento a ser carregado pelo iframe
