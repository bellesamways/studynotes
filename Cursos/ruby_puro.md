# Ruby Puro

Anotações do curso gratuito: https://onebitcode.com/course/ruby-puro/

Todos os exercícios desse curso estão no [repositório](https://github.com/bellesamways/ruby-exercises)

Roda várias linguagens https://repl.it/languages/ruby

Instalação do Ruby:
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
* – (Subtração)
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

##### Each

Percorre uma coleção de forma parecida ao for, porém, não sobrescrevendo o valor de variáveis fora da estrutura de repetição.

Em um *array*:

```Ruby
names = ['Joãozinho', 'Manoel', 'Juca']

name = 'Leonardo Scorza'

names.each do |name|
 puts name
end

puts name
```
Ao executar o programa perceba que não foi alterado o valor da  variável name, definida antes da estrutura de repetição.

Em um *hash*:
```Ruby
aulas = {'Aula 1 ' => 'liberada', 'Aula 2 ' => 'liberada', 'Aula 3 ' => 'liberada', 'Aula 4 ' => 'liberada', 'Aula 5 ' => 'em breve'}

aulas.each do |key, value|
 puts "#{key} #{value}"
end
```

Em cada vez que a estrutura percorre o hash, o elemento atual é representado por key e value.

##### Map

Cria um array baseando-se em valores de outro array existente.

```ruby
array = [1, 2, 3, 4]

# \n é uma quebra de linha
puts "\n Executando .map multiplicando cada item por 2"
# .map não altera o conteúdo do array original
new_array = array.map do |a|
  a * 2
end

puts "\n Array Original"
puts " #{array}"

puts "\n Novo Array"
puts " #{new_array}"

puts "\n Executando .map! multiplicando cada item por 2"
# .map! força que o conteúdo do array original seja alterado
array.map! do |a|
  a * 2
end

puts "\n Array Original"
puts " #{array}"
puts ''
```
Podemos forçar que o array original seja alterado utilizando map!

##### Select

Realiza uma seleção de elementos presentes em uma collection através de uma condição pré definida. Traz como resultado somente os valores que passam nesta condição.

Em um *array*:
```ruby
array = [1, 2, 3, 4, 5, 6]

selection = array.select do |a|
  a >= 4
end

puts selection
```
A condição para que um item do array seja selecionado é que seu valor seja maior ou igual a 4.

Em um *hash*:
```Ruby
hash = {0 => 'zero', 1 => 'um', 2 => 'dois', 3 => 'tres'}

puts 'Selecionando keys com valor maior que 0'
selection_key = hash.select do |key, value|
  key > 0
end

puts selection_key
```
Veja que dentro de um Hash podemos fazer uma seleção por chave ou valor.

Alguns links importantes:
- https://ruby-doc.org/core-2.6/Enumerable.html
- https://ruby-doc.org/core-2.6/Enumerable.html#method-i-sort_by
- http://www.rubyinside.com/how-to/ruby-sort-hash

### Métodos

Forma de organizar funções específicas de um programa.  Caso necessário permite a reutilização de código.

**Como criar?**
- Para definir um método utiliza-se a palavra reservada def seguida pelo nome do método. Depois é escrito um conjunto de expressões, e por fim, a palavra end determina o término do método.
- Para executar um método basta apenas escrever o seu nome.  

**Parâmetros**: Um método pode depender de um ou mais parâmetros para realizar determinada tarefa. Definindo um valor padrão ao parâmetro, ele torna-se opcional.

**Retorno**: O retorno de um método ruby é sempre o resultado de sua última instrução.

### Gems

Pacote que oferece funcionalidades a fim de resolver uma necessidade específica de um programa Ruby. Pense como o conceito de biblioteca em outras linguagens de programação.

**Como instalar uma gem:**
```Ruby
gem install [gem_name]
```

**Novas Funcionalidades**: No começo do arquivo, o require ‘gem_name’ carrega os arquivos da gem. Isso possibilita a declaração de códigos com funcionalidades da biblioteca.

**Desinstalar uma gem:**
```Ruby
gem uninstall [gem_name]
```

**Informação**: Liste todas as gems instaladas na máquina rodando
```Ruby
gem list
```

**Bundler**: Para ter controle sobre as dependências de um projeto contamos com uma ferramenta que procura e instala gems chamada Bundler.
```Ruby
gem install bundler
```

Salve a lista de gems do projeto em um arquivo chamado Gemfile
```ruby
source 'https://rubygems.org'
gem 'os'
```

Na primeira linha é definido onde o bundle deve procurar pelas gems. Depois é listado as dependências do projeto.
Instale estas gems com o comando:
```ruby
bundle install
```

### Programação Orientada a Objetos

POO (Programação Orientada a Objetos) é um  Paradigma de programação criado para lidar com softwares grandes e complexos.

Sua estrutura é definida por 04 pilares: Abstração, Encapsulamento, Herança e Poliformismo.

**Abstração**: Ação de abstrair uma entidade do mundo real e transformá-la em uma classe.

**Encapsulamento**: Ato de dividir um programa em diversas partes tornando-o flexível, fácil de modificar e incluir novas funcionalidades.

**Herança**: Habilidade de criar uma Classe com características de outra existente. A herança prove o reuso e reaproveitamento de código.

**Poliformismo**: Capacidade de utilizar um método de diferentes formas para diferentes Objetos.

**Objeto**

Objeto é toda coisa material que pode ser percebida pelos sentidos, como por exemplo um carro, livro, cachorro, caneta, avião e etc. Na programação um objeto é a representação de um objeto do mundo real. Todos estes objetos apresentam duas característica em comum: informações e comportamentos.

Ex:  Cachorro

**Informações = attributes**
* Raça: Pastor Alemão
* Peso: 35 Quilos
* Idade: 3 Anos

**Comportamento = methods**
* Late
* Come
* Corre

**Classe**

Tendo como exemplo o objeto carro, pense em uma classe como a planta deste carro. Com ela é possível construir vários carros. Uma classe é como a planta de um objeto.

Classes no Ruby: definida pela palavra *class* seguida de seu *Nome*, e finalizada pela palavra *end*. O nome de uma classe deve sempre começar com letra maiúscula. Para nomes compostos utilize o padrão *CamelCase*.

```ruby
class Computer
  def turn_on
    puts 'turn on the computer'
  end

  def shutdown
    puts 'shutdown the computer'
  end
end
```
##### Herança
Para herdar características de outra classe, adicione na frente do nome de uma classe filha o símbolo de menor e  depois o nome da classe pai.

```ruby
class ClasseFilha < ClassePai
end
```

##### Poliformismo

Poder chamar o mesmo método com o mesmo nome e ter comportamentos diferentes.

Se usar a palavra reservada *super* ela chama o método pai mesmo que você coloque outra instrução dentro do método.

##### Require

É possível importar arquivos que eu mesma escrevi e não só gems.

Assim vai especificar o arquivo que será procurado require *'./nomedoarquivo.rb'*

Se só existe um arquivo com aquele nome, é possível chamar assim: *require_relative 'animal'*

Se o aquivo *animal* estivesse dentro de uma pasta *example*, ficaria assim: *require_relative 'example/animal'*

Se o arquivo já faz um require, não precisa fazer de novo no mesmo arquivo.

##### Escopo das variáveis

**Variável Local**: É declarada com a primeira letra de seu nome sendo uma letra minúscula ou sublinhado. Pode ser acessada apenas onde foi criada. Por exemplo, se você definir uma variável local dentro de de uma classe ela estará disponível apenas dentro desta classe, se a definiu dentro de um método conseguirá acessá-la apenas dentro deste método e assim por diante.

**Variável Global**: Declarada com o prefixo $. Pode ser acessada em qualquer lugar do programa. Seu uso é FORTEMENTE DESENCORAJADO pois além de ser visível em qualquer lugar do código, também pode ser alterada em inúmeros locais ocasionando dificuldades no rastreamento de bugs.

**Variável de Classe**: É declarada com o prefixo @@. Pode ser acessada em qualquer lugar da classe onde foi declarada e seu valor é compartilhado entre todas as instâncias de sua classe.

**Variável de Instância**: Seu nome começa com o símbolo @. Semelhante a variável de classe, tendo como única diferença o valor que não é compartilhado entre todas as instâncias de sua classe.

##### Atributos

Também conhecidos como variáveis de instância, em Ruby são sempre privados e começam com @. Não há como alterá-los de fora da classe; apenas os métodos de um objeto podem alterar os seus atributos (encapsulamento!).

O ruby disponibiliza um método chamado **attr_accessor** que cria os métodos var e var= para todos atributos declarados.
```ruby
class Dog
  attr_accessor :name, :age
end

dog = Dog.new

dog.name = 'Marlon'
puts dog.name

dog.age = '1 ano'
puts dog.age
```

##### Construtores

Podemos fazer com que algum código seja executado na criação de um objeto. Para isso, todo objeto pode ter um método especial, chamado de initialize:

```Ruby
class Pessoa
  def initialize
    puts "Criando nova Pessoa"
  end
end

Pessoa.new
# => "Criando nova Pessoa"
```

Os initializers são métodos privados (não podem ser chamados de fora da classe) e podem receber parâmetros.

```Ruby
class Pessoa
  def initialize(nome)
    @nome = nome
  end
end

joao = Pessoa.new("João")
```

Métodos acessores e modificadores são muito comuns e dão a ideia de propriedades.

O número de parâmetros utilizados no método initialize é opcional.

##### Blocks
Um bloco pode ser entendido como uma função anônima = função sem nome.
Definido entre *do..end* ou *colchetes* e pode receber parâmetros para sua execução.
```ruby
5.times { puts "Exec the block" }
```

```ruby
sum = 0
numbers = [5, 10, 5]
numbers.each {|number| sum += number }
puts sum
```

```ruby
foo = {2 => 3, 4 => 5}
foo.each do |key, value|
 puts "key = #{key}"
 puts "value = #{value}"
 puts "key * value = #{key * value}"
 puts '---'
end
```

```ruby
def foo
 # Call the block
 yield
 yield
end
foo { puts "Exec the block"}
```

Quando você adiciona o **yield** ele automaticamente já sabe que deve chamar um bloco que foi declarado como parâmetro.

O ruby oferece um método chamado **block_given?** para verificar se o bloco foi passado como argumento

```Ruby
def foo
 if block_given?
   # Call the block
   yield
 else
   puts "Sem parâmetro do tipo bloco"
 end
end


foo
foo { puts "Com parâmetro do tipo bloco"}
```

A saída do programa será:
```
Sem parâmetro do tipo bloco
Com parâmetro do tipo bloco
```

Outra forma de receber blocos como parâmetro é utilizar o símbolo **&**. Para executar um bloco recebido desta forma é necessário apenas utilizar o nome do bloco acompanhado pelo método **call**. Outra dica importante é sempre deixar o **&nome_do_bloco** como último parâmetro a ser recebido pelo método.

```Ruby
def foo(name, &block)
 @name = name
 block.call
end

foo('Leonardo') { puts "Hellow #{@name}" }
```

```ruby
def foo(numbers, &block)
  if block_given?
    numbers.each do |key, value|
      block.call(key, value)
    end
  end
end

numbers = { 2 => 2, 3 => 3, 4 => 4 }

foo(numbers) do |key, value|
 puts "#{key} * #{value} = #{key * value}"
 puts "#{key} + #{value} = #{key + value}"
 puts "---"
end
```

##### Lambda
São similares aos blocks, mas podem ser **salvas em variáveis para serem reutilizadas**. É uma versão especial de um bloco. Ela pode ser guardada em uma variável para ser chamada futuramente com o método **call**.

```ruby
first_lambda = lambda { puts "my first lambda"}
first_lambda.call
```

também funciona com o -> no lugar da palavra lambda
```ruby
first_lambda = -> { puts "my first lambda"}
first_lambda.call
```

também pode ter vários parâmetros para a execução
```ruby
first_lambda = -> (names){ names.each { |name |puts name} }
names = ["joão", "maria", "pedro"]
first_lambda.call(names)
```

lambdas que ocupam várias linhas, não declare a lambda de forma abreviada e utilize o *do..end*
```ruby
my_lambda = lambda do |numbers|
 index = 0
 puts 'Número atual + Próximo número'
 numbers.each do |number|
   return if numbers[index] == numbers.last
   puts "(#{numbers[index]}) + (#{numbers[index + 1]})"
   puts numbers[index] + numbers[index + 1]
   index += 1
 end
end

numbers = [1, 2, 3, 4]

my_lambda.call(numbers)
```

você pode passar mais de uma lambda como argumentos de um método.
```ruby
def foo(first_lambda, second_lambda)
 first_lambda.call
 second_lambda.call
end

first_lambda = lambda { puts "my first lambda"}
second_lambda = lambda { puts "my second lambda"}

foo(first_lambda, second_lambda)
```

##### Modules
Possuem duas funções:
* namespace: serve como container para agrupar objetos relacionados (classes, constantes, métodos ou outros modules)
* mixins: serve para incluir funcionalidades extras nas classes.

**Namespace**:

```ruby
module ReverseWorld
  def self.puts text
    print text.reverse.to_s
  end
end

ReverseWorld::puts 'O resultado é'
puts 'O resultado é'
```

**Mixins**:
```ruby
module ImpressaoDecorada
  def imprimir text
    decoracao = '#' * 100
    puts decoracao
    puts text
    puts decoracao
  end
end

module Pernas
  include ImpressaoDecorada

  def chute_frontal
    imprimir 'Chute Frontal'
  end

  def chute_lateral
    imprimir 'Chute Lateral'
  end
end


module Bracos
  include ImpressaoDecorada

  def jab_de_direita
    imprimir 'Jab de direita'
  end

  def jab_de_esquerda
    imprimir 'Jab de esquerda'
  end

  def gancho
    imprimir 'Gancho'
  end
end

class LutadorX
  include Pernas
  include Bracos
end

class LutadorY
  include Pernas
end

lutadorx = LutadorX.new
lutadorx.chute_frontal
lutadorx.jab_de_direita

lutadory = LutadorY.new
lutadory.chute_lateral
```

##### Proc
Um pedaço de código que pode ser executado e passado como parâmetro para outros métodos.
```ruby
hello_proc = Proc.new do
  puts "Hello World"
end
hello_proc.call
```

podemos ainda usar "proc" ao invés de "proc.new"
```Ruby
hello_proc = proc do
  puts "Hello World"
end
hello_proc.call
```

```Ruby
hello_lambda = lambda {}
hello_proc = proc {}
hello_proc.class #=> Proc
hello_lambda.class #=> Proc
```

##### Procs vs. Lambdas
```Ruby
hello_proc = proc do |msg|
  puts msg
end
hello_proc.call
```

A saída é uma linha vazia, pois o parâmetro “msg” não foi passado. Assim, podemos ver que procs automaticamente atribuem “nil” para variáves cujo valor não tenha sido definido.

```Ruby
hello_lambda = lambda do |msg|
  puts msg
end
hello_lambda.call
```

Aqui ele lançará uma exceção *“ArgumentError: wrong number of arguments (0 for 1)”*! Ou seja, **os argumentos são necessários para a execução de um lambda**. No entanto, podemos contornar esse problema utilizando valores default para o lambda.
```Ruby
hello_lambda = lambda do |msg = nil|
  puts msg
end
hello_lambda.call
```

Outra grande diferença está em como o “return” é tratado. O “return” em um lambda retorna o fluxo de execução para o método onde o lambda foi chamado.
```Ruby
hello_lambda = lambda do |msg|
  return msg
end
def run_hello_block(block)
  puts "Preparando para executar lambda..."
  puts "Lambda em execução: #{block.call("Hello World")}"
  return "Lambda executado com sucesso!"
end
puts run_hello_block(hello_lambda)
```

Tudo funciona como esperado e todas as mensagens são exibidas. No entanto, o mesmo pedaço de código, agora utilizando proc, tem um resultado bem diferente:
```Ruby
hello_proc = proc do |msg|
  return msg
end
def run_hello_block(block)
  puts "Preparando para executar proc..."
  puts "Proc em execução: #{block.call("Hello World")}"
  return "Proc executado com sucesso!"
end
puts run_hello_block(hello_proc)
```

Ao tentar executar este código veremos uma exceção *“LocalJumpError: unexpected return”*. Esta exceção é lançada quando tentamos executar um return dentro de um argumento, exceto quando o argumento é um lambda.

Uma maneira de resolver o problema seria definir o proc dentro do método, assim ele não seria mais um parâmetro e poderia retornar algo:
```Ruby
def run_hello_block
  hello_proc = proc do |msg|
    return msg
  end
  puts "Preparando para executar proc..."
  puts "Proc em execução: #{hello_proc.call("Hello World")}"
  return "Proc executado com sucesso!"
end
puts run_hello_block
```

Referência: https://brizeno.wordpress.com/2013/10/30/conceitos-na-pratica-ruby-procs/

### Regex
Abreviatura de Regular Expressions (Expressões Regulares), regex é uma sequência de caracteres especiais que nos ajudam a identificar (e selecionar) padrões de caracteres em strings.

**3 maneiras de criar um regex**

1. utilizando o formato /.../ sendo a mais comum
```ruby
/expressao/
```
2. através do formato %r{...}
```ruby
%r{expressao}
```
3. utilizando um construtor através do Regex.new('...')
```ruby
Regex.new('expressao')
```

**Casamento de padrões**: é um ato que verifica a presença de padrões em uma cadeia de caracteres. Pode ser realizado através do **operador =~** ou do método **match**.

##### Operador =~
* O operador **=~** retorna o offset, ou seja, a distância entre o começo da string até o local onde ocorre o casamento de padrão especificado na expressão.
* A mesma comparação pode ser realizada iniciando pela string.
* Quando não ocorre o casamento de padrão, o resultado é **nulo**.

##### Método match
* Retorna um objeto do tipo **MatchData**, contendo todos os resultados do casamento de padrão.
* Em um objeto do tipo **MatchData** você pode, por exemplo, acessar o que vem antes do casamento através do método **pre_match**
* Ou acessar o que vem depois do casamento com **post_match**


##### Metacharacters and Escapes
Os símbolos __(, ), [, ], {, }, ., ?, +, \*__,  são **metacharacters**. Eles possuem um significado quando utilizados em expressões regulares. Caso o padrão que você procura seja um metacharacter, utilize o símbolo de escape \ para realizar a busca.

*Character Classes*: É uma lista que informa quais caracteres devem aparecer em um ponto do casamento.
* Uma character class é delimitada por colchetes [, ]
* Você pode especificar um range com o símbolo –
* O range pode ser utilizado para letras
* Existem alguns metacharacters que se comportam como character classes, exemplo, o metacharacter \d verifica o padrão [0-9].

*Repetition*: É possível definir a repetição de um mesmo padrão, evitando escrever a mesma coisa diversas vezes.
* Ao em vez de digitar \d\d\d você pode escrever \d{3}
* A vírgula em {3, } informa que a repetição pode ocorrer 3 ou mais vezes

### Math
É um método nativo para funções matemáticas.

* Raiz quadrada de 64: `Math.sqrt(64)`
* Logaritmo de 10000 na base 10: `Math.log10(10000)`
* Logaritmo de 16 na base 2: `Math.log2(16)`
* Calculando o cosseno para o ângulo de 30º
    * Primeiro transforme o ângulo em um valor radiano: `radian = 30 * (Math::PI / 180)`
    * Depois utilize o método cos: `Math.cos(radian)`
* Para consultar o valor da constante E execute: `Math::E`
* Consulte o valor da constante PI com a instrução: `Math::PI`

### Time
O Ruby conta com uma classe chamada Time para representar datas e horas.

* Para imprimir o horário atual execute:
```ruby
time = Time.now
puts time
```
* Para o ano, year: `puts time.year`
* Para o mês: `puts time.month`
* Para o dia: `puts time.day`
* O método *strftime* permite a formatação de uma data em uma forma específica. Essa formatação é feita por diretivas que começam com o símbolo de %.
```Ruby
time.strftime('%d/%m/%y')
```
**Significado das diretivas**:
- %d -> Dia do mês
- %m -> Mês do ano
- %y -> Ano


* Verificando se o dia da semana é sábado: `puts time.saturday?`
* Você também pode comparar duas datas.
    * Crie um novo objeto com o horário atual: `time2 = Time.now`
    * Ao comparar as datas de forma completa o resultado será false: `time == time2 # => false`
    * Comparando o ano das duas datas, o resultado será true: `time.year == time2.year # => true`

### Missing Methods
Ele é utilizado para interceptar chamadas a métodos que não existem. Quando um método que não existe é chamado, o método method_missing faz uma interceptação.

### Self
No ruby, *self* é uma variável especial que aponta para o objeto atual.
A variável self não precisa ser declarada. Ela é disponível em qualquer lugar, mas não esqueça que seu valor é referente ao objeto que pertence.
Variáveis self em objetos diferentes possuem valores diferentes.
Com o self é possível criar métodos de classe,  que não precisam de uma instância para serem chamados.
Você também pode utilizá-lo para se referir a atributos do objeto atual.

### Métodos Private e Protected
Por padrão, todos os métodos definidos são públicos. Isso significa que eles podem ser acessados por qualquer um.

Mas além dos métodos públicos, existem outros dois tipos de métodos chamados *private* e *protected*.

*Private*: Método interno de uma classe. Apenas os métodos públicos dessa classe ou de classes descendentes podem chamá-lo. O self é o único receptor de um método private

*Protected*: A diferença entre ele e o private, é que o método protected pode ter como receptor qualquer instância de sua classe.

### Leitura e Escrita de Arquivos
Através de poucas instruções, é possível ler o conteúdo, ou então, escrever algumas informações dentro de um arquivo externo. Isso é feito por meio de uma classe chamada File, a qual conta com diversas opções para manipulação de arquivos.

**Leitura de arquivo**: método **open** da classe **File** para acessar o arquivo **list.txt**. Depois o método **each** para percorrer e exibir o conteúdo do arquivo.

**Escrita de arquivo**: Para adicionar conteúdo sem sobrescrever o que já existe , foi necessário passar o argumento ‘a’. Este argumento significa **append**, ou seja,  acrescentar conteúdo. Perceba que o método puts e print tem o mesmo significado do que em outros exemplos deste curso. **Os dois inserem valores ao arquivo, com a diferença de que apenas o puts insere uma nova linha após a string.**


Caso queira saber o tamanho do arquivo: O método size retorna o tamanho do arquivo em bytes.

```Ruby
File.open('shopping-list.txt').size
```

Para substituir o conteúdo desse arquivo utilize o argumento ‘w’ no lugar do 'a', de **write**.

### Chamadas Web
Para isso o ruby conta com uma biblioteca chamada **Net::HTTP** que é capaz de realizar chamadas web.

##### Requisições http
```Ruby
require 'net/http'

example = Net::HTTP.get('example.com', '/index.html')

File.open('example.html', 'w') do |line|
 line.puts(example)
end
```

O que aconteceu?

- No início, é preciso  adicionar a biblioteca **Net::HTTP**
- Depois é feito uma requisição *HTTP* do tipo *GET* para o domínio *example.com*, com o caminho */index.html*.
- É a mesma coisa que entrar no browser e procurar pelo endereço *http://example.com/index.html*
- Você salvou a resposta dentro de uma variável para depois escrevê-la dentro de um arquivo.
- Quando você utilizou *File.open* para um arquivo inexistente, o ruby detectou isso e criou o arquivo antes de escrever as informações nele.

##### Requisições https
Para fazer as próximas requisições  você utilizará o site https://reqres.in
Ele está preparado para receber e responder suas requisições, o que facilitará os testes de requisições https.

```Ruby
require 'net/http'

https = Net::HTTP.new('reqres.in', 443)
# para fazer chamadas https
https.use_ssl = true

response = https.get("/api/users")
# status code
puts response.code
# status message
puts response.message
# body (json)
puts  response.body
```

O que aconteceu?

- Você construiu um objeto **Net::HTTP** iniciando com os valores de  domínio e porta
- Você informou que é uma requisição que utiliza o certificado ssl com o método `use_ssl = true`
- Fez um *GET* para o caminho *api/users*
- Por fim exibiu o código da resposta, o status e o corpo da resposta

```Ruby
require 'net/http'

req = Net::HTTP::Post.new("/api/users")
# para fazer chamadas https
req.set_form_data({ name:'Mario', job:'Encanador' })

response = Net::HTTP.start('reqres.in', use_ssl: true) do |http|
  http.request(req)
end

puts response.code
puts response.body
```

O que aconteceu?

- Você inicializou um objeto `Net::HTTP::Post.new()` passando como argumento o caminho da url
- Depois informou quais são os  parâmetros a serem enviados com o método `set_form_data`
- Por fim utilizou o método *start* para criar uma conexão com o servidor e dentro de um bloco fez a requisição *POST*

##### Web Scraping
O Web Scraping existe para evitar essas tarefas manuais, ou então, trabalhosas. Uma técnica que automatiza o processo de extração de dados de uma página web.

Uma das bibliotecas mais utilizadas no mundo ruby para fazer isso é a **nokogiri**

```Ruby
require 'nokogiri'
require 'net/http'

https = Net::HTTP.new('onebitcode.com', 443)
# para fazer chamadas https
https.use_ssl = true

response = https.get("/")

doc = Nokogiri::HTML(response.body)

h1 = doc.at('h1')

puts h1.content
```

O que aconteceu?

- No começo nenhuma novidade. Você realizou uma requisição para o site do onebitcode
- Depois utilizou **Nokogiri::HTML** para parsear o documento HTML
- Por fim, você fez uso do método at para buscar a tag h1 e imprimir o seu conteúdo.

O último post do onebitcode encontra-se dentro das tags \<h3>\<a href=’/ultimo-post’>Título Ultimo Post\</a>\</h3>. Para buscar este post faça:
```Ruby
last_post = doc.at('h3 a')
puts last_post.content
puts last_post['href']
```

Você também pode procurar por todos os posts que estão na página inicial do onebitcode com o método search

```Ruby
doc.search('h3 a').each do |a|
  puts a.content
  puts a['href']
  puts ''
end
```
