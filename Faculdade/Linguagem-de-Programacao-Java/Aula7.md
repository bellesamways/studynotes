## Aula 7 -  Interfaces e polimorfismo 


#### As interfaces gráficas em Java 


O Java fornece uma infinidade de funcionalidades para prover comunicação humano-computado, ou melhor, para desenvolver interfaces. São fornecidas duas bibliotecas para desenvolver um GUI. Elas são: 


- java.awt : Abstract Window Toolkit (classes básicas); 


- javax.swing : Swing Componets – Fornece um conjunto de components alternativos, mais funcionais que os conjuntos fornecidos pela java.awt. 


Essas bibliotecas são fornecidas pelo JFC (Java Foundation Classes) 

 
#### Componentes atômicos 

São elementos ou componentes que não permitem conter outros elementos. Podemos citar, dentre outros, botões, labels, textFields, sliders, check boxes, scrollbars, etc. 

 

 

**JLabel** 

São rótulos estáticos que, geralmente, apresentam funcionalidades de outros componentes GUI, como por exemplo, campos de texto, ícones etc. Também, serve para apresentar um pequeno texto. As instruções são mostradas por meio de uma linha de texto: somente leitura, uma imagem ou ambas. O construtor mais elaborado é JLabel (String, Icon, int). Os argumentos representam o rótulo a ser exibido, um ícone e o alinhamento, respectivamente. Também, é possível a exibição de ícones em muito dos componentes Swing. Para JLabels, basta especificar um arquivo com extensão png, gif ou jpg no segundo argumento do construtor do JLabel, ou utilizar o método setIcon(Icon), o arquivo da imagem algumNome.xxx deve encontrar-se no mesmo diretório do programa, ou especifica-se corretamente a estrutura de diretórios até ele.  

 
 As constantes SwingConstants, que definem o posicionamento de vários componentes GUI e aqui, são apropriadas ao terceiro argumento, determinam a locação do ícone em relação ao texto. São elas:  

* SwingConstants.NORTH,  
* SwingConstants.SOUTH,  
* SwingConstants.EAST,  
* SwingConstants.WEST,  
* SwingConstants.TOP,  
* SwingConstants.BOTTOM,  
* SwingConstants.CENTER,  
* SwingConstants.HORIZONTAL,  
* SwingConstants.VERTICAL,  
* SwingConstants.LEADING,  
* SwingConstants.TRAILING,  
* SwingConstants.NORTH EAST,  
* SwingConstants.NORTH WEST,  
* SwingConstants.SOUTH WEST,  
* SwingConstants.SOUTH EAST,  
* SwingConstants.RIGHT,  
* SwingConstants.LEFT 

  
**Botões** 

Componente que tem ação parecida com um botão real, ou seja, quando clicamos ali uma ação é executada. Para se criar um desses botões, deve-se instaciar uma das muitas classes que descendem da classe AbstractButton, a qual define muito dos recursos que são comuns ao botões do swing.  

 

 

JButton: Um dos componentes mais familiares e intuitivos ao usuário. Os seus botões de comando são criados com a classe JButton e seu pressionamento, geralmente, dispara a ação especificada em seu rótulo, que também suporta a exibição de pequenas imagens. 

 

 

JCheckBox: Dá suporte a criação de botões com caixa de marcação, sendo que qualquer o número de itens pode ser selecionado. Quando um item é selecionado, um ItemEvent é gerado.   

 

 

JRadioButton: Botões de opção, se assemelham ao checkbox, quanto ao seu estado (selecionado ou não). Costumeiramente usados em grupo onde apenas um botão de opção pode ser marcado, forçando os demais botões no estado não-selecionado.  

 

 

JTextField: Compreende uma área de uma única linha que suporta a inserção ou exibição de texto. Quando o usuário digita e pressiona enter, ocorre um evento de ação.  

 

 

JPasswordField: subclasse do textfield, e acrescenta vários métodos específicos para processamento de senhas. 

 

 

JTextArea: área dimensionável que permite que múltiplas linhas de texto sejam editadas com a mesma fonte. não tem eventos de ação.  

 

 

JScrollPane: Objetos dessa classe fornecem a capacidade de rolagem a componentes da classe JComponent, quando estes necessitam de mais espaço para exibir dados. É possível configurar o comportamento do JScrollPane para um objeto com os métodos setVericalScrollBarPolicy(int) e setHorizontalScrollBarPolicy(int), valendo-se das mesmas constantes como argumentos.  

 
 

JSlider: é um marcador que desliza entre um intervalo de valores inteiros, podendo selecionar qualquer valor de marca de medida em que um marcador repouse. (restringir valores de entrada de em um app, por exemplo.) 

 
 

JComboBox: assemelha-se a um botão, mas quando clicado ele abre uma lista de valores ou opções.  

 
 

**Menus**

Instanciados a partir da classe JMenu, são anexadas a barra de menus com o método add(JMenu) de JMenuBar. A classe JMenuBar fornece os métodos necessários ao gerenciamento da barra onde os menus são anexados. A ordenação dos mesmos depende da ordem em que foram adicionados, sendo que são "empilhados" horizontalmente da esquerda para a direita. A classe JMenuItem capacita a criação de itens de menu que devem ser anexados ao menu.  