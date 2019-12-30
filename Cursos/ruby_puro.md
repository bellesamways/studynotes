# Ruby Puro

Anotações do curso gratuito: https://onebitcode.com/course/ruby-puro/

Roda várias linguagens https://repl.it/languages/ruby

Instalação:
* [Rbenv](https://github.com/rbenv/rbenv)
* [Rvm](https://github.com/rvm/ubuntu_rvm)
* [Asdf](https://asdf-vm.com/#/core-manage-asdf-vm)
* [Codeanywhere](https://codeanywhere.com/): ruby online

Colocando **irb** e enter, ele executa códigos ruby direto, sem necessidade de criar um arquivo para teste.

* **Integer**: conjunto de números positivos, negativos e 0
* **Float**: são números decimais, números que contêm ponto flutuante
* **Boolean**: possui apenas dois estados, sendo eles true que é uma instância da classe TrueClass e false que é uma instância da classe FalseClass.
* **String**: conjunto de letras, símbolos ou números.
* **Array**: permite armazenar uma lista ordenada de dados em um único objeto.

### Tipos de dados
No ruby não é preciso definir o tipo de dado antes de atribuir um valor à uma variável. O tipo é dinâmico, ou seja, ele é definido de acordo com o dado atribuído. Não existem "tipos primitivos" em Ruby; todos os tipos são classes:


* **Object** é a classe mãe de todas as outras classes em Ruby
* **Numeric** é uma classe abstrata que representa números
* **Integer** é uma classe que representa números inteiros
* **Fixnum** representa números inteiros de precisão fixa
* **Bignum** representa números inteiros de precisão infinita, dependente apenas da memória disponível
* **Float** é uma classe que representa números de ponto flutuante (números reais)
* **String** uma cadeia de caracteres. Pode ser delimitado por apóstrofes (') ou aspas ("). Tudo o que há entre apóstrofes é interpretado literalmente, entre aspas o programador deve se utilizar de símbolos para representar caracteres específicos, como em C. Exemplos: 'azul', "a\nb\nc"
* **Symbol** é semelhante a uma string, mas dois símbolos iguais possuem o mesmo endereço de memória, sendo assim é ótimo para se utilizar como índice numa Hash. Porém, devido à sua natureza, o coletor de lixo do Ruby não os elimina. É definido com um sinal de dois pontos (:), por exemplo, :nome
* **Array** são arrays dinâmicos, que podem ser usados para representar matrizes e vetores. É delimitado por colchetes ([]) e cada valor é separado por vírgula. Exemplo: [4, 'azul', :termometro]
* **Hash** representa um vetor associativo, e, assim como as Arrays, é dinâmica. É delimitada por chaves ({}), e o índice precede o valor com um sinal '=>'. Exemplo: {:controller => 'user', :action => 'index'}. Qualquer objeto pode ser um índice, mas os mais usados são as Strings e os Symbols
* **Regexp** representa expressões regulares, delimitadas por //. Funciona de forma semelhante a Perl. Exemplo: /a|ae/

### Declaração de variáveis
Um objeto em Ruby é declarado com uma atribuição comum:

```Ruby
class Carro
  @@marcas = [ "Ford", "GM", "Fiat", "VW" ]
end
```

* Uma variável **local** é declarada normalmente.
* Uma variável de **instância** é declarada com um "@" no nome.
* Uma variável de **classe** é declarada com "@@".
* Uma variável **global** é declarada com "$".
* Variáveis que iniciam com uma **letra maiúscula** são consideradas **constantes**.

```Ruby
class A
  @@contexto = "classe"


  def initialize
    @contexto = "instância"
  end


  def contexto
    @contexto
  end


  def A.contexto
    @@contexto
  end
end


a = A.new
a.contexto  # >> "instância"
A.contexto  # >> "classe"
```

### Operadores Matemáticos
Para resolver operações matemáticas no ruby contamos com a seguinte lista de operadores aritméticos:
* \+ (Adição)
* \– (Subtração)
* \* (Multiplicação)
* \/ (Divisão)
* \% (Módulo)
* \** (Expoente)

### Entrada/Saída
Essas duas operações manipulam dados, com a diferença que a entrada ocorre quando o programa lê dados que podem ter sido recebidos de um teclado, de um arquivo, ou então de outro programa e a saída é um dado produzido pelo programa que pode ser exibido em uma tela, enviado para um arquivo ou então para outro programa.

**gets** é um método que recebe como entrada um dado inserido pelo teclado. Como ele captura qualquer coisa precisamos do **.chomp** para que quando o enter for pressionado ele não crie uma quebra de linha.

**.to_i** transforma a string em número inteiro

### Condicional
Tipo de estrutura de controle que executa um trecho de código dependendo do resultado de uma condição.
Instruções Condicionais If, Else, Elsif, Unless e Case:

* **If**: Expressão que verifica se uma condição é verdadeira(true), e a partir deste resultado determina se as instruções dentro de seu corpo serão ou não executadas.
* **Else**: Informa o que fazer quando a verificação de uma condição if for falsa.
* **Elsif**: Utilizado quando há a necessidade de verificar mais de uma condição em um if.
* **Unless**: Enquanto o if é executado quando sua condição é verdadeira, o unless ocorre de forma contrária. É executado apenas quando a condição é falsa.
* **Case**: Instrução muito parecida com o if. Ele se enquadra muito bem a situações com diversas condições.

### Iteração
Tipo de estrutura de controle que gerencia quantas vezes um trecho de código será executado.
Instruções de iteração For, While, Times, Do/While:

* **For**: Usado para percorrer uma coleção de elementos.
* **While**: Instrução que repete um bloco de código enquanto sua condição é verdadeira.
* **Times**: Executa uma repetição por um especificado número de vezes.
* **Do/While**: Na verdade, no Ruby utilizamos uma estrutura de repetição chamada loop que faz o mesmo que o do/while em outras linguagens de programação. Ele cria um laço de repetição que só é parado quando uma instrução break for verdadeira.

### Collections

O que são **Collections**? Na programação, collection representa um conjunto de dados semelhantes em uma única unidade.

**Array**: existem várias maneiras de manipular arrays. Abaixo encontram-se algumas muito úteis para todo programador.

* Criando um array vazio:
```Ruby
estados = []
```
Collections podem ter zero ou mais elementos.

##### Adicionando itens:

```Ruby
estados.push('Espírito Santo')
```
O push sempre irá adicionar itens de forma sequencial.

* Também é possível inserir vários elementos de uma só vez.
```Ruby
estados.push('Minas Gerais', 'Rio de Janeiro', 'São Paulo')
```

* Veja o array estados com a instrução
```Ruby
puts estados
```

* Para manter nossa coleção organizada em ordem alfabética ao inserir os itens ‘Acre’ e ‘Amapá’, devemos especificar que eles ocuparão as primeiras posições do array. Para isso contamos com o insert.
```Ruby
estados.insert(0, 'Acre', 'Amapá')
```
Primeiro é passado o valor do índice onde a instrução será aplicada  acompanhado por um ou mais itens a serem adicionados.

##### Acessando elementos:

O item de um array pode ser acessado pelo valor de seu index.

* Recupere o segundo elemento do array estados
```Ruby
estados[1]
```
Saiba que o primeiro elemento não inicia no índice 1, mas sim no 0.

* Você também pode acessar índices através de intervalos
```Ruby
estados[2..5]
```
Retorna os itens dos índices 2, 3, 4 e 5

* Utilizando números negativos conseguimos recuperar elementos a partir do ultimo item do array, de forma regressiva. O número -1 representa o ultimo elemento. Adquira o penúltimo elemento de estados
```Ruby
estados[-2]
```

* Também funciona com intervalos
```Ruby
estados[-3..-1]
```

* Uma forma muito intuitiva e natural de recuperar o primeiro item é usar first
```Ruby
estados.first
```

* Seguindo a mesma ideia, use last para o último
```Ruby
estados.last
```

##### Obtendo informações

* Para saber a quantidade de itens em um Array você pode utilizar qualquer uma destas duas instruções
```Ruby
estados.count
estados.length
```

* Descubra se o array está vazio
```Ruby
estados.empty?
```
O resultado será verdadeiro ou falso

* Verifique se um item específico está presente
```Ruby
estados.include?('São Paulo')
```
Igual ao empty, também resulta um valor verdadeiro ou falso

##### Excluindo elementos

* Remova um item através de seu índice
```Ruby
estados.delete_at(2)
```

* Exclua o ultimo item do array estados
```Ruby
estados.pop
```

* Para excluir o primeiro item faça
```Ruby
estados.shift
```

**Hash**: a seguir veja exemplos importantíssimos sobre manipulação de Hashes

##### Novo Hash

* Crie um hash vazio
```Ruby
capitais = Hash.new
```

* Um Hash também pode ser iniciado com vários pares de chave-valor
```Ruby
capitais = { acre: 'Rio Branco', sao_paulo: 'São Paulo'}
```

* A chave de um Hash pode ser qualquer tipo de dado
```Ruby
hash = {1 => 'Chave do tipo inteiro', true => 'Chave do tipo booleano', [1,2,3] => 'Chave do tipo array'}
```

##### Adicionando itens

* Adicione um novo item ao hash estados
```Ruby
capitais[:minas_gerais] = "Belo Horizonte"
```

* Acesse a capital que acabamos de inserir utilizando sua chave
```Ruby
capitais[:minas_gerais]
```
De forma sucinta, a chave é o index de nossos itens

* Para retornar todas as chaves de um hash
```Ruby
capitais.keys
```

* Agora, todos os valores de um hash  
```Ruby
capitais.values
```

##### Exclusão

* Remova um elemento chave-valor
```Ruby
capitais.delete(:acre)
```

##### Obtendo informações

* Descubra o tamanho do hash
```Ruby
capitais.size
```

* Verifique se o Hash está vazio
```Ruby
capitais.empty?
```

### Iterações
