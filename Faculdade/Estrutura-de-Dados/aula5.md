## Aula 5 - A estrutura de dados - Lista 

### Definição

A estrutura que permite representar um conjunto de dados de forma a preservar a relação de ordem linear (ou total) entre eles é a lista linear. Uma lista linear é composta de nós, os quais podem conter, cada um deles, um dado primitivo ou um dado composto. 


* nó ou nodo: item da lista 
* comprimento ou tamanho de uma lista: números de nós de uma lista. 
* se uma lista é composta de nós, uma Lista Vazia é uma lista que não tem nós.  


### Agrupamento
* **Sequencial**: apresenta os nós em posições contíguas de memória, isto é, um após o outro. Sendo assim, fica fácil identificarmos o endereço de qualquer nó de uma Lista Sequencial. 

* **Encadeado**: um conjunto de nós (nodos) encadeados onde cada nó contém o dado e um apontamento para o próximo nó, visto que eles não estão alocados de forma contígua. 


O agrupamento é a forma como os dados são armazenados na memória principal. Pode ser confundido com alocação estática ou alocação dinâmica.  

* **Estática**: determinada durante a compilação. 

* **Dinâmica**: você poderá determinar o tamanho, ou acrescentar, durante a execução. 

![](/media/estrutura_dados/agrupamento.png)


#### Lista linear sequencial 

Ideal para um conjunto pequeno de dados.  
 

Apresenta a vantagem do acesso ao nó pelo índice.  
Desvantagem da movimentação quando se remove dado e insere se desejarmos deixar os vazios ao final.  
 

A forma de acesso à LISTA no que diz respeito à inserção e à remoção de um dado determina uma classificação. 

![](/media/estrutura_dados/listaLinear.png)


* **Pilha**: A inserção e a remoção é sempre realizada em um extremo da lista. 
* **Fila**: A inserção é feita em um extremo e a remoção em outro. 
* **Fila Dupla**: DEQUE( Double-Ended Queue), significando fila de extremidade dupla. 
* **FDER - Fila Dupla de Entrada Restrita**: Nesse tipo de Fila, a remoção do elemento pode acontecer em qualquer extremidade, mas a inserção, em apenas uma. 
* **FDSR - Fila Dupla de Saida Restrita**: Nesse tipo de Fila, a inserção do elemento pode acontecer em qualquer extremidade, mas a recuperação, em apenas uma. 
Inicializar uma lista é atribuir zero à variável que será responsável por armazenar a quantidade de dados que já se encontram na lista. 