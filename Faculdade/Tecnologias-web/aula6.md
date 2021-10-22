# Aula 6 - Tabelas

## A construção

A construção de tabelas não é complicada.

O que é mais desafiador é a construção de layouts utilizando-a.

Hoje, é muito comum utilizarmos editores Web que apresentam o recurso da construção visual de tabelas. Este tipo de recurso poupa-nos tempo, porém o refinamento manual ainda é a melhor alternativa.

## TAG: <TABLE>

Para definirmos uma tabela em HTML devemos utilizar a tag <table>.

Seu navegador quando encontra esta tag procura por informações de linhas <tr> células <td>, em uma tradução livre dados de tabela.

Repare o atributo border na tag <table>. Ele define a espessura da linha da tabela. Para omitirmos as marcas de linhas nas tabelas, utilize o border=“0”.

## Cabeçalhos nas colunas

Outro recurso interessante é o uso de cabeçalhos nas colunas das células.

Para identificar de maneira diferenciada a informação dos cabeçalhos, a tag <th> coloca o texto nela contido em negrito.

Outra dica importante: não se esqueça de fechar esta tag.

Caso você deseje apresentar o conteúdo de algumas células, não todas, basta fechar a tag <td> sem conteúdo.
