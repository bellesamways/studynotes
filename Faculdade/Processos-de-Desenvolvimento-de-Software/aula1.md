# Aula 1 - Conceitos de Software e Linguagem de Programação

**O que é software?** É um conjunto integrado de programas de Computador.

**O que é um programa de computador?** É um conjunto de instruções que descreve, passo a passo, uma tarefa que deve ser realizada pelo hardware.

**Paradigma:** classificações para as linguagens de programação, avalia como as instruções são compostas e organizadas para formar o programa.

**1. Imperativo:** elementos de código em formato de blocos que se interligam através de três tipos de instrução, da chamada Programação Estruturada.

- a) **Sequência:** As instruções são organizadas de forma sequencial (tarefa 1 finaliza, entra tarefa 2).

- b) **Seleção:** Onde as instruções podem ser executados baseadas na avaliação de uma condição (IF (Condição=V) THEN Sequencia1 ELSE Sequencia2

- c) **Iteração:** Onde as instruções podem ser repetitivas até uma condição ser atingida.

**2. Orientada a Objeto (OO):** elementos de código em formato de objetos que se interligam. Um objeto é composto de atributos (dados) e métodos (ações). Os objetos são agrupados em classes.

- a) **Classe:** tipo de objeto
- b) **Atributos:** variáveis que estão dentro de cada objeto da classe
- c) **Método:** ação que a classe pode realizar

Exemplo: Classe ALUNO.

Atributos: Nome, Matricula, Telefone, endereço

Métodos: Incluir Aluno, Matricular em curso, Incluir Disciplina

## Software básico

São softwares que permitem a operação e programação de computador, como as linguagens de programação e o sistema operacional. Exemplos de sistemas operacionais: Windows, MacOs, Ios, Android

![software básico](/media/processos_dev_software/software_basico.png)

- **Monotarefa:** Executa somente um processo de cada vez.
- **Monousuário:** Somente é permitida a utilização de um usuário de cada vez.
- **Multitarefa:** Os processos são compartilhados e enfileirados a espera do processador. É distribuído de modo que pareça ser executado simultaneamente.
- **Multiprocessamento:** Distribui para mais de um processador.
- **Multiusuário:** Vários usuários utilizam ao mesmo tempo.

## Software aplicativo

O software aplicativo, como diz o nome, revela alguma utilidade (aplicativo) ao usuário, como por exemplo: editores de texto, planilhas eletrônicas, folha de pagamento, contas a pagar, aplicativos diversos de celulares e etc.

![software aplicativo](/media/processos_dev_software/software_aplicativo.png)

### Características e aplicações do software

O software pode ser classificado de acordo com a sua forma de cópia e distribuição (licença de uso). Em geral, o software pode ser:

1.  **Software gratuito ou freeware:** Programa de computador cujo uso não implica o pagamento de licença de uso. O Freeware pode ser copiado e distribuído gratuitamente. O Freeware pode ser utilizado sem pagar, mas o código fonte não é disponibilizado, logo o freeware não pode ser modificado. Assim sendo o freeware só pode ser usado da forma como é disponibilizado.
1.  **Software livre:** Programa de computador cuja utilização, cópia e distribuição não possui restrição. É comum o código fonte estar disponível para manuseá-lo, e dessa forma o software pode ser modificado, por quem desejar, sem que seja necessária a permissão ou que se pague ao autor.
1.  **Comercial:** Programa onde deve-se pagar um valor para sua aquisição e/ou uso.
1.  **Adware:** Programa de computador que executa automaticamente algum tipo de publicidade após sua instalação ou durante sua utilização.
1.  **Demo:** Fração de um programa. Funciona como material promocional para dar a oportunidade do produto ser avaliado. É restrito de suas funcionalidades apenas para teste.
1.  **Trial:** Programa semelhante ao demo, mas com funcionalidades disponíveis por tempo determinado.
1.  **Shareware:** Programa de computador que possui limitações de tempo e/ou funcionalidades. Ao final do tempo estabelecido, o programa pode requisitar o pagamento para uso do software completo ou pode continuar rodando sem todas as suas funcionalidades ou, ainda, interromper o seu uso.

#### O processo de desenvolvimento de software

![processo de desenvolvimento de software](/media/processos_dev_software/processo_desenvolvimento_software.png)

- **Concepção:** fase onde o sistema é concebido e avaliada a sua viabilidade (técnica, econômica, tempo). Caso viável o desenvolvimento segue nas fases seguintes e caso contrário é interrompido.
- **Requisitos:** Em muitos modelos de processos de desenvolvimento, a fase de requisitos pode estar junta com a de Analise, mas a finalidade é identificar as necessidades dos usuários para definir os requisitos do sistema.
- **Análise:** fase de estudo, onde é definido O QUE o sistema deve fazer, independente da tecnologia que venha a ser usada. Define-se, dentre outras coisas as funcionalidades que o sistema precisa ter.
- **Projeto:** onde define-se as tecnologias a serem usadas: linguagem de programação e banco de dados. É também a fase de definição da arquitetura do software e seus respectivos elementos. E fase do COMO fazer o software.
- **Codificação:** é a escrita de cada programa que vai compor o sistema, na linguagem de programação selecionada. Depende tecnicamente da qualidade do programador para gerar códigos inteligíveis e de fácil manutenção.
- **Testes:** Verificação de erros no sistema e apuração se o mesmo executa as ações previstas e necessárias a seus usuários. Abrange um conjunto de testes em diferentes momentos da fase de codificação. Deve-se testar, inicialmente, cada programa separadamente e depois o conjunto integrado de programas.
- **Homologação:** fase onde os usuários atestam que o software atende (ou não) as suas necessidades, liberando-os (ou não) para uso.
- **Implantação:** fase onde o sistema é posto em uso, no ambiente do usuário, o que requer instalação dos softwares , treinamento a usuários e acompanhamento do uso por um período de tempo (acordado previamente, em contrato, preferencialmente).
- **Manutenção:** uma vez implantado, o sistema precisa sobreviver ao longo dos anos, adequando-se as mudanças da empresa e do contexto onde a mesma esta inserida.

O **RUP** é um processo de desenvolvimento de software. Ele engloba as ações necessárias para transformar um conjunto de requisitos do cliente em um sistema de software. O RUP combina os ciclos de vida iterativo e incremental de forma que cada entrega do software em um ciclo agrega mais valor ao produto em relação ao ciclo anterior. A grande vantagem em desenvolver um grande sistema usando um processo incremental é a diminuição do risco, pois cada entrega pode ser avaliada e o passe seguinte alinhado com os objetivos do cliente, que nem sempre permanecem constantes durante o desenvolvimento de um projeto.

Suas fases são:

1.  Iniciação
1.  Elaboração
1.  Construção
1.  ransição
