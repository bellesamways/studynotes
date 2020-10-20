# Aula 8 -  Listeners e adapters 
 

### Eventos 

Evento é um acontecimento relevante no meio externo ao sistema relevante. Pode ser considerado como o resultado da interação do usuário com algum componente GUI. Mover o mouse, clicá-lo, digitar num campo de texto, selecionar um item de menu, fechar uma janela, clicar num botão etc. são interações que enviam eventos para o programa, normalmente realizando serviços.  


Eventos também podem ser gerados em resposta a modificações do ambiente. Em outras palavras, definem-se eventos GUI como mensagens (chamadas a métodos) que indicam que o usuário do programa interagiu com um dos componentes GUI. 

**Um sistema orientado a objetos é definido como um conjunto de objetos interagindo ou trocando mensagens**. Os eventos representam as ações dos atores nesse processo ou alguma resposta a uma mudança de estado. 
 

### Tratamento de eventos 
Quase todos os componentes propagam eventos. Esses eventos devem ser tratados em algum ponto do código da aplicação. Os eventos nunca são tratados no próprio componente (dado que não se tem acesso ao código do componente).  

Para ligar o código do tratamento de eventos ao componentes existem, no Java, um conjunto de interfaces chamadas **listeners**. Um **listener** é uma interface que especifica os métodos que uma aplicação deve ter para ser notificada da ocorrência de um determinado evento.  

Os componentes que geram eventos permitem que sejam adicionados ou removidos listeners em qualquer altura.  

O modelo de eventos do Java funciona da seguinte forma: O componente que produz eventos possui métodos especiais do tipo addXXListener(XXListener) que permite adicionar ou remover listeners. XX representa o nome do evento. O método addXXListener recebe, por parâmetro, o objeto que implementa a interface XXListener. A implementação do método addXXListener no componente apenas adiciona o objeto, passado por parâmetro a uma lista interna. **Sempre que ocorrer um evento (exp.: botão pressionado), o componente percorre a lista e invoca, para cada elemento, o método definido na interface XXListener.**

![](/media/Linguagem_de_Programacao-Java/Aula8/listener.PNG)

Resumindo:  

**ActionEvent** - gerado pelo botão quando pressionado. sempre que o botão for pressionado, este irá percorrer a sua lista interna de listeners, chamando para cada um o método actionPerformed. 

**ActionListener** - interface que especifica os objetos que tratam eventos do tipo ActionEvent. existem várias soluções possíveis para tratar o evento: 
* recorrendo a própria classe (GUI) - a aplicação gráfica tem de implementar os listeners necessários 
* recorrendo a classes locais - é criada uma classe local que implementa os listeners necessários 
* recorrendo a classes internas - é criada uma classe dentro da GUI. a classe interna implementa os listeners necessários 
* recorrendo a classes anônimas - criam-se classes anônimas que implementem os listeners dos eventos a tratas. as classes anônimas são classes internas especiais. 
 

### Diálogos pré definidos 

O swing oferece um conjunto de diálogos simples, pré-definidos, para uso em interações breves com o usuário. 
* Mensagens de erro, de alerta. 
* Obtenção de uma confirmação. 
* Entrada de um único campo de texto. 

**Classe JOptionPane**

Estrutura básica: 
![](/media/Linguagem_de_Programacao-Java/Aula8/estruturaJOptionPane.PNG)


**MessageDialog** 
Exibe uma mensagem e aguarda um ok do usuário.  
![](/media/Linguagem_de_Programacao-Java/Aula8/messageDialog.PNG)


**ConfirmDialog**

Exibe uma mensagem e obtém uma confirmação (YES/NO, OK/CANCEL)  
Conjuntos de botões de opção(optionType):  

- JOptionPane.DEFAULT_OPTION  
- JOptionPane.YES_NO_OPTION  
- JOptionPane.YES_NO_CANCEL_OPTION  
- JOptionPane.OK_CANCEL_OPTION 

![](/media/Linguagem_de_Programacao-Java/Aula8/confirmDialog.PNG)


**InputDialog** 
Exibe uma mensagem e obtém um valor de entrada do usuário: 
* Campo de texto editável 
* Combo box 

![](/media/Linguagem_de_Programacao-Java/Aula8/inputDialog.PNG)

 

 
