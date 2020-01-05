# Aula 1 - Apresentando as Estruturas de Dados

Árvore binária: Duas subárvores. A binária tem no máximo grau 2 \
Grau de uma árvore é definido pelo número de subárvores de um nó. \
Grau 0: terminais ou folhas

Tudo que requer hierarquia, pode usar árvore.

**Grafo:** estrutura de dados não linear; conjunto de nós (vértices) e suas conexões (arcos) entre eles. Não existe limitações para os vértices.

**Fila:** segue a regra **FIFO** - first in, first out. **Inserção** de elementos na fila acontece **sempre ao final**. **Remoção** de um elemento sempre acontece no **início**.

Métodos de **pesquisa**: sequencial e binária
* **sequencial**: listas não ordenadas
* **binária**: listas ordenadas

**Lista**: mais simples para **agrupar** dados, formando um conjunto de elementos do **mesmo tipo** e preservando a relação de ordem linear entre os elementos.

* **nós** ou nodos: elementos de uma lista
* operações podem ser feitas com as listas
formas de inserção definem o tipo de lista: **pilha, fila**.
* Listas lineares: sequencial e encadeada.
    * **sequencial**: dados são armazenados na memória principal de forma **contígua** (matrizes)
    * **encadeada**: dados armazenados na memória em posições não adjacentes (**não contíguas**)

**Ordenação**: classificação dos dados.

**Pilha**: **inserção** de elementos sempre acontece no **topo** da pilha e a **remoção** também. 
* método de acesso: **LIFO** (last in, first out)

**Struct**: conjunto de elementos geralmente agrupados sob uma **lógica** e associados por um **nome**.
* cada elemento da estrutura é chamado de membro ou campo.

**Função**: bloco contendo cabeçalho, início e fim. Serve para executar tarefas menores.

**Lista encadeada:** se caracteriza por não ter seus nós alocados de forma contígua. **Cada nó da lista leva o endereço do próximo nó para não perder o encadeamento.** 
* Ponteiro para o primeiro nó
* do primeiro ao último segue o encadeamento através dos ponteiros presentes em cada nó
* último elemento aponta para o NULL

**Tipo de dados abstratos (TDA)**: conjunto de valores e uma coleção de operações que atuam sobre esses valores.

Dimensionando matrizes:
* **tipo nomeMatriz[tamanho];**
* **tipo nomeMatriz[tamLinha][tamColuna];**

tipo: int, float, double, char, long long int, etc

localizar um elemento da matriz: endereço-base + deslocamento * tamanho do tipo

0 significa que não tem deslocamento em relação ao endereço-base.

\0 finaliza o vetor de char