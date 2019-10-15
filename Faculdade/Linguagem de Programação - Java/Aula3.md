## Aula 3 - INTRODUÇÃO AS INTERFACES GRÁFICAS

#####Introdução as IDEs
![Introdução as IDEs](/media/Linguagem_de_Programacao-Java/Aula3/IntroducaoIDEs.png)

##### Introdução a concepção de interfaces gráficas
A interface gráfica com o usuário (GUI) fornece a um programa um conjunto consistente de componentes intuitivos, familiarizando o usuário com as diversas funções e diminuindo o tempo de aprendizado da nova ferramenta. As GUIs são construídas a partir de componentes GUI, que são objetos com o qual o usuário interage através dos dispositivos de entrada, ou seja, o mouse, o teclado, a voz, etc.

##### Criação de Interfaces Gráficas

As classes necessárias para criação de componentes gráficos, bem como para fornecer-lhes funcionalidade, estão agrupadas em dois grandes pacotes: **java.awt (pacote de núcleo) e javax.swing (pacote de extensão)**. Os dois pacotes definem componentes com peculiaridades distintas e que serão discutidas a seguir.

**Componentes swing**: maioria dos componentes Swing é escrita, manipulada e exibida completamente em Java, estes são conhecidos como componentes Java puros. Maior nível de portabilidade e flexibilidade. Os nomes de tais componentes recebem um “J”, como, por exemplo: JLabel, JButton, JFrame, JPanel, etc.

**Componentes básicos**: mostra a maioria das classes que compõem o Java Swing e mostra também a relação entre as classes AWT (claro) e as classes Swing (escuro).
![Fluxograma de relação entre as classes](/media/Linguagem_de_Programacao-Java/Aula3/componentesBasicos.png)

##### Painéis

Áreas que comportam outros componentes, inclusive outros painéis. São criados com a classe JPanel, que é derivada da classe Container. A classe JPanel não tem painel de conteúdo como JFrames, assim, os elementos devem ser diretamente adicioandos ao objeto painel.
```Java
import javax.swing.*;

public class Frm01 {
    public void criaTela(){
        JFrame f = new JFrame();
        f.setSize(290, 100);
        f.setTitle("Cadastro");
        f.setLocation(10, 10);
        f.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        f.setVisible(true);
    }
}
```
```Java
public class TestaFrm01 {
    public static void main(String []args){
        Frm01 tela = new Frm01();
        tela.criaTela();
    }
}
```
O método setDefaultCloseOperation()também pode ser executado com outras constantes como argumento

**DISPOSE_ON_CLOSE** - Destróia a janela
**HIDE_ON_CLOSE** - Apenas fecha a janela
**DO_NOTHING_ON_CLOSE** - Desabilita opção
**EXIT_ON_CLOSE** - Encerra a aplicação