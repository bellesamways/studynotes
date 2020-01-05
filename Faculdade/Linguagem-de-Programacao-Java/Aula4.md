## Aula 4 - PRINCÍPIOS DA ORIENTAÇÃO A OBJETOS

#### Introdução classes e objetos

As classes definem a estrutura e o comportamento de um tipo de objeto.
**Classes**: Um protótipo que define os atributos e os métodos comuns a todos os objetos de um determinado tipo e da própria classe, com a finalidade de servir de molde para a criação de objetos.
**Objetos**: São a representação de uma entidade do mundo real, que tem identificador único, propriedades embutidas e a habilidade de interagir com outros objetos e consigo mesmo.  Um objeto é uma instância de uma classe. A classe descreve todas as características e funcionalidades de um objeto. Modelamos os objetos através das classes.

##### Abstração
* Extrair tudo que for essencial e mais nada para o escopo do sistema;
* É o processo de filtragem de detalhes sem importância do objeto real, para que apenas as características apropriadas que o descrevam tenham relevância para o sistema permaneçam;
* Conceito aplicado a criação de software baseado em objetos, partindo do princípio que devemos considerar a essência de cada objeto e não pensar em todos os detalhes de implementação.

##### Encapsulamento
* Mecanismo utilizado em OO para obter segurança, modularidade e autonomia dos objetos;
* Implementamos através da definição de visibilidade privada dos atributos;
* Sempre definir os atributos de uma classe como privados;
* Esse mecanismo protege o acesso direto aos dados do objeto;
* Permite acesso através dos métodos públicos;
É a disponibilização de uma interface pública, com granularidade controlada, para manipular os estados e executar as operações de um objeto (* acesso permitido).

|Modificadores|Mesma classe|Mesmo pacote|Subclasses|Universo|
|:-:          |:-:         |:-:         |:-:       |:-:     |
|private      |*           |            |          |        |
|\<sem modif> |*          |*           |          |        |
|protected    |*           |*           |*         |        |
|public       |*           |*           |*         |*       |
Os atributos e métodos de um objeto podem ser escondidos de outros objetos por uma interface pública de métodos, de modo a impedir acesso indevidos.

#### Definindo uma classe em java
A primeira linha é um comando que inicia a declaração da classe.
Após a palavra-chave **class**, segue-se o nome da classe, que deve ser um identificador válido para a linguagem.
O modificador **modif** é opcional; se presente, pode ser uma combinação de **public** e **abstract** ou final.
A definição da classe, propriamente dita, está entre as chaves **{** e **}** que delimitam blocos na linguagem Java.
```Java
[modif] class NomeDaClasse {
   // corpo da classe...
}
```
Corpo da classe segue, geralmente, a ordem abaixo:
1. **Variáveis de classe** (definidas como static), ordenadas segundo sua visibilidade: iniciando pelas **public**, depois **protected**, depois com **visibilidades padrão** (sem modificador) e depois as **private**.
2. **Atributos** (variáveis de instância) dos objetos dessa classe, seguindo a mesma ordenação segundo a visibilidade definida para as variáveis de classe.
3. Os **construtores** de objetos dessa classe.
4. Os **métodos da classe**, geralmente agrupados por funcionalidade.

#### Criando objetos em java
Construtor é responsável por alocar memória para o objeto. A criação de um objeto se dá através da aplicação do operador new.
```Java
ClasseNome objeto = new ClasseNome();
```
O método a direita do operador new é o construtor da classe ClasseNome.

**Atributos**: representam as características do objeto. Devem ser privados.
```Java
[modificador] tipo nome [ = default];
```
* modificador é opcional, especificando a visibilidade diferente da padrão;
* tipo deve ser um dos tipos primitivos do java ou o nome de uma classe;
* nome deve ser um identificador válido do java;
* valor default é opcional; se presente, especifica um valor inicial para a variável.

**Métodos**: representam as funcionalidades que os objetos podem desempenhar. Além dos atributos de objetos, métodos podem definir e manipular variáveis locais; também podem receber parâmetros por valor através da lista de argumentos.
```Java
[modificador] tipo nome(argumentos)
{
    //corpo do método
}
```
* modificador (opcional) é uma combinação de: public, protected ou private; abstract ou final; e static;
* tipo é um indicador do valor de retorno, sendo void, se o método não tiver um valor de retorno;
* nome do método deve ser um indicador válido no java;
* os argumentos são representados por uma lista de parâmetros separados por vírgulas onde, para cada parâmetro, é indicado primeiro o tipo e depois (separado por espaço) o nome.
  
*Boa prática -> manter a funcionalidade de um método simples, desempenhando uma única tarefa*.