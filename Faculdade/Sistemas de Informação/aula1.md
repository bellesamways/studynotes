# Aula 1

Sistema = conjunto de elementos inter-relacionados, cada qual desempenhando uma função, para, de forma integrada e coordenada, contribuir e garantir que o objetivo do sistema seja atingido.

![Sistema de Informação](/media/realimentação.png)

**Entrada** são os insumos de que o sistema precisa para atingir o seu objetivo.

**Processamento** é a execução dos procedimentos necessários ao bom funcionamento do sistema. Propicia a conversão da entrada bruta em forma mais útil e apropriada.

**Saída** é a apresentação do resultado ao ambiente externo gerado pelo sistema.

**Realimentação (ou feedback)** é a parte da saída do sistema que retorna ao próprio sistema com o objetivo de refinar ou corrigir os dados de entrada ou o processamento. É parte da saída produzida pelo sistema que informa sobre seu comportamento.

**Controle** refere-se ao monitoramento e avaliação do feedback, determinando se o sistema está atingindo o seu objetivo.

**Dado x Informação**

Dado: fato isolado em sua forma primária que não tem valor intrínseco.

Informação: conjunto de fatos (dados) organizados (processados) de tal forma que tenham valor agregado em si.

![Dado x Informação](/media/dados_informação.png)

## Sistema de informação

sistema cuja finalidade é PROVER INFORMAÇÃO a alguém na medida certa. Informação -> útil para quem recebe, possibilitando tomada de decisão.

**Sistemas de processamento de transação:** sistemas automatizaram os processos rotineiros,  úteis não só na redução de custos mas também em um melhor controle e eficiência das operações de rotina. Os SPTs provêm informações de cunho operacional, ajudando no melhor controle das operações.

**Sistemas de informação gerencial:** para a gestão das atividades a que se destinavam. Os SIGs provêm informações gerenciais aos supervisores, gerentes e cargos correlatos, apoiando as decisões que se fazem necessárias no dia a dia.

**Sistemas estratégicos:** visam a atender à demanda da direção das empresas (diretores, vice-presidentes e presidentes), ajudando a traçar as diretrizes estratégicas da organização.

![Sistema de informação](/media/sistema_informacao_piramide.png)
![Sistema de informação](/media/sistema_informacao_tabela.png)

## Tecnologia da informação

**Conjunto de recursos tecnológicos e computacionais para a geração e uso da informação**, ou seja, o  conjunto de recursos não humanos que desempenha uma ou mais tarefas de processamento das informações do SI tal como coletar, transmitir, armazenar, recuperar, manipular e exibir dados. Em sistemas de informação, a tecnologia da informação é fundamental, pois é o meio utilizado para alcançar os fins desejados.

    Tecnologia de informação (TI) é a infra-estrutura para os sistemas de informação (SI).

**Benefício da TI:** melhorar a qualidade e a disponibilidade de informações; aperfeiçoa ou adiciona eficiência; é um facilitador, não cria diretamente a satisfação.

**SI e TI não são sinônimos.**

## Características básicas dos SI

- Os sistemas estão inseridos em um contexto complexo; sofrem influẽncia do ambiente em que estão inseridos.

![Contexto dos SI](/media/contexto_sistemas_informacao.png)

- Os sistemas estão organizados em níveis hierárquicos. Os subsistemas são partes de um sistema maior que podem ser formados por outros subsistemas (hierarquia de níveis).

![Hierarquia dos SI](/media/hierarquia_sistemas_informacao.png)


### Teoria geral dos sistemas:

- Analisar a natureza dos sistemas e a relação entre suas partes;
- Identificar leis, propriedades e princípios característicos dos sistemas em geral;
- **Possui duas características relevantes:**
    - **Funcionalismo:** cada parte deve desempenhar uma parte da função maior
    - **Holismo:** o todo não é a simples soma das partes, o próprio sistema só pode ser explicado como um todo. Seus subsistemas e seus elementos estão inter-relacionados.

### Classificação de sistema:

- **Aberto ou fechado**
    - **Aberto:** interage com o seu ambiente; sofrem influências (positivas ou negativas) e influenciam o meio ambiente com suas ações.
    - **Fechado:** não possui interação com o ambiente.
- **Simples ou complexo**
    - **Simples:** possuem poucos componentes; relacionamento entre eles é simples e direto.
    - **Complexo:** muitos elementos altamente relacionados e interconectados.
- **Estável ou dinâmico**
    - **Estável:** mudanças no ambiente resultam em pouca ou nenhuma alteração no sistema.
    - **Dinâmico:** sofre rápidas e constantes mudanças em decorrência de mudanças no ambiente.
- **Adaptável ou não adaptável**
    - **Adaptável:** capaz de sofrer mudanças em resposta a mudanças no ambiente.
    - **Não adaptável:** não é capaz de mudar em resposta a mudanças no ambiente.
- **Permanente ou temporário**
    - **Permanente:** existe por um período de tempo relativamente longo.
    - **Temporário:** existe por um período de tempo relativamente curto.

### Propriedades fundamentais dos sistemas:
- **Entropia:** tendência de todos os sistemas fechados apresentarem, com o tempo, estado caótico ou aleatório, caminhando para a desordem e consequentemente declínio.
- **Equifinalidade:** sistemas abertos podem alcançar um estado constante de equilíbrio, de modo que não chegue a um repouso estático; certo estado final pode ser atingido de muitas maneiras e de vários pontos de partida diferentes.
- **Mecanismo de feedback:** correspondem a respostas a um descontrole externo.
- **Homeostase (autorregulação):** tendência ao equilíbrio, objetivando manter a constância durante um período de tempo.
- **Diferenciação e interação:** sistema deve ser adaptável e ser capaz de efetuar mudanças e reordenar-se, em resposta às pressões ambientais.
- **Hierarquias:** todo sistema compõe-se de sistemas de ordem inferior que fazem parte de um sistema de ordem superior.
- **Fronteiras:** separação entre o sistema e o meio ambiente e fixa o domínio em que deve ocorrer as atividades dos subsistemas. Toda organização possui fronteira, ou seja, uma determinação de seu campo de ação.
- **Inputs e outputs:** transforma um determidado tipo de entrada (input) em determinado tipo de saída (output). A ideia é definir para cada output desejado, prever o input necessário.

Principais componentes da plataforma de desenvolvimento Android:

- Activity: é um componente de aplicativo que fornece uma tela com a qual os usuários podem interagir para fazer algo, como discar um número no telefone, tirar uma foto, enviar um e-mail ou ver um mapa. Cada atividade recebe uma janela que exibe a interface do usuário. Geralmente, a janela preenche a tela, mas pode ser menor do que a tela e flutuar sobre outras janelas.

- Intent: é um objeto de mensagem que pode ser usado para solicitar uma ação de outro componente de aplicativo.

- Service: é o componente responsável pelo processamento em segundo plano associado a uma aplicação.

- Broadcast Receiver: são componentes responsáveis por receber e tratar eventos (broadcasts) provenientes do sistema ou de outras aplicações. É sempre executada em segundo plano.

- Content Provider: são componentes responsáveis por prover às aplicações o conteúdo que elas precisam para funcionar, ou seja, os dados. Permitem o compartilhamento de dados entre aplicações, centralizam as rotinas de armazenamento e recuperam em um único local.