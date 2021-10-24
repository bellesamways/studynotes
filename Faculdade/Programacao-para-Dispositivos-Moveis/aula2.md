# Aula 2 - Activity e Intent

## Estrutura de um projeto Android

O Android Studio pode abrir um projeto de cada vez. Cada projeto pode possuir um ou mais módulos.

![Estrutura de um projeto Android](/media/programacao-dispositivos-moveis/estrutura-android-studio.png)

Aqui temos os arquivos do diretório raiz do projeto:

![diretório raiz do projeto](/media/programacao-dispositivos-moveis/diretorio-raiz-android-studio.png)

Aqui temos os arquivos do módulo app:

![Arquivos do módulo app](/media/programacao-dispositivos-moveis/arquivos-modulo-app.png)

Detalhes de alguns tipos de arquivos:

### Arquivo androidmanifest.xml

Considerado um dos principais arquivos de sua aplicação. É nele que são descritas informações essenciais à execução de seu projeto como, por exemplo:

<ul>
 <li>Nome do pacote utilizado;</li>
 <li>Nome das Activities;</li>
 <li>Permissões que o aplicativo possui;</li>
 <li>Versão mínima da API Android.</li>
<ul>

![Arquivo androidmanifest.xml](/media/programacao-dispositivos-moveis/arquivo-androidmanifest.png)

### Arquivo activity_main.xml

Esse arquivo, por default, possui este nome. Porém, podemos escolher um nome mais adequado.
Nesse arquivo são definidas as configurações para criação do layout da tela.

![Arquivo activity_main.xml](/media/programacao-dispositivos-moveis/arquivo-activity-main.png)

### Arquivo strings.xml

Esse arquivo centraliza as mensagens de seu aplicativo. Facilita muito, inclusive, a internacionalização do aplicativo.

![Arquivo strings.xml](/media/programacao-dispositivos-moveis/arquiv-strings.png)

### Classe R

Esse arquivo possui as referências para acessar os recursos de seu projeto.
É gerada automaticamente pelo compilador. É recomendável que essa classe não seja alterada manualmente.

![Arquivo Classe R.xml](/media/programacao-dispositivos-moveis/arquivo-classer.png)

## Activity

Muito similar ao JFrame do J2SE, a Activity é responsável por construir uma tela em Android, bem como tratar os eventos gerados por ela. Toda aplicação Android deve implementar ao menos um Activity, podendo chamar outras Activities.

O Android é responsável por gerenciar o ciclo de vida dos Activities. Para tanto, faz uso do conceito de pilha, chamada de “Activity Stacks” (pilha de atividades). Toda Activity ao ser executada é inserida no topo dessa pilha. A Activity anterior é parada e move-se para baixo da pilha.

O Android pode até mesmo encerrar Activities, se precisar de recursos. Neste caso, ele verifica a pilha de atividade para determinar a prioridade das atividades e quais podem ser fechadas.

Exemplo de uma pilha de atividades:

![Activity stack](/media/programacao-dispositivos-moveis/activity-stack.png)

### Ciclo de vida activity

![Ciclo Activity stack](/media/programacao-dispositivos-moveis/ciclo-activity.png)

Os principais métodos do ciclo de vida Activity são:

<ul>
<li>
onCreate(): primeira função executada quando a Activity é criada. Tem por responsabilidade carregar os layouts XML, inicializar os objetos, variáveis e outras operações de inicialização. É importante lembrar que é executada somente uma vez.</li><li>
onStart(): é executado antes da Activity ficar visível na tela do dispositivo, podendo ser chamado após os métodos **onCreate()** ou **onRestart()**.</li><li>
onResume(): representa o estado que a Activity está executando. É chamada logo após o evento onStart.</li><li>
onRestart(): é chamado imediatamente após ao método onStart(), quando uma Activity que estava parada volta ao foco.</li><li>
onPause(): é chamado sempre que a tela da Activity fechar. Isto ocorre quando uma outra Activity (da sua aplicação ou não) ganhar o foco.
onStop(): é chamado após o método **onPause()**, quando a Activity não está mais visível e está sendo encerrada.</li><li>
onDestroy(): é chamado antes da Activity ser destruída e logo após será liberada a memória.
</li>
</ul>

No diagrama abaixo, referente ao ciclo de vida da Activity os 3 níveis:

![Niveis Ciclo Activity](/media/programacao-dispositivos-moveis/niveis-ciclo-activity.png)

<ol>
<li>
**Entire lifetime**: tempo de vida completo. Ocorre desde a primeira chamada ao método onCreate() até a chamada do método onDestroy(), os quais são executados apenas uma vez durante o ciclo de vida da Activity. 
</li>
<li>
**Visible lifetime**: tempo de vida visível. Ocorre entre uma chamada do método onStart() e a chamada correspondente do método onStop(). A activity pode estar no topo da pilha (visível para o usuário) ou em segundo plano. 
</li>
<li>
**Foreground lifetime**: tempo de vida no topo da pilha. Ocorre entre uma chamada no método onResume() e a chamada correspondente do método onPause(). A Activity está no topo da pilha e interagindo com o usuário. 
</li>
</ol>
</br>

### Classe Intent

Cada Activity corresponde a uma tela de nossa aplicação no Android.

Devido à limitação de tamanho de nossos dispositivos, é muito comum distribuirmos componentes por várias telas visando facilitar o uso da aplicação.

Entre os vários componentes fundamentais, na programação de aplicativos Android (como Activities, Services e BroadCast Receivers), a Intent possibilita realizar a ligação, em tempo de execução, de componentes separados (por exemplo, chamar Activities diferentes).

Em outras palavras, podemos dizer que uma Intent nada mais é do que a intenção da aplicação em realizar uma determinada tarefa.

Trata-se de uma intenção, ou seja, não necessariamente será executada, pois depende da permissão do dispositivo.

A Intent envia ao sistema operacional o equivalente a uma mensagem (broadcast). Este receberá a chamada e, dependendo do conteúdo, tomará as providências necessárias. Como exemplo, podemos citar: Iniciar uma nova Activity; Iniciar Bluetooth do aparelho; Ligar o GPS (Global Positioning System); Efetuar uma ligação telefônica; Abrir o programa de envio de SMS (Short Message Service); Chamar o navegador Web; Enviar mensagens para o Sistema Operacional.

Uma Intent é basicamente um conjunto de dados que possui informações de interesse para os componentes que a recebem e também para o Android.

Deve conter:

<ul>
  <li>Componente</li>
  <li>Ação</li>
  <li>Dados</li>
  <li>Categorias</li>
  <li>Extras</li>
  <li>Flags</li>
</ul>

Podemos definir ações específicas de nossa aplicação, biblioteca ou ações pré-definidas conforme a tabela abaixo:

| Constante               | Component          | Ação                                                                                 |
| ----------------------- | ------------------ | ------------------------------------------------------------------------------------ |
| ACTION_CALL             | activity           | Inicia uma chamada de telefone.                                                      |
| ACTION_EDIT             | activity           | Mostra dados para o usuário editar.                                                  |
| ACTIVE_MAIN             | activity           | Inicia a atividade que está marcada como inicial em modo vazio e com nenhum retorno. |
| ACTIVE_SYNC             | activity           | Sincroniza dados no servidor a partir do dispositivo móvel.                          |
| ACTIVE_BATTERY_LOW      | broadcast receiver | Mostra um aviso que a bateria está baixa.                                            |
| ACTIVE_HEADSET_PLUG     | broadcast receiver | Mostra que um fone de ouvido foi plugado no dispositivo ou desplugado.               |
| ACTIVE_SCREEN_ON        | broadcast receiver | A tela foi ligada.                                                                   |
| ACTIVE_TIMEZONE_CHANGED | broadcast receiver | As configurações da zona de tempo foram mudadas.                                     |

Aqui temos as constantes pré-definidas:

| Constante           | Significado                                                                                                                            |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| CATEGORY_BROWSABLE  | A atividade alvo pode ser chamada de maneira segura pelo navegador para mostrar dados referenciados por um link (imagem ou e-mail etc) |
| CATEGORY_GADGET     | A atividade pode ser embarcada dentro de outra atividade que hospeda gadgets.                                                          |
| CATEGORY_HOME       | A atividade mostra a tela home. A primeira tela que o usuário vê quando o dispositivo é ligado ou quando a tecla HOME é pressionada.   |
| CATEGORY_LAUNCHER   | A atividade pode ser a atividade inicial ou uma tarefa e é listada no tipo de aplicação launcher.                                      |
| CATEGORY_PREFERENCE | A atividade alvo é o painel de preferencias.                                                                                           |

### Tipos de Intents

**Explícitas**: como determina o componente pelo nome, é usada para passagem de mensagens no próprio app.

**Implícitas**: é enviada ao sistema operacional e pode ser tratada por componentes em outros apps. Nesse caso, a definição de quem tratará a intent é feita. O conteúdo do objeto intent é comparado com alguns filtros chamados "intent filters".

### Intent filter

Um Intent Filter informa ao sistema quais Intents um certo componente pode tratar. Um componente pode ter uma ou mais Intent Filters.

![Intent Filter](/media/programacao-dispositivos-moveis/intent-filter.png)

Com relação ao tipo implícito, as Intents serão entregues se um dos filtros atender aos critérios da Intent.

Já no caso da explícita, será entregue diretamente ao componente designado, não importando o filtro, pois nem chega a consultá-lo.
