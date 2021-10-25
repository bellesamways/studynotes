# Aula 4 - Interface Gráfica Avançada

## ScrollView

É muito comum que telas de aplicativos tenham muitos componentes, dificultando a exibição de todos em uma única tela. Por isso, o componente ScrollView permite que barras de rolagens sejam apresentadas automaticamente, caso sejam necessárias para exibição de todos os componentes na mesma tela.

Embora o ScrollView possua vários métodos, implementá-los é bastante simples. Apenas precisamos nos lembrar que esta classe somente pode possuir um componente-filho e que as barras de rolagens serão inseridas automaticamente quando a View ultrapassar o tamanho da tela física.

Deve-se inserir dentro do ScrollView um ViewGroup que será responsável por conter todos os demais componentes.

O emprego do ScrollView é demonstrado abaixo:

```xml

<?xml version="1.0" encoding="utf-8"?>
            <ScrollView xmlns:android="//schemas.android.com/apk/res/android"
                 android:layout_width="fill_parent" android:layout_height="wrap_content" >
                 <LinearLayout
                 android:layout_width="fill_parent" android:layout_height="fill_parent"
                 android:orientation="vertical" >
                 <RadioButton
                     android:id="@+id/radioButton2" android:layout_width="wrap_content"
                     android:layout_height="wrap_content" android:text="RadioButton 1" />
                 <RadioButton
                     android:id="@+id/radioButton1" android:layout_width="wrap_content"
                     android:layout_height="wrap_content" android:text="RadioButton 2" />
                 <Button
                     android:id="@+id/button4" android:layout_width="match_parent"
                     android:layout_height="wrap_content" android:text="Botão 8" />
                 <CheckBox
                     android:id="@+id/checkBox1" android:layout_width="wrap_content"
                     android:layout_height="wrap_content" android:text="CheckBox" />
                 <!--Foram omitidos neste ponto vários outros componentes -->
            </LinearLayout>
            </ScrollView>

```

## Gerenciadores de Layouts aninhados

O Android permite a implementação de layouts aninhados, pois os Gerenciadores de Layouts são classes Views e, como estudado anteriormente, podem conter tanto Views simples (Widgets) como layouts (ViewGroups).

Assim, é possível implementar telas muito mais elaboradas apenas combinando as características de cada tipo de gerenciador de layouts.

## Listas

Sem sombra de dúvidas, um dos componentes mais implementados no Android é o ListView.

Normalmente, é utilizado quando precisamos exibir uma grande quantidade de dados na forma de lista, que pode possuir rolagem (scroll).

Podemos otimizá-lo com textos e imagens, tratar eventos de clique e de seleção.
