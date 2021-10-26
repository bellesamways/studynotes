# Aula 10 – Folhas de estilo em cascata – Layout

## Blocos e elementos alinhados

Com o surgimento do CSS, pode-se elaborar layouts extremamente complexos utilizando recursos de blocos ou alinhando elementos.

**Bloco de elementos**: `<div>` - define um bloco para dividir os elementos na página. Essa tag sinaliza uma divisão lógica na página. Ela é utilizada para trechos em bloco.

**Elementos alinhados**: `<span>` - alinha os elementos. Essa tag informa ao navegador a, simplesmente, aplicar o estilo no que está entre suas tags. Utiliza-se <span> quando se quer mudar o estilo dos elementos sem ter que colocá-los em um novo bloco dentro do documento. Ela é utilizada para configurações em trechos de parágrafos.

## Layouts

Você já possui todos os elementos para criar páginas Web de forma prática utilizando Folhas de Estilo em Cascata.

Exemplo 1 - Layout com 2 colunas, topo e rodapé.

```html

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">

<html>

    <head>
        <meta http-equiv="Content-Type" content="text/html; charset=iso-8859-1">

        <title>Exemplo</title>

        <style type="text/css">

            #bloco {

                width: 90%;

                margin: 10px auto;

                background-color: #fff;

                color: #333;

                border: 1px solid gray;

                line-height: 130%;

            }



            #topo {

                padding: .5em;

                background-color: #0000a0;

                border-bottom: 1px solid gray;

            }



            #topo h1 {

                padding: 0;

                margin: 0;

                color: #F5F5F5;

            }



            #coluna_esquerda {

                float: left;

                width: 160px;

                margin: 0;

                padding: 1em;

            }



            #conteudo {

                margin-left: 200px;

                border-left: 1px solid gray;

                padding: 1em;

                max-width: 36em;

            }



            #rodape {

                clear: both;

                margin: 0;

                padding: .5em;

                color: #333;

                background-color: #ddd;

                border-top: 1px solid gray;

            }



            h3 {

                font-weight: bold;

                color: blue;

            }



            #coluna_esquerda {

                margin: 0 0 1em 0;

            }



            #conteudo h2 {

                margin: 0 0 .5em 0;

            }



        </style>

    </head>

    <body>

        <div id="bloco">

            <div id="topo">

                <h1>Cursos</h1>

            </div>

            <div id="coluna_esquerda">

                <p>

                    A Estácio Interativa oferece diferentes possibilidades para quem quer estudar utilizando as novas tecnologias de informação disponíveis para aprendizagem: cursos que privilegiam aulas ao vivo, transmitidas via satélite, e aulas on-line, que oferecem o conteúdo via internet. Em ambos os casos, você conta com flexibilidade para acessar os conteúdos e as aulas.

                </p>

            </div>

            <div id="conteudo">

            <h2>Cursos a Distância</h2>

            <h3>

                <p>

                    Gestão da Tecnologia da Informação

                </p>

            </h3>

            <p>

                O curso habilita o aluno para que atue em organizações de qualquer setor (público ou privado), indústria, comércio e empresas que utilizam as tecnologias da informação e comunicação como diferencial estratégico para suas operações e decisões. Além disso, o gestor da tecnologia da informação é um profissional apto a prestar assessoria e consultoria nas diversas áreas das organizações.

            </p>

            <h3>

                <p>

                    Análise e Desenvolvimento de Sistemas

                </p>

            </h3>

            <p>

                O profissional da área de Análise e Desenvolvimento de Sistemas administra e mantém softwares que apóiam o funcionamento de uma organização. Possui conhecimento para a criação de projetos de automação de processos administrativos e para a gestão do desenvolvimento de sistemas. Também aprende as técnicas para documentar, testar e implantar os sistemas de informação como também para usar ferramentas metodológicas de garantia de qualidade em sistemas de informação.

            </p>

            <h3>

                <p>

                    Sistemas de Informação

                </p>

            </h3>

            </p>

            O Bacharel em Sistemas de Informação estará apto a atuar com inovação, planejamento e gerenciamento da informação e da infra-estrutura de tecnologia da informação alinhados às estratégias organizacionais como também com o desenvolvimento e evolução de sistemas de informação e da infra-estrutura de informação e comunicação, ambos aplicados aos processos organizacionais.

        </p>

        </div>

        <div id="rodape">

            UNESA

        </div>

    </div>

    </body>

</html>

```

Exemplo 2 - Layout com 2 colunas, topo e rodapé.

```html

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">

<html>

    <head>

        <meta http-equiv="Content-Type" content="text/html; charset=iso-8859-1">

        <title>Exemplo</title>

        <style type="text/css">

        body {

        font-family:Verdana, Geneva, Arial, Helvetica, sans-serif;

font-size:12px;

        }

            #bloco {

                width: 90%;

                margin: 10px auto;

                background-color: #fff;

                color: #333;

                border: 1px solid gray;

                line-height: 130%;

            }



            #topo {

                padding: .5em;

                background-color: #0000a0;

                border-bottom: 1px solid gray;

            }



            #topo h1 {

                padding: 0;

                margin: 0;

                color: #F5F5F5;

            }



            #coluna_esquerda {

                float: left;

                width: 160px;

                margin: 0;

                padding: 1em;

            }

            #coluna_direita

{

float: right;

width: 160px;

margin: 0;

padding: 1em;

}

            #conteudo {

                margin-left: 200px;

                border-left: 1px solid gray;

                padding: 1em;

                max-width: 36em;

            }



            #rodape {

                clear: both;

                margin: 0;

                padding: .5em;

                color: #333;

                background-color: #ddd;

                border-top: 1px solid gray;

            }



            h3 {

                font-weight: bold;

                color: blue;

            }



            #coluna_esquerda {

                margin: 0 0 1em 0;

            }

#coluna_direita {

                margin: 0 0 1em 0;

            }



            #conteudo h2 {

                margin: 0 0 .5em 0;

            }



        </style>

    </head>

    <body>

        <div id="bloco">

            <div id="topo">

                <h1>Cursos</h1>

            </div>

            <div id="coluna_esquerda">

                <p>

                    A Estácio Interativa oferece diferentes possibilidades para quem quer estudar utilizando as novas tecnologias de informação disponíveis para aprendizagem: cursos que privilegiam aulas ao vivo, transmitidas via satélite, e aulas on-line, que oferecem o conteúdo via internet. Em ambos os casos, você conta com flexibilidade para acessar os conteúdos e as aulas.

                </p>

            </div>

<div id="coluna_direita">

<p>

Inscreva-se <a href="">Já</a>

</p>

</div>

            <div id="conteudo">

            <h2>Cursos a Distância</h2>

            <h3>

                <p>

                    Gestão da Tecnologia da Informação

                </p>

            </h3>

            <p>

                O curso habilita o aluno para que atue em organizações de qualquer setor (público ou privado), indústria, comércio e empresas que utilizam as tecnologias da informação e comunicação como diferencial estratégico para suas operações e decisões. Além disso, o gestor da tecnologia da informação é um profissional apto a prestar assessoria e consultoria nas diversas áreas das organizações.

            </p>

            <h3>

                <p>

                    Análise e Desenvolvimento de Sistemas

                </p>

            </h3>

            <p>

                O profissional da área de Análise e Desenvolvimento de Sistemas administra e mantém softwares que apóiam o funcionamento de uma organização. Possui conhecimento para a criação de projetos de automação de processos administrativos e para a gestão do desenvolvimento de sistemas. Também aprende as técnicas para documentar, testar e implantar os sistemas de informação como também para usar ferramentas metodológicas de garantia de qualidade em sistemas de informação.

            </p>

            <h3>

                <p>

                    Sistemas de Informação

                </p>

            </h3>

            </p>

            O Bacharel em Sistemas de Informação estará apto a atuar com inovação, planejamento e gerenciamento da informação e da infra-estrutura de tecnologia da informação alinhados às estratégias organizacionais como também com o desenvolvimento e evolução de sistemas de informação e da infra-estrutura de informação e comunicação, ambos aplicados aos processos organizacionais.

        </p>

</div>





        <div id="rodape">

            UNESA

        </div>

    </div>

    </body>

</html>

```

Exemplo 3 - Layout 3 colunas, além do topo e rodapé, sendo que este com links de navegação.

```html

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">

<html>

<head>

<meta http-equiv="content-type" conteudo="text/html; charset=iso-8859-1">

<title>Exemplo</title>

<style type="text/css" media="screen">



.botao_proximo a:link, .botao_proximo:visited

{

display: block;

padding: .2em .5em;

background-color: #03F;

color: #fff;

border: 1px solid #006;

width: 11em;

text-decoration: none;

text-align: center;

}



.botao_proximo a:hover, .botao_proximo a:active

{

background-color: #fff;

color: #006;

}



body

{

margin: 0;

padding: 0;

font-size: 12px;

font-family: georgia, times, "times new roman", serif;

color: #000;

background-color: #fff;

}



a:link { color: #036; }

a:visited { color: #066; }



a:hover, a:active

{

color: #fff;

background-color: #036;

}



div#logo

{

color: #fff;

background-color: #333;

border-bottom: 1px solid #000;

}



div#logo h1

{

margin: 0;

padding: .3em 0 .3em .5em;

font-size: 2.2em;

font-weight: normal;

}



div#conteudo

{

background-image: url(nav_col_base.jpg);

background-repeat: repeat-y;

}



div#bloco2

{

background-image: url(more_col_base.jpg);

background-repeat: repeat-y;

background-position: right;

}



div#navegacao

{

float: left;

width: 150px;

padding-top: 2em;

}



div#navegacao ul

{

list-style-type: none;

padding: 0;

margin: 0;

}



div#navegacao ul li { margin-top: 4px; }



#navegacao ul li a

{

display: block;

width: 135px;

padding: 3px 5px 3px 10px;

text-decoration: none;

color: #000;

background-image: url(nav_base.jpg);

background-repeat: repeat-y;

}



#navegacao ul li a:hover

{

color: #fff;

background-color: #ccc;

background-image: url(nav_base2.jpg);

background-repeat: repeat-y;

}



div#mais

{

float: right;

width: 160px;

margin: 0;

padding: 2em 10px 0 0;

color: #000000;

}



div#mais h3

{

margin-top: 0;

color: #fff;

padding: .2em;

background-image: url(mais.jpg);

background-position: right;

background-repeat: repeat-y;

}



div#conteudo

{

margin-left: 190px;

margin-right: 200px;

}



div#conteudo h2

{

font-size: 18px;

color: #036;

margin: 0;

padding-top: 1em;

font-weight: bold;

}



div#conteudo { line-height: 150%; }



#limpa_div

{

clear: both;

height: 1em;

}



div#rodape

{

clear: both;

padding: .5em 1em;

border-top: 1px solid #999;

text-align: right;

}



div#rodape ul

{

padding: 0;

margin: 0;

list-style-type: none;

}



div#rodape li

{

display: inline;

margin-right: 1em;

}

</style>



</head>

<body>

    <div id="logo">

        <h1>Estácio de Sá</h1>

    </div>

    <div id="bloco">


    <div id="bloco2">


    <div id="navegacao">
        <ul>
            <li><a href="#">Graduação</a></li>

            <li><a href="#">Graduação a Distância</a></li>

            <li><a href="#">Pós-graduação</a></li>
        </ul>
    </div>



    <div id="mais">

        <h3>Maiores Informações</h3>

        <p>Inscreva-se <a href="">Já</a></p>

    </div>



    <div id="conteudo">

        <h2>Cursos</h2>

        <h3>
            <p>
                Gestão da Tecnologia da Informação
            </p>

        </h3>

            <p>

                O curso habilita o aluno para que atue em organizações de qualquer setor (público ou privado), indústria, comércio e empresas que utilizam as                     tecnologias da informação e comunicação como diferencial estratégico para suas operações e decisões. Além disso, o gestor da tecnologia da                         informação é um profissional apto a prestar assessoria e consultoria nas diversas áreas das organizações.

            </p>

            <h3>

                <p>

                    Análise e Desenvolvimento de Sistemas

                </p>

            </h3>

            <p>
                O profissional da área de Análise e Desenvolvimento de Sistemas administra e mantém softwares que apóiam o funcionamento de uma organização.                       Possui conhecimento para a criação de projetos de automação de processos administrativos e para a gestão do desenvolvimento de sistemas. Também                   aprende as técnicas para documentar, testar e implantar os sistemas de informação como também para usar ferramentas metodológicas de garantia de                   qualidade em sistemas de informação.
            </p>

            <h3>

                <p>

                    Sistemas de Informação

                </p>

            </h3>

            <p>

            O Bacharel em Sistemas de Informação estará apto a atuar com inovação, planejamento e gerenciamento da informação e da infra-estrutura de tecnologia               da informação alinhados às estratégias organizacionais como também com o desenvolvimento e evolução de sistemas de informação e da infra-estrutura de             informação e comunicação, ambos aplicados aos processos organizacionais.

            </p>



            <p class="botao_proximo"><a href="JavaScript:history.back()">Retorna</a></p>

    </div>



    <div id="limpa_div"></div>



    </div>

    </div>



    <div id="rodape">

        <ul>

            <li><a href="#">A Empresa</a></li>

            <li><a href="#">Trabalhe Conosco</a></li>

            <li><a href="#">Estatísticas</a></li>

            <li><a href="#">Copyright &copy; Universidade Estacio de Sá</a></li>

        </ul>

    </div>


</body>

</html>

```
