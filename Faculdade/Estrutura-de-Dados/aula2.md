# Aula 2 - Funções

Única função obrigatória é a main.

**Modularização**: melhorar o entendimento do programa, encontrar erros com mais facilidade, simplificar a manutenção, reutilização de código, etc. São "pequenos programas" conhecidos como funções.

### Função
Uma função é um conjunto de comandos limitado por um par de chaves e precedido por um cabeçalho.

**Definição de função:**
```
<tipo de função> nome da função (declarações dos parâmetros) {
    <declaração das variáveis locais>
        comandos que formam o corpo da função
    return <valor>; // return; ou nada
}
```

* tipo de função: tipo de retorno da função
* nome da função: deve sugerir a finalidade da função
* variáveis locais: variáveis que vão ser utilizadas dentro da função (tipo e nome)
* corpo da função: conjunto de comandos
* return \<valor>: só existe esse comando se a função retornar um valor para a função chamadora
* return; ou nada: para função do tipo *void*

**Protótipo de uma função:**
```
<tipo de função> nome_da_função (declarações dos parâmetros);
```

Podem ser colocadas **antes ou depois** da *main*.
* **Antes**: serão conhecidas pelo compilador antes de serem chamadas, evitando problemas. Isso diminui a legibilidade do programa dependendo do tamanho dele.
* **Depois**: aumenta a legibilidade, mas cria-se um problema: função é chamada antes da identificação dela pelo compilador. Resolve-se esse problema com os **protótipos** das funções **antes** da *main* e as definições depois da main.

**Chamada da função e o seu retorno**
Quando uma função é chamada, o fluxo de controle é direcionado a executar os comandos da função e depois ele volta para onde foi ativado (se for void) ou ao ponto de onde ela foi chamada, para funções com retorno.

Não podemos desconsiderar o tipo de retorno e os parâmetros caso existam.

**Tipos de funções:**
1. **Funções sem parâmetros**

    No C++ não é obrigatório o uso de parâmetros em todas as funções. Uma função que não retorna nada é do tipo void, e é hierarquicamente considerado abaixo da main.
    Ela é chamada pelo nome, sem necessitar de comando que a anteceda.
    ```
    nomeDaFuncao();
    ```

2. **Funções com parâmetros**
   
   1. **Passagem por valor**: uma cópia do valor, ou valores, é passada para os parâmetros formais da função chamada através dos parâmetros reais da função chamadora. Podendo ser representados por variáveis ou constantes. 
   2. **Passagem por referência**: o endereço da variável é passado para a função chamada e dessa forma o valor poderá ser alterado. Em C era passado usando ponteiro, em C++ usa-se a **referência** (&).
   
        ```
        void troca (float &a, float &b);
        ```
        1. *Passagem por referência por ponteiros (passagem por nome ou passagem por endereço):* **&** é o endereço e **\*** é o conteúdo do endereço apontado
        2. *Passagem por referência*: referência não é ponteiro, mas ambos manipulam endereço.


| Função | Significado |
| - | - |
| **void linha(char c, int n);** | Função que recebe dois argumentos por passagem de valor. Um do tipo char e outro do tipo int, mas não retorna nada para função chamadora. |
| **int descobreIdade(int anoAtual, int anoNas)**; | Função que recebe dois argumentos por passagem de valor. Os dois do tipo inteiro e retorna, para a função chamadora, um valor inteiro.|
| **float areaRetangulo(float, float);** | Função que recebe dois argumentos reais e retorna, para a função chamada, um valor real. |
| **void troca(float&, float&)** | Função que recebe dois argumentos que são endereços que armazenam números reais, por passagem por referência. A função não retorna nada para a função chamadora. |


Uma função que retorna valor deverá ser chamada através de um comando, não importando se ela tem, ou não, parâmetros. Uma função só poderá retornar um valor!

**Return**: Uma função que retorna valor terá, obrigatoriamente esse comando no corpo da função. Isso não quer dizer que não poderá ter mais de um comando return no corpo da função. Quando existir múltiplas respostas, poderemos ter vários tipos de retorno. Pode estar presente uma variável, uma constante, uma expressão.

**Variáveis locais**: variáveis só visualizáveis dentro das funções onde foram declaradas. \
**Variáveis globais:** variáveis declaradas fora do escopo de todas as funções. Pode ser manipulada por qualquer função.

**Padrão da main**: *int main ();* \
Return da main poderia ser dispensável, pois ele já retorna automaticamente para o SO. \
Bom hábito: *return 0;* ou *return EXIT_SUCESS;*

**Passando uma estrutura de dados homogênea para uma função**