# Aula 1 - Princípios da segurança e o ciclo de vida da informação

### Dado e informação 

O dado pode ser considerado o valor de determinada medida sem uma contextualização e, portanto, sem valor para ser aplicado ou tratado. No momento em que um dado é contextualizado, ou seja, é atribuído a um contexto ou a uma situação, torna-se uma informação, consequentemente obtendo valor.

Informação pode ser definida como um dado contextualizado no qual existe uma percepção de valor. Dessa forma, é necessário haver uma atenção quanto à sua preservação.

### Ciclo de vida da informação 

Criação >> Transporte >> Manuseio >> Descarte 

Após a primeira etapa (criação), o dado pode ser transportado ou manuseado. Esta figura representa o transporte antes do manuseio por tal procedimento ser o mais comum nesses casos, porém é perfeitamente possível que ele seja manuseado anteriormente. Na etapa final, a informação é descartada. 

Durante todas essas etapas, a informação deve ser protegida. Seu vazamento em quaisquer etapas pode provocar problemas em vários aspectos. 

A informação, que é o dado contextualizado, precisa de proteção em todo o seu ciclo de vida. A partir dos exemplos citados, conseguimos entender a necessidade de **sempre** estabelecer uma proteção adequada dela em qualquer etapa do seu ciclo de vida. 

No caso do transporte de mídias magnéticas contendo informações sigilosas de usuários de determinada empresa, por exemplo, uma boa proteção é o emprego da **criptografia**. Esta chave é usada para embaralhar (criptografar) e desembaralhar (decriptografar) as informações.

**Criptografia pode ser definida como o embaralhamento das informações por meio de uma sequência de dados que utiliza uma chave e um algoritmo.** 

Quando a mesma chave é usada nas duas etapas, a criptografia é dita **simétrica**; quando são usadas chaves distintas, ela é **assimétrica**. Vejamos seus dois tipos nas figuras a seguir:

![Criptografia Simétrica](media/introducao-a-seguranca-da-informacao/cripto-simetrica.png)

![Criptografia Assimétrica](media/introducao-a-seguranca-da-informacao/cripto-assimetrica.png)

Devemos observar que a **proteção** e a **facilidade** caminham em direções contrárias. Por isso, o processo de compactar com senha gera um aumento de tempo no manuseio da informação, pois ele sempre torna necessária a tarefa de descompactar e compactar para tratar a informação. 

Seu descarte deve ser realizado de forma padronizada, já que o propósito é evitar a recuperação de suas informações.

![Triturador](media/introducao-a-seguranca-da-informacao/triturador.png)

### Aspectos da segurança da informação 

Dos aspectos da informação, seus três principais requerem cuidados especiais:

- Confidencialidade;
- Integridade;
- Disponibilidade.

![Informacao](media/introducao-a-seguranca-da-informacao/informacao.png)

1) Confidencialidade: Capacidade do acesso à informação apenas por quem possui autorização.

2) Integridade: Possibilidade de alteração da informação por pessoas ou sistemas autorizados 

3) Disponibilidade: Faculdade de a informação poder ser acessada, em qualquer tempo, por pessoas ou sistemas autorizados para tal.

Portanto, a **segurança da informação** pode ser definida como as atividades, os procedimentos e as metodologias que objetivam a proteção da informação, principalmente no que tange à confidencialidade, à integridade e à disponibilidade (CID).

Os seguintes aspectos também são considerados importantes:

1) Autenticidade: Assegura que a informação foi gerada por pessoa ou sistema autorizado para isso.

2) Legalidade: Trata-se do alinhamento da informação e/ou dos processos com normas, portarias, leis e quaisquer outros documentos normativos, cada um na sua respectiva esfera de atribuição e abrangência.

3) Não repúdio: Também conhecido como **irretratabilidade**, ele está relacionado ao fato de o emissor negar a autoria de uma informação divulgada.

Juntos, todos eles compõem os principais aspectos empregados pelos controles – ou pelas ferramentas que proporcionam a segurança da informação – para proteger a informação.

Resumo dos aspectos da segurança:

**Disponibilidade**: Capacidade de a informação poder ser acessada, em qualquer tempo, por pessoas ou sistemas autorizados para tal. 

**Irretratabilidade**: Está relacionada ao emissor negar a autoria de uma informação divulgada. 

**Confidencialidade**: Capacidade do acesso à informação apenas por quem possui autorização. 

**Autenticidade**: Assegura que a informação foi gerada por pessoa ou sistema autorizado para isso. 

**Integridade**: Possibilidade de alteração da informação por pessoas ou sistemas autorizados. 

**Legalidade**: Alinhamento da informação ou dos processos com normas, portarias, leis e quaisquer outros documentos normativos. 

### Segurança física 

Tendo como exemplo de roubo de dados no seu transporte. Mesmo que eles estivessem criptografados, a ação poderia ocorrer da mesma forma, pois ela foi uma consequência de vulnerabilidades na segurança física das mídias em questão. 

Aspecto integridade: A informação foi totalmente impactada, pois a mídia poderia ser destruída. 

X

Aspecto Confidencialidade: Dependeria, por exemplo, da informação armazenada ter ou não algum controle de proteção, como, por exemplo, a criptografia. 

A família de normas ABNT ISO/IEC 27.000 divide a segurança física em dois aspectos: um é relacionado aos equipamentos e outro, ao ambiente. 

A segurança da informação age dessa forma. Ela é entendida como camadas justapostas que permitem à informação ficar cada vez mais protegida, como, por exemplo, uma cebola e suas camadas. 

Quanto ao ambiente, em uma instalação empresarial, por exemplo, é possível observar as camadas de segurança físicas e, a partir daí, estabelecer um paralelo com a imagem da cebola. 

![Informação](media/introducao-a-seguranca-da-informacao/informacao-cebola.png)

Ao nos aproximarmos de uma instalação, alcançamos a cancela para automóveis, que, normalmente, conta com dois seguranças. Sua função é solicitar alguma identificação ou verificar se o veículo possui algum selo de identificação. 

Normalmente, esse selo é único para aquela instituição. Em alguns casos, essa verificação pode ser feita de forma automatizada com alguma tecnologia de emissão de sinal de baixa frequência, como o RFID. 

Após a ultrapassagem dessa primeira barreira (camada mais externa à nossa cebola de segurança), geralmente existe mais uma etapa: catraca e elevador. Ela está vinculada a algum controle biométrico ou de crachá. O RFID novamente surge como um exemplo. 

 

Físicos, esses controles são justapostos, permitindo que a vulnerabilidade de um deles possa ser recoberta por outro controle. Isso funciona de forma similar nas salas de servidores, data centers e salas-cofres, criando camadas de segurança que dificultam o acesso físico ao servidor. 

Outro aspecto que deve ser levado em consideração é a proteção contra ameaças da natureza, como enchentes, incêndios e outras calamidades provocadas pela natureza e/ou pelo homem. 

Tendo isso em vista, certos controles de monitoramento e prevenção devem ser instalados e controlados. 

 

O cabeamento e o acesso à rede externa (internet), bem como ao fornecimento de energia, são fatores fundamentais nesse processo. Como eles dependem de um fornecimento feito por terceiros, certos aspectos contratuais e de redundância precisam ser estabelecidos. 

Além disso, políticas e instruções normativas devem ser instituídas, treinadas e simuladas visando à prontidão. Nesse sentido, é razoável haver uma redundância no fornecimento de rede (internet), bem como uma independência física desse fornecimento no que tange ao tipo de conexão estipulada. 

 

Os maiores computadores do mundo são organizados em uma lista conhecida como Top 500 (top500.org). Pelo custo e poder computacional deles, esses equipamentos requerem uma série de recursos de proteção. 

Maior recurso computacional do Brasil, o supercomputador Santos Dumont consta na referida lista. Para prover os recursos necessários de segurança, uma série de medidas foi tomada e, em seguida, publicada no Youtube. 

 

### Segurança Lógica 

 

Em adição às medidas de segurança física, há as de segurança lógica, que correspondem às medidas baseadas em software. Dessa lista, podemos destacar as senhas, as listas de controle de acesso, a criptografia, e o firewall. 

 

Repetindo o padrão apresentado anteriormente, esses mecanismos estão justapostos; com isso, a demanda de uma camada pode criar uma adicional a outra que possua alguma vulnerabilidade particular. 

 

Como exemplo disso, existem no próprio equipamento controles de acessos biométricos, como a leitura de digital e o reconhecimento facial. Esses sistemas de controle biométricos são caracterizados pela captura da geometria humana, a qual, em grande parte, difere em cada pessoa. 

 

Atualmente, os leitores de digitais têm dado espaço para o reconhecimento facial pela disseminação dos sensores e da tecnologia empregada. Há diversas APIs disponibilizadas para uso gratuito e comercial, como a do Amazon Rekognition. Esses controles atuam na proteção da confidencialidade da informação. 

A criptografia corresponde ao conjunto de técnicas que permite o embaralhamento de dados por intermédio do uso de chaves e de algoritmos computacionais baseados em funções matemáticas. Essas funções propiciam, em linhas gerais, a presença de duas grandes classes de algoritmos: os **simétricos** e os **assimétricos**. 

 

#### Criptografia simétrica 

 

Utiliza funções matemáticas mais simples e uma única chave para criptografar e decriptografar. Esta classe de algoritmos é composta por, entre outros exemplos, Cifra de César, Blowfish, Twofish e Rijnadel. Graças a esse controle, é possível assegurar a confidencialidade da informação.

| Algoritmo | Tamanho da chave |
| - | - |
| AES (Rijnadel) | 128, 192 e 256 bits |
| Twofish | 128, 192 e 256 bits |
| Serpent | 129, 192 e 256 bits |
| Blowfish | 32 e 448-bits |
| RC4 | 40-128 bits |
| 3DES (baseado no DES) | 168 bits |
| IDEA | 128 bits |

#### Criptografia assimétrica 

 

Caracteriza-se por algoritmos que normalmente envolvem técnicas matemáticas mais sofisticadas, como a fatoração de números grandes e o logaritmo discreto. 

Esta família emprega duas chaves: uma é utilizada para cifrar; a outra, para decifrar. Essas chaves são conhecidas como: 

 

Pública: Normalmente, ela fica disponibilizada em um servidor de confiança. 

 

X 

 

Privada: Ela está sob a posse do usuário. 

 

Com a combinação dessas duas chaves, é possível assegurar não somente a confidencialidade, mas também o não repúdio ou irretratabilidade. Afinal, pode-se combinar o uso desse controle tanto com a chave privada do emissor (não repúdio) quanto com a pública do destinatário (confidencialidade). 

Diffie-Hellman, El Gamal e Curvas Elípticas são alguns dos algoritmos desta família. Quanto aos controles aplicados às redes, destacam-se os firewalls, os sistemas detectores de intrusão e os VPNs. 

 

**Firewalls: Equipamentos que filtram o tráfego de rede relacionado à troca de dados entre clientes e servidores.** 

 

Esses controles permitem a criação de zonas de segurança dentro e fora da instituição. Tais zonas, por sua vez, possibilitam a criação de segregações de funcionalidades. 

Das zonas de segurança, a mais comumente encontrada é a DMZ. Zona desmilitarizada, ela limita, conforme demonstra a figura a seguir, a região onde os servidores web e de aplicação podem ficar. 

![Informação](media/introducao-a-seguranca-da-informacao/diagrama-dmz.png)

As regras dos firewalls podem seguir duas políticas: 

 

**Negar por padrão**: Todo o tráfego é negado. Apenas os servidores e os protocolos são autorizados. 

Trata-se da política normalmente encontrada e recomendada no mercado. Como todos os tráfegos são negados, apenas podem trafegar aqueles cujas regras (R1) são aceitas. 

 

**Aceitar por padrão**: Nesta política, todo o tráfego é autorizado, embora o destinado para determinados servidores seja negado. 

Qualquer tráfego é aceito por padrão. Regras específicas (R1 e R2) definem quais serão negados. 

# Aula 2 - Ameaças e vulnerabilidades à segurança da informação 

 

### Ameaças e vulnerabilidades 

 

Atualmente, a informação é um dos principais ativos das empresas. Por meio das informações, novas tecnologias são obtidas, novos fármacos são ofertados no mercado e salvam vidas. O filme Trocando as Bolas (do inglês, Trading Places, de 1983) ilustra bem essa questão: O enredo trata de dois corretores bem-sucedidos, os irmãos Duke, que resolvem apostar 1 dólar pela troca de um alto executivo, personagem de Dan Aykroyd, por um mendigo, interpretado por Eddie Murphy. Com o desenrolar da história, aborda-se o acesso a informações privilegiadas dos irmãos Duke sobre a safra da laranja no mercado norte-americano. 

 

As instituições têm o seu valor de mercado calculado a partir de seu market share, produtos, patentes, instalações, bens e informações, ou seja, de seus ativos. Os ativos podem ser classificados como tangíveis, quando é possível medir o seu valor, e como intangíveis, quando é difícil, ou impossível, medir o seu valor. Para compreender melhor esses conceitos, vejamos alguns exemplos: 

 

Um **ativo intangível** é a imagem de uma organização ou um produto. Durante muito tempo, algumas operadoras de telefonia tiveram a qualidade de seus serviços prejudicada em função de problemas técnicos de cobertura de sinal. Esse “fantasma” ainda assola os corredores dessas empresas. Que campanha pode ser realizada para mudar tal situação? Percebeu o quão intangível é a imagem de uma companhia? 

 

Os **ativos tangíveis**, por sua vez, são aqueles que conseguimos medir. Eles podem ser classificados como lógicos, quando nos referimos a informações ou softwares; físicos, quando nos referimos a equipamentos ou infraestruturas; e humanos, quando nos referimos a colaboradores e prestadores de serviço 

 

Ativos tangíveis lógicos: São aqueles que envolvem a informação e sua representação em algoritmos, como, por exemplo, uma fórmula química, os detalhes sobre a safra da laranja no mercado norte-americano, o algoritmo principal de busca do Google, os detalhes técnicos das baterias dos carros do Elon Musk. 

 

Ativos tangíveis físicos: São aqueles que conseguimos tocar, como a usina hidrelétrica de Itaipu, a ponte Golden Gate e o Cristo Redentor. Esses são exemplos de infraestruturas cuja ausência poderá provocar uma perda significativa que ficará marcada na memória. Provavelmente, você se lembra de onde estava no dia 11 de setembro de 2001. Em termos de equipamentos, podemos citar as prensas de papel moeda da Casa da Moeda; o supercomputador Santos Dumont, que permite fazer o sequenciamento do genoma de diversos seres vivos etc. 

 

Ativos tangíveis humanos: Referem-se aos colaboradores e prestadores de serviço, como, por exemplo, a troca de jogadores de futebol e técnicos nos clubes e as cifras astronômicas que circulam nesse mercado. A mesma situação ocorre em outros esportes, como automobilismo, basquete etc. 

 

De maneira geral, os ativos tangíveis e intangíveis se posicionam e se desdobram desta maneira: 

![Ativos tangíveis e intangíveis](media/introducao-a-seguranca-da-informacao/ativos_tan_int.png)

A perda ou a danificação desses ativos poderia acarretar problemas financeiros gigantescos. Vamos analisar o caso da Apple. Em 1997, Steve Jobs (1955-2011) retornou para a Apple e, até o seu falecimento, as ações da empresa aumentaram 9000%. Em termos comparativos, nos últimos dois anos de vida de Jobs, os valores das ações mais do que dobraram, enquanto os da Microsoft subiram 5,1% e os da Intel valorizaram 14% no mesmo período. Quando Jobs faleceu, as ações da Apple tiveram uma queda, não tão acentuada, mas ainda assim uma queda. Trata-se de um claro exemplo de um ativo humano e da perda financeira causada quando ocorre um problema desse tipo. Do mesmo modo, pode ocorrer também a hipervalorização quando um novo ativo é obtido. 

 

Para proteger esses ativos, precisamos criar barreiras de proteção aos diversos tipos de problemas que possam acontecer. Os controles de segurança da informação, também conhecidos como medidas de proteção, são as ferramentas, os equipamentos, as metodologias e os processos que usamos para proteger um ativo contra uma ameaça e a(s) sua(s) vulnerabilidade(s) associada(s). 

 

Como relacionar uma ameaça e uma vulnerabilidade? 

Vamos pensar em um exemplo baseado em um desenho infantil, o Papa-Léguas. 

 

Na animação, o coiote tentava jogar uma bigorna em cima do pássaro, mas vamos trocar nossos atores. Em vez do pássaro, imaginemos um refrigerante, cuja fórmula está salva em um dispositivo de armazenamento externo (pen drive). Nesse caso, a bigorna é uma ameaça contra o nosso dispositivo. Para proteger o nosso pen drive, podemos colocá-lo dentro de uma caixa de metal hiper-resistente. Certamente criamos uma proteção (controle) contra a ameaça (bigorna). 

Vamos agora trocar o pen drive por uma folha de papel. Uma bigorna é uma ameaça contra uma folha de papel? Não necessariamente. Mas o fogo seria uma ameaça antes e continua sendo agora. Então, nesses dois casos, o fogo persiste e provavelmente o controle anterior não protegeria o pen drive nem a folha de papel contra essa ameaça. Podemos perceber, portanto, que para explorar a vulnerabilidade de um ativo pode existir uma ou mais ameaças. Da mesma forma, contra uma vulnerabilidade pode haver uma ou mais ameaças. 

![Ativos tangíveis e intangíveis](media/introducao-a-seguranca-da-informacao/ativos_tan_int.png)

O ativo corresponde à figura estrelada central. Cada sulco é uma vulnerabilidade que pode ser explorada por uma ameaça. Cada ameaça tem uma chance (probabilidade) de acontecer, representada na figura pelo tamanho da seta. Assim, há ameaças com grande probabilidade (setas maiores) de acontecer e outras com pouca probabilidade de acontecer (setas menores). 

Os semicírculos vermelhos correspondem aos controles que podem proteger o ativo contra uma ou mais ameaças. 

Por exemplo, um incêndio e uma enchente são ameaças físicas para um servidor em um data center. Mais do que isso, são pesadelos para os melhores administradores de TIC. Um sistema anti-incêndio com sprinklers, detectores de fumaça, extintores e uma brigada contra incêndio com treinamentos periódicos correspondem a bons controles que podem envolver equipamentos, pessoas e processos. Em um incêndio, esses itens são boas formas de proteção. Mas e em uma enchente? Esses controles são totalmente ineficientes. E durante a falta de energia elétrica? Ou mesmo em uma sobrecarga de energia elétrica? 

 

Recorrendo à figura, o que seria mais usual de acontecer: incêndio, enchente, falta de energia elétrica ou sobrecarga de energia elétrica? Certamente isso dependeria de uma análise geográfica do local de instalação do data center. Se ele estivesse instalado no Cerrado nordestino, seria razoável pensar em uma enchente? Ou se o data center estivesse instalado em uma região de mangues mato-grossenses, seria razoável pensar em uma enchente? Ou em uma região da Amazônia conhecida pelo elevado número de descargas atmosféricas que ocorrem por ano? 

O correto seria a análise e avaliação dos riscos associados à instalação de data centers na região, devendo obedecer a critérios específicos de probabilidade de ocorrência e sorte, afinal de contas, qual seria a probabilidade de dois aviões colidirem em duas torres de um mesmo prédio? 

![Sistema de combate a incêndio](media/introducao-a-seguranca-da-informacao/incendio.png)


Após a análise e avaliação do risco e a sua probabilidade de ocorrência, podemos adotar uma metodologia como a identificação dos ativos e o cálculo do seu valor. Será mesmo que precisamos usar todo e qualquer controle para proteger o ativo? E se o ativo valer menos do que o controle, ainda seria vantajoso implementar esse controle? Com a definição do valor do ativo, a análise e avaliação do risco e os custos para implementar as proteções necessárias, começam as decisões. 

 

Uma boa comparação está no seguro de um automóvel. Ao contratarmos uma seguradora, o valor da franquia do seguro nos é apresentado. Se ocorrer um sinistro e ele for mais barato do que o valor da franquia, valerá a pena acionar o seguro? Não, pois pagaremos mais caro. Um risco na carroceria é o suficiente para acionar o seguro? E uma batida frontal? E quando o carro sofre perda total? A seguradora decide pagar o valor segurado, pois é mais barato do que mandar consertar. 

 

### Tipos de ameaças e vulnerabilidades 

 

A segurança da informação é fundamentada em três aspectos: 

![Três aspectos](media/introducao-a-seguranca-da-informacao/tres_aspectos.png)

Tomando-se por base esses três aspectos, pode-se classificar alguns tipos de ameaças e os respectivos controles que podem ser adotados. 

Nos últimos meses, as ocorrências de pessoas relatando problemas de invasão nas contas de WhatsApp multiplicaram. Esse incidente permite que alguém se aproprie da conta do serviço de mensagem de outra pessoa para pedir dinheiro em nome do dono da conta. Nesse exemplo, podemos perceber o acesso não autorizado, que poderia ser corrigido pelo uso de senhas, evitando possíveis problemas de alteração de dados, ou pela adoção de métodos múltiplos de autenticação. São exemplos clássicos de perdas de confidencialidade e integridade. Poderá, ainda, haver recuperação de dados dos usuários por meio de backups realizados pelo sistema. Para esse problema, recomenda-se o uso da confirmação em duas etapas. 

Outro exemplo que podemos citar é o armazenamento de documentos eletrônicos. Atualmente, em termos de aplicações que conseguem colocar o rosto de uma pessoa em outra, alterar documentos torna-se uma ação simples de ser realizada. Logo, uma forma de proteger o documento eletrônico é guardar um selo de autenticidade para assegurar que o documento está íntegro. Uma ferramenta bem disseminada é o uso de funções de hashes. 

![](media/introducao-a-seguranca-da-informacao/aspecto-ameaca-seguranca.png)

Outra forma de abordar as ameaças descritas é utilizando a classificação quanto a ser física ou lógica. Fenômenos naturais e perdas de dispositivos de armazenamento são exemplos de ameaças físicas enquanto as demais são exemplos de ameaças lógicas. 

Podemos reorganizar a tabela anterior e reapresentar as ameaças de acordo com a taxonomia física e lógica, obtendo a seguinte tabela: 

![](media/introducao-a-seguranca-da-informacao/classificacao-ameaca-seguranca.png)

Podemos consolidar da seguinte forma: se ocorrer falha em equipamentos e instalações, a ameaça é física. Caso contrário, se estiver relacionada a problemas de software, algoritmos etc., é considerada ameaça lógica. 

 

Quando a ameaça tiver algum agente humano, é classificada dessa forma. Caso contrário, como, por exemplo, nos fenômenos oriundos de causas naturais, como incêndio e enchentes, é conhecida como ameaça não humana. Veremos os detalhes na próxima tabela: 

![](media/introducao-a-seguranca-da-informacao/classificacao-ameaca-seguranca-2.png)

As ameaças humanas são aquelas que foram provocadas por seres humanos, e as não humanas são provocadas pela natureza ou por problemas de infraestrutura. As ameaças provocadas por seres humanos podem ainda ser classificadas de duas formas: 

 

As oriundas de colaboradores ou pessoas mal-intencionadas e aquelas oriundas de pessoas ou colaboradores que não possuem o conhecimento adequado (mal treinados). Nesse caso, o colaborador, propositalmente, faz ações que podem provocar incidentes e prejuízos financeiros, seja pela perda de confidencialidade de algum ativo, seja pela adulteração de algum ativo para agente ou processo não autorizado. 

 

X 

 

Em oposição, há os chamados hackers que exploram as vulnerabilidades para demonstrar conhecimento e exibir seu feito para a comunidade; ou ainda pelo simples desafio de alcançar o objetivo, como se fosse um jogo; ou mesmo para obter ganhos financeiros a partir da obtenção de ativos das instituições. Exemplo disso são as notícias que circularam em junho de 2020, quando o governo norte-americano alegou terem sido realizadas invasões para o roubo da pesquisa farmacológica de remédios do coronavírus. 

 

As ameaças não humanas podem ainda ser classificadas em ameaças oriundas de desastres ou de problemas de infraestrutura. Essas ameaças podem ser mitigadas pela gestão do risco envolvido na implantação dos ativos. 

Por exemplo, na construção do data center, se a região possui enchentes com certa regularidade, é razoável pensar em alternativas concretas para mitigar esses riscos. A enchente é um exemplo de causa natural. Na contramão, um incêndio causado por uma sobrecarga elétrica é um exemplo de uma ameaça não humana, resultante de problemas de infraestrutura. 

 

Quando a ameaça tiver algum agente humano, é classificada dessa forma. Caso contrário, como, por exemplo, nos fenômenos oriundos de causas naturais, como incêndio e enchentes, é conhecida como ameaça não humana. Veremos os detalhes na próxima tabela: 

![](media/introducao-a-seguranca-da-informacao/tipo-classificacao-ameaca.png)

Essas classificações se sobrepõem e permitem que determinada ameaça possa ser classificada por vários critérios. Vamos explorar um exemplo disso: 

 

Considere uma chuva torrencial em uma região metropolitana, onde tenha um data center implantado. Nosso país, pela sua geografia, possui locais em que ocorrem chuvas em determinadas épocas do ano, em especial as chuvas durante o verão no Rio de Janeiro. Trata-se de um problema que ocorre em diversas capitais brasileiras. Se uma rua inundasse, como ficaria um data center? Já imaginou a perda ocasionada por essa ameaça? 

 

No caso de uma inundação em um data center, o principal problema gerado é a disponibilidade. Dependendo dos controles (proteções) escolhidos pelo gestor, até mesmo problemas de integridade dos dados podem ser gerados. Por isso, sempre é necessário realizar a abordagem em camadas. Nesse cenário, alguns controles simples poderiam ser desenvolvidos: 


1. Contingência: desenvolvimento de alguma técnica/metodologia para suprir a ausência ou falha do data center. 

2. Processo e treinamento do uso da contingência. 

3. Processo e realizações de cópias de segurança, bem como a verificação do status dessas cópias, inclusive com simulação de desastres. 

Lógico que não é possível esgotar totalmente o assunto, pois várias situações complementares poderão ocorrer e a lista estaria incompleta, mas, por si só, essas seriam as principais abordagens. 

Um exemplo de classificação das ameaças, como uma inundação, pode afetar a disponibilidade e/ou integridade (quanto ao aspecto da segurança da informação (CID)), física (quanto ao tipo de ativo envolvido), não humana (quanto ao vetor de ataque) e causada por desastre natural. 

 

### Ataques cibernéticos 

 

As ameaças cibernéticas são concretizadas por meio do uso de técnicas que normalmente exploram a **vulnerabilidade de uma tecnologia**, de um **processo** ou de uma **metodologia**. 

No caso de uma vulnerabilidade relacionada à tecnologia, ela se vincula com a forma de desenvolvimento da ferramenta e, certamente, novas versões daquele software trarão a correção adequada. Um bom exemplo disso é o ping da morte (ping of death) que durante muitos anos foi o pesadelo dos gerentes de TI e atualmente não passa de história nos livros sobre segurança. 

 

São ações maliciosas intencionais, provocadas por hackers ou por funcionários insatisfeitos. Essas ameaças humanas já foram objeto de explicação no módulo anterior e vimos que as pessoas estão envolvidas. Aqui falaremos do que essas pessoas poderiam realizar. 

As razões e motivações já foram explicadas, mas podermos resumi-las ao estímulo de se obter determinada informação (ferindo a confidencialidade), danificar a informação (ferindo a integridade) e interromper o funcionamento de determinado sistema (ferindo a disponibilidade). 

No campo do exibicionismo que motiva essas pessoas, podemos exemplificar as informações divulgadas pelo site zone-h, que possui uma lista dos últimos ataques que aconteceram, funcionando como um hall da fama, onde os hackers disputam a quantidade e qualidade dos ataques realizados. Percebe-se que o principal fator é a motivação do hacker em proferir o ataque. 

 

Mas como tornar um serviço indisponível por meio de outro tipo de ameaça que não a humana? 

Outras situações podem gerar a indisponibilidade do serviço, como enchentes etc. Um simples poste caído devido a uma batida de carro pode gerar uma perda de comunicação e a indisponibilidade do serviço. 

De qualquer forma, uma boa análise e a avaliação do risco associado devem ser realizadas buscando o desenvolvimento dos controles associados para a criação da contingência necessária. 

 
Dica: Redundâncias e contingências são sempre úteis e, quando possível, devem sempre ser utilizadas. 

 

### Ataques de negação de serviço (DOS) 

 

Corresponde a um tipo de ataque que tem por objetivo indisponibilizar determinado sistema ou equipamento. Ou seja, o equipamento pode até estar funcionando, mas seu uso fica prejudicado pela impossibilidade de acesso ao serviço prestado. Nesse tipo de ataque, são exploradas vulnerabilidades de softwares, de equipamentos e de algoritmos/protocolos. 

 

São exemplos o pod (ping of death), syn flood, udp flood e o tcp flood. Esses ataques exploram vulnerabilidades na implementação de algum serviço de rede, sistema operacional ou protocolo utilizado. Foram muito famosos no início de disseminação desse tipo de ataque e atualmente são utilizados com mais de um agente (fonte), caracterizando assim uma nova classe de ataques, os distribuídos, que é interpretada como uma variante do DoS quando a fonte do ataque é distribuída, ou seja, quando há mais de uma fonte de emissão de sinais de ataques destinados para uma ou mais vítimas. 

 
 

Antes eram utilizados os mesmos tipos de ataques para cada fonte. Atualmente, é comum encontrarmos situações em que cada fonte possui um tipo de ataque diferente, utilizando vulnerabilidades em implementação, sistema operacional ou protocolo. Assim, fica claro que há uma coordenação que determina a sincronicidade e o momento que os ataques serão proferidos. A necessidade de coordenação tornou urgente o desenvolvimento de uma infraestrutura de ataque e que diversas etapas predecessoras fossem criadas. 

 

### Engenharia social 

 

Situação em que são usadas as fraquezas humanas para se obter informação (ferir a confidencialidade) de uma pessoa ou organização. Normalmente, comenta-se que o elo mais fraco, exatamente aquele que poderá ser o primeiro a ser explorado, é o humano. Em uma organização é difícil que todos os colaboradores tenham o mesmo entendimento e a mesma maturidade com relação ao sigilo de informações. 

 

O exemplo mais comum desse tipo de ataque é o phishing, comumente utilizado para obter dados de cartões de crédito, visando ao ganho financeiro. 

 

Ações de phishing podem acontecer de diversas formas. Pode ser um e-mail semelhante ao de uma instituição financeira, um SMS com um link para regularizar uma situação, uma página (ou post) em uma rede social e até mesmo um site inteiro clonado. 

Outro exemplo bem comum na década de 1990 eram dispositivos, que possuíam várias formas e partes diferentes, que liam os cartões de crédito (naquela época sem chip) para copiar a tarja magnética. No Brasil, eles ganharam o apelido de chupa-cabra, fazendo menção a uma situação ocorrida em Minas Gerais, que era creditada à presença de alienígenas naquela região, na mesma época da aparição desses mecanismos. 

 

O que chama bastante atenção é o grau de sofisticação usado pelos fraudatários na construção dos dispositivos de fixação e com aparência bem próxima aos dos bancos. 

 

### Pichação de site 

 

Corresponde à técnica mais utilizada e se caracteriza pela alteração não autorizada de determinado site na internet. Também conhecido como defacement, essa técnica objetiva a adulteração do portal, sem o consentimento do proprietário. São exploradas as vulnerabilidades dos portais e, por meio disso, são realizadas as modificações. 

Esse ataque é mais popular pela repercussão gerada após a sua realização. É relativamente fácil encontrá-lo em ferramentas de gestão de conteúdos (CMS), onde o proprietário do site apenas customiza determinados assuntos no portal, ou faz uso de plug-ins para ofertar novas formas de interação com o usuário. 

 

### Botnets 

 

Também conhecido como rede zumbi, é um conjunto de equipamentos que sofreu um ataque, resultando no controle do equipamento pelo hacker. O ataque é realizado através de um software chamado bot, que explora uma vulnerabilidade do equipamento e faz a instalação nele. 

Na botnet, existem alguns equipamentos cuja finalidade é orquestrar o ataque, permitindo a manutenção do sigilo do hacker. Esses equipamentos são chamados de centros de comando e controle. Os bots se assemelham aos worms no que se refere à forma de proliferação, porém divergem por acatarem às ordens dos centros de comando e controle. Através de botnets é possível fazer ataques de negação de serviço, envios de e-mails em massa e vários outros. 

 

### Outras técnicas utilizadas em ataques cibernéticos 

 

IP SPOOFING: Ocorre quando o atacante forja o seu endereço IP, colocando outro valor nesse campo, fingindo ser a fonte dos dados de outra origem. É muito comum por explorar a vulnerabilidade do protocolo. 

 

PHARMING OU DNS CACHE POISONING: Ocorre quando os servidores de DNS são atacados, visando alterar a troca dos nomes de domínios por endereços IPs e, assim, destinando a vítima para equipamentos e softwares falsos. Explora vulnerabilidades em determinadas implementações e marcas de equipamento. É uma técnica difícil de ser identificada pelo usuário final. 

 

IP SESSION HIJACKING: A conexão entre o cliente e o servidor na internet é realizada através de troca de comandos HTTP de requisição e resposta, por exemplo. Durante esse processo, é comum ter alguma sessão de usuário (HTTP Session) configurada e em execução, visando identificar o usuário que está acessando o portal. 

Uma das técnicas utilizadas, seja para quebrar a confidencialidade do usuário, ou para realizar um ataque ao portal, é o sequestro de sessão do usuário. Logo, o invasor captura essa troca de informações e se faz passar por um dos equipamentos. Trata-se de uma técnica com certo grau de sofisticação e difícil de ser identificada por gerentes de rede e usuários finais. 

 

QUEBRA DE SENHAS: As senhas nos sistemas de informação ficam codificadas no servidor. A codificação pode ser realizada por meio de técnicas proprietárias do sistema, onde são desenvolvidos algoritmos específicos de codificação, ou por meio de funções de condensação, também conhecidas como hash. 

As quebras de senha podem usar conjuntos especiais de tabelas, conhecidas como rainbow tables, ou até mesmo a testagem de todas as combinações possíveis, chamada de força bruta. Nessa técnica, o grau de conhecimento do atacante determinará a eficácia do ataque. 

 

HASH: São algoritmos criados usando manipulações algébricas que transformam os dados de entrada em um conjunto finito de números hexadecimais, chamado de hash do dado. Essas manipulações impedem que os valores iniciais sejam recuperados a partir dos dados gerados. 

 

TRASHING DUMPSTER DIVING: Nessa técnica, são realizadas buscas nos lixos corporativos na expectativa de ter sido realizado algum descarte de forma inapropriada. Isso nos remete ao primeiro módulo, onde tratamos do ciclo de vida da informação. Se o descarte não for feito de forma apropriada, técnicas como essa permitem a recuperação da informação direto do lixo. Em muitos países, não há legislação que torne essa técnica ilegal. 

 

WARDRIVING: Pesquisa de locais físicos contendo sinal de Wi-Fi desprotegido visando à exploração da vulnerabilidade encontrada. Nessa técnica, o invasor percorre os espaços públicos procurando os sinais desprotegidos, podendo ser a pé, de carro ou utilizando drones. 

 

#### Funções dos hashes 

 

As manipulações impedem que os valores iniciais sejam recuperados a partir dos dados gerados, desta forma: 

![Algoritmo do Hash](media/introducao-a-seguranca-da-informacao/algoritmo-hash.png)

A tabela a seguir apresenta os principais algoritmos de hash (funções de condensação) utilizados no mercado: 

| Algoritmo | Tamanho do hash gerado (bits) |
| - | - |
| MD5 | 128 |
| SHA-1 | 160 |
| SHA-256 | 256 |
| SHA-512 | 512 |

Na tabela a seguir, consta o resultado para cada algoritmo do hash da palavra Brasil: 

![Exemplo de Hash](media/introducao-a-seguranca-da-informacao/exemplo-hash.png)

Como as funções de hashes podem ser aplicadas a quaisquer tipos de conjunto de dados, independentemente do tamanho, e o conjunto resultado possui um tamanho fixo, para um dado algoritmo, pode acontecer de dois dados de entrada diferentes encontrarem o mesmo conjunto resultado, fenômeno conhecido como colisão. 

 

### Softwares maliciosos 

 

Malwares: São softwares maliciosos que objetivam a infecção dos ativos de TI. Nessa categoria, há uma variação muito grande e com diversos tipos. Podemos citar os vírus, cavalos de Troia (referenciado na imagem) relacionados com propaganda, ferramentas de suporte usadas indevidamente, exploits e worms.. 

 

**Cavalo de Troia**: Inspirado no exemplo histórico que deu origem à técnica, mascara-se um vetor de ataque, normalmente um malware, dentro de um documento ou ferramenta, enganando a vítima do ataque. 

 

**Exploits e worms**: São as aplicações construídas especificamente para explorar determinadas vulnerabilidades existentes e os worms, muitas vezes confundidos com os vírus, utilizam as estruturas de comunicação para sua disseminação. 

 

Há divergências entre as formas de classificação dos tipos de malwares. Porém, de maneira geral, pode-se dizer que os vírus são os malwares que precisam de um ambiente para a sua execução. 

Os vírus relacionados com propaganda, como os spywares (por exemplo, aplicações que capturam tudo o que é digitado pelo usuário, conhecidas como keyloggers) e adwares (aplicações que trazem propaganda para o usuário, sem sua autorização) monitoram o usuário de alguma forma, visando explorar o aspecto comportamental humano. 

Ainda há o uso mal-intencionado de ferramentas de suporte, como sniffers (farejadores) de rede e port scanners. O primeiro permite analisar o tráfego de rede e o segundo permite verificar quais são as portas de comunicação dos protocolos da camada de transporte que estão disponíveis para conexão. 

 

### Ransomware 

 

Software malicioso, com alto poder de reprodutibilidade, que invade a máquina da vítima, criptografa os seus dados e solicita um resgate. Nos últimos anos, esse tipo de ataque tem sido bem frequente, tendo como caso emblemático o WannaCry. 

# Aula 3 – Normas de segurança da informação 

 

### Conceito 

 

A ISO ‒ International Organization for Standardization (Organização Internacional de Padronização) é uma entidade fundada em 1947, sediada na Suíça e que congrega organismos de normalização nacionais.   

 

Sua principal atividade é elaborar padrões para especificações e métodos de trabalho nas mais diversas áreas da sociedade. 

 

A ISO colabora estreitamente com a International Electrotechnical Commission (IEC) em todos os assuntos de padronização eletrotécnica. 

 

As normas internacionais para sistemas de gerenciamento fornecem um modelo a ser seguido para a configuração e operação de um sistema de gerenciamento. 

Por meio do uso da família de padrões de um Sistema de Gestão da Segurança da Informação ‒ SGSI (do inglês Information Security Management System – ISMS), torna-se possível o desenvolvimento e a implementação de uma estrutura visando à gerência da segurança dos ativos de informações. 

Dentre outros documentos que eventualmente podem existir, a família ISO/IEC 27000 oferece um conjunto de normas relacionadas à Segurança da Informação. 

 

A norma ISO/IEC 27000 traz os princípios e o vocabulário utilizados nas normas seguintes da família 27000. O download pode ser feito gratuitamente (em inglês) na página da ISO. 

 

De acordo com a ABNT NBR ISO/IEC 27001:2013: 
 
A norma ISO/IEC 27001 (Information Technology ‒ Information Security Management Systems ‒ Requirements foi preparada para prover requisitos para estabelecer, implementar, manter e melhorar continuamente um Sistema de Gestão de Segurança da Informação (SGSI). 

 

Cabe à alta direção de cada organização decidir pela adoção de um Sistema de Gestão da Segurança da Informação (SGSI). 

 

A norma cita alguns fatores de influência para o seu estabelecimento e a sua implementação, como: 

 

1- Necessidades; 

2- Objetivos; 

3- Requisitos de segurança; 

4- Processos organizacionais; 

5- Tamanho e estrutura da organização. 

O SGSI **preserva a tríade CID** (confidencialidade, integridade e disponibilidade) da informação, aplicando um **processo de gestão de riscos**. Com isso, as partes interessadas (stakeholders) poderão ter uma maior confiança de que os riscos serão convenientemente gerenciados. 

Segundo a ABNT (2013), é importante que um SGSI seja parte, e esteja integrado com os **processos da organização** e com a estrutura de **administração global**, e que a segurança da informação seja considerada no projeto dos processos, sistemas de informação e controles. 

A norma ISO/IEC 27001, em conjunto com a norma ISO/IEC 27002 (Código de Boas Práticas da Gestão da Segurança da Informação), formam as principais referências, atualmente, para quem procura tratar a questão da segurança da informação de maneira eficiente e com eficácia. 

As normas técnicas nacionais são estabelecidas por um organismo nacional de normalização para aplicação em um dado país. No Brasil, as Normas Brasileiras (NBRs) são elaboradas pela ABNT (Associação Brasileira de Normas Técnicas). 

A ABNT é reconhecida pelo Estado brasileiro como o Fórum Nacional de Normalização, e as NBRs são reconhecidas formalmente como as normas brasileiras. 

As nomenclaturas das normas ISO/IEC 27001 e 27002 são, respectivamente, **ABNT NBR ISO/IEC 27001 e ABNT NBR ISO/IEC 27002**. 

Ao longo do texto, podem ser consideradas tanto as normas brasileiras quanto as normas ISO, mas as NBRs são idênticas às normas ISO, sendo possível fazer referência a ambas sem prejuízo no contexto do conteúdo e no entendimento. 

Observe, a seguir, um comparativo sobre o que a norma ISO/IEC 27001 é e não é. 

![ISO/IEC 27001 é](media/introducao-a-seguranca-da-informacao/27001-eh.png)

![ISO/IEC 27001 não é](media/introducao-a-seguranca-da-informacao/27001-nao-eh.png)

A versão mais atual da norma (até a escrita desse texto) a ser considerada nesse texto é a **ISO/IEC 27001: 2013**, que sucede e substitui a versão de 2005. 

Uma grande novidade dela é o alinhamento com as diretrizes do **Anexo L**, chamado até 2019 de Anexo SL (conhecido antigamente como ISO Guide 83).   

O Anexo L é uma seção da ISO/IEC Directives, Part 1, Consolidated ISO Supplement, que padroniza definições e estruturas de **diferentes sistemas de gestão** ISO. Com isso, a norma está alinhada com outros padrões de sistemas de gestão, como ISO 9001, ISO 14000, ISO 20000, ISO 22000, ISO 22301. 

Na versão 2013 da norma ISO/IEC 27001 houve o alinhamento com as diretrizes do Anexo L, que padroniza definições e estruturas de diferentes sistemas de gestão ISO. 

No Anexo L, todas as normas de sistema de gestão do futuro terão a **mesma estrutura de alto nível** (tabela 1), **texto principal idêntico**, bem como **termos e definições comuns**. 

A estrutura de alto nível não pode ser modificada; por sua vez, podem ser acrescentadas subcláusulas e textos específicos para cada disciplina abordada. 

![Clausulas](media/introducao-a-seguranca-da-informacao/clausulas.png)

### Requisitos 

 

Conforme a ABNT NBR ISO/IEC 27001 (2013), o título da norma **ABNT NBR ISO/IEC 27001:2013** é **Sistemas de Gestão da Segurança da Informação – Requisitos**. 

Essa norma, então, especifica os requisitos para estabelecer, implementar, manter e melhorar continuamente um sistema de gestão da segurança da informação dentro do contexto da organização. 

Também inclui requisitos para a avaliação e o tratamento de riscos de segurança da informação voltados para a necessidade da organização. 

A principal característica, ou palavra-chave, é: **DEVE**. 

O leitor observará que a norma sempre indicará o que o gestor **deverá** fazer em relação às cláusulas das disciplinas do SGSI. Por exemplo, em 4.3, a organização deve determinar os limites e a aplicabilidade do sistema de gestão da segurança da informação para estabelecer o seu escopo. 

 

Para você que está começando a se familiarizar com a norma, uma boa maneira de ter uma noção geral dos conteúdos de normas é analisando o sumário e assimilando o que possuem as suas estruturas. 

 

Algumas razões para adotar a norma incluem: 

* Eficácia melhorada da Segurança da Informação. 

* Diferenciação do mercado. 

* Satisfazer exigências dos clientes. 

* Único padrão com aceitação global. 

* Responsabilidades focadas na equipe de trabalho. 

* A Tecnologia da Informação cobre padrões tão bem quanto a organização, pessoal e facilidades. 

* Mandados e leis. 

 

A norma ISO/IEC 27001 é passível de certificação acreditada. 

Alguns benefícios da **certificação** ISO/IEC 27001 incluem: 

* Responsabilidade reduzida devido às políticas e aos procedimentos não implementados ou reforçados. 

* Oportunidade de identificar e eliminar fraquezas. 

* A Gerência participa da Segurança da Informação. 

* Revisão independente do seu SGSI. 

* Fornece segurança a todas as partes interessadas. 

* Melhor consciência da segurança. 

* Une recursos com outros sistemas de gerenciamento. 

* Mecanismo para medir o sucesso do sistema. 

 

### Certificados 

 

Uma visão geral da situação dos certificados no mundo pode ser obtida através dos dados disponibilizados no **The ISO Survey of Certifications**.

Trata-se de uma pesquisa anual do número de certificados válidos para os padrões do sistema de gerenciamento ISO em todo o mundo. 

Os dados são fornecidos pelos organismos de certificação credenciados. 
 

**Certificado** é o documento emitido por um organismo de certificação. 

**Site** é um local permanente em que uma organização realiza trabalho ou serviço. 

 

O conteúdo do gráfico, que você verá a seguir, foi extraído da planilha disponível na página da ISO. Ele exibe um trecho do número total de certificados válidos e o número total de sites para o padrão ISO/IEC 27001:2013. 

![Lista dos 10 países com maior número de certificados](media/introducao-a-seguranca-da-informacao/lista-paises.png)

A norma **ABNT NBR ISO/IEC 27002:2013** apresenta as **melhores práticas** a serem utilizadas na gestão da segurança da informação. Seu título é Código de Prática para a Gestão da Segurança da Informação. 

A sua principal característica, ou palavra-chave, como já foi explicado anteriormente, é: **CONVÉM**. 

A versão **mais atual** da norma (até a escrita desse texto) a ser considerada neste tema é a ISO/IEC 27002:2013, que sucede e substitui a versão de 2005. No passado, era conhecida como ISO/IEC 17799. 

Em comparação com a versão 2005, na versão 2013 o número de **seções** aumentou de 11 para **14**. 

 

A versão 2013 recomenda 114 tipos de controles básicos. 

 

Cada seção principal contém: 

* Um objetivo do controle declarando o que se espera que seja alcançado. 

* Um ou mais controles que podem ser aplicados para se alcançar o objetivo de controle. 

 

As **descrições do controle** estão estruturadas da seguinte forma: 

 

CONTROLE: Define a declaração específica do controle, para atender ao objetivo de controle. 

Segundo a ISO/IEC 27000 (2018), o controle é uma medida que pode modificar o risco, seja ele através de um processo, política, dispositivo, prática ou outras ações que modifiquem a ameaça e/ou a vulnerabilidade e, consequentemente, o risco. 

 

DIRETRIZES PARA IMPLEMENTAÇÃO: Apresenta informações mais detalhadas para apoiar a implementação do controle e alcançar o objetivo do controle. 

As diretrizes podem não ser totalmente adequadas ou suficientes em todas as situações e podem, portanto, não atender completamente aos requisitos de controle específicos de uma organização. 

 

INFORMAÇÕES ADICIONAIS: Apresenta mais dados que podem ser considerados, como questões legais e referências normativas. 

Se não existem informações adicionais, esta parte não é mostrada no controle. 

 

### Tendências 

 

O estudo das normas técnicas não se limita apenas ao aprendizado dessas normas aqui apresentadas. 

Um caminho que pode ser seguido é analisar também outras normas de sistemas de gestão, tais como qualidade, meio ambiente, conhecimento, ativos, educação etc. 

 

### Considerações finais 

 

As normas ISO/IEC 27001 e ISO/IEC 27002 fazem parte de um ecossistema de boas práticas em tecnologia da informação. Em um ambiente organizacional cada vez mais competitivo e alinhado com a conformidade em suas atividades, o processo para a adoção das normas, bem como de outros guias (por exemplo, ITIL, COBIT), está sendo uma estratégia necessária até para a própria sobrevivência, dependendo do contexto de suas atividades. E é nesse ambiente que o futuro profissional poderá continuamente se valorizar e se inserir. 

# Aula 4 – Boas práticas em segurança da informação 

 

Segurança da informação: Um conjunto de medidas que visa a garantir a confidencialidade, a integridade e a disponibilidade das informações de uma organização ou de um usuário. 

 

Cada vez mais empresas estão investindo em segurança da informação devido à necessidade de se protegerem contra ataques digitais e, dessa forma, garantirem sua operacionalidade. Além dessas ações é preciso que os usuários e colaboradores com acesso aos sistemas de uma empresa ajam de modo a não comprometer a segurança da informação. 

 

### Gerenciamento de senhas 

 

O ponto de partida de qualquer sistema de segurança é garantir o acesso a dados, equipamentos, demais sistemas e ambientes físicos e eletrônicos aos indivíduos autorizados. A essa característica dá-se o nome de **autenticidade** e a forma mais simples de oferecê-la é por meio do login e da senha de acesso. 

Deve-se dar atenção particular à senha, mais especificamente ao **gerenciamento das senhas**, visto que, com o login e a senha, um usuário pode ter acesso a equipamentos, sistemas e demais recursos de uma companhia, como, por exemplo, instituições de ensino, comerciais, governamentais ou religiosas. 

Além da óbvia preocupação de garantir segredo sobre a senha, também é necessário preocupar-se com o grau de dificuldade ao elaborá-la. Senhas fáceis − como datas de aniversários de familiares ou placas de carro − são alvo de pessoas mal-intencionadas, já existindo muitos ataques a senhas baseados na exploração de informações pessoais. As senhas com sequências do tipo “123” também devem ser evitadas. De acordo com **Shay** et al. (2010), para criar uma **senha segura** é recomendável que os colaboradores observem as seguintes instruções: 

 

1- As senhas devem ter, pelo menos, **oito caracteres**. 

2- Deve-se **alterar as senhas com frequência** e **nunca as repetir**. 

3- Observar se houve algum tipo de vazamento de dados de determinados serviços. Caso tenha ocorrido, as **credenciais de acesso aos sistemas, equipamentos e demais recursos** devem ser modificadas para evitar que dados sejam obtidos por indivíduos mal-intencionados. 

4-Para aumentar a segurança das senhas, elas devem conter **letras maiúsculas e minúsculas, números e caracteres não alfanuméricos** (por exemplo: @, $, #). Ou seja, não se deve utilizar apenas letras ou números. 

5- As **senhas não devem conter nomes dos usuários e nem o nome da empresa** em que trabalham ou qualquer variação desse tipo. 

6- **Não utilizar a mesma senha para todas as contas**, em especial nas contas institucionais, pois, caso alguém descubra uma das senhas do usuário, não conseguirá acessar todos os serviços em que ele possui cadastro. 

7- **Nunca informar a senha a terceiros, nem as anotar em papel ou em arquivos digitais**, ou **inclui-las em um processo automático de acesso ao sistema**. Senhas devem ser sempre memorizadas e de uso estritamente pessoal, de modo a nunca serem compartilhadas ou acessíveis a terceiros. 

As recomendações que vimos são muito importantes para garantir que as **senhas** realmente atuem como um **mecanismo de segurança** para acesso dos indivíduos aos sistemas. Trata-se de recomendações simples que demandam disciplina e conscientização de todos os envolvidos no processo: tanto os responsáveis pelas políticas de criação e controle das senhas quanto os usuários que as utilizam para acessar os sistemas. 

 

### Treinamento 

 

Não importa o quão abrangentes sejam as defesas de segurança de uma organização e nem quanto foi investido em produtos de segurança eletrônica, essas defesas podem ser quebradas com um único e-mail de phishing. Você pode estar se perguntando: 

 

*O que é phishing?* 

É um tipo de fraude, que se dá por meios eletrônicos, utilizada por indivíduos mal-intencionados. 

É aplicada, principalmente, para roubar senhas de banco e outras informações pessoais, causando prejuízos materiais e morais, uma vez que os criminosos podem fazer compras e saques se passando pela vítima. 

 

Como ocorre? 

Pode ocorrer por meio de websites ou e-mails falsos muito parecidos com os de uma empresa com imagem consolidada no mercado de modo a atrair as vítimas. 

Os sites ou e-mails com phishing oferecem promoções para o usuário muito atrativas como: “Parabéns, você ganhou nossa promoção especial desse mês! Para receber seu prêmio, basta clicar no link e fornecer o que é solicitado.” 

Ou, ainda, solicitam que façam uma atualização dos dados bancários para evitar o cancelamento da conta, por exemplo. 

Perceba que, se um e-mail contendo um ataque de phishing chegar a um usuário que não possui um entendimento básico de segurança e ele responder à mensagem, um malware poderá ser instalado, ou o invasor poderá, ainda, acessar a rede por meio da análise do endereço de IP do usuário, causando um dano ainda maior para outros usuários. 

O risco desse tipo de ataque levou muitas organizações a desenvolverem um programa de conscientização sobre segurança. Ao ensinar a todos os funcionários as melhores práticas de segurança cibernética – da diretoria aos funcionários –, a postura de segurança pode ser bastante aprimorada e a vulnerabilidade a ataques de phishing e outros ataques cibernéticos pode ser bem reduzida. 

No entanto, simplesmente fornecer aos funcionários uma sessão de treinamento quando eles ingressam na empresa não é suficiente, tampouco tentar disseminar a segurança cibernética com apenas uma sessão anual de reciclagem. Não se espera que os funcionários mantenham o conhecimento por um longo período, a menos que sejam fornecidas sessões frequentes de atualização. Além disso, os cibercriminosos estão constantemente desenvolvendo novas estratégias para enganar os usuários. Os **programas de treinamento** devem estar contextualizados com o intuito de refletir a **realidade dos tipos de ataques**. 

A **ISO/IEC 27002 - Código de Prática para a Gestão de Segurança da Informação**, norma da **Associação Brasileira de Normas Técnicas (ABNT)**, trata de todos os aspectos necessários para garantir que as melhores práticas sejam aplicadas para a segurança da informação. Essa norma tem como objetivo dar suporte para a implantação, a manutenção e a melhoria contínua dos controles de segurança da informação, padronizando diretrizes e procedimentos para auxiliar na sua gestão. A norma ISO 27002 possui 133 controles, divididos em 11 seções, que abrangem a segurança da informação em todos os seus aspectos, tratando de ferramentas, processos e pessoas que são: 

* Política da Segurança da Informação: Prover orientação e apoio da direção para a segurança da informação de acordo com os requisitos do negócio e com as leis e regulamentações pertinentes. 

 

* Organizando a Segurança da Informação: Estrutura de gerenciamento para iniciar e controlar a implementação da segurança da informação na organização. 

 

* Gestão de Ativos: Alcançar e manter a proteção adequada dos ativos da organização. 

 

* Segurança em Recursos Humanos: Assegurar que os funcionários, fornecedores e terceiros entendam suas responsabilidades e estejam de acordo com os seus papéis, além de reduzir o risco de furto, roubo, fraude ou mau uso de recursos. 

 

* Segurança Física e do Ambiente: Prevenir acesso físico não autorizado, danos e interferências com as instalações e informações da organização. 

 

* Gestão das Operações e Comunicações: Garantir a operação segura e correta dos recursos de processamento da informação. 

 

* Controle de Acesso: Controlar o acesso à informação com base nos requisitos de negócio e segurança da informação. 

 

* Aquisição, Desenvolvimento e Manutenção de Sistemas de Informação: Garantir que a segurança seja parte integrante de sistemas da informação. 

 

* Gestão de Incidentes de Segurança da Informação: Assegurar que fragilidades e eventos de segurança da informação associados aos sistemas de informação sejam comunicados, permitindo a tomada de ação em tempo hábil. 

 

* Gestão da Continuidade do Negócio: Não permitir a interrupção das atividades dos negócios e proteger os processos críticos contra efeito de falhas ou desastres significativos e assegurar a sua retomada em tempo hábil. 

 

* Conformidade: Adequar os requisitos de segurança para não permitir a violação de regulamentações ou leis estabelecidas, além de obrigações contratuais. 

Com o objetivo de apoiar as **organizações** a **desenvolverem um programa eficaz de treinamento** em conscientização de segurança, são sugeridas as seguintes recomendações baseadas na **ISO/IEC 27002**: 

 

Obrigatoriedade do envolvimento da diretoria 

Todos os funcionários de uma organização são responsáveis por sua segurança, portanto, precisam estar comprometidos com as políticas de proteção dos dados. Dada a importância estratégica para a organização, espera-se que a diretoria entenda que a sua responsabilidade é maior do que a dos demais funcionários, pois tem direitos de acesso a dados e sistemas que, se caírem nas mãos de pessoas mal-intencionadas, podem causar grandes prejuízos. 

Se a diretoria não se interessar ativamente pela segurança e não perceber a importância do elemento humano nisso, é improvável que sejam fornecidos recursos suficientes e suporte adequado. O envolvimento de executivos na segurança cibernética também pode facilitar a criação de uma cultura de segurança na organização, estimulando a colaboração dos funcionários. 

Envolvimento de toda a organização 

É muito provável que a responsabilidade de desenvolver e implementar um programa de conscientização de segurança seja de uma única área. Essa atividade, porém, não pode ser feita sem o apoio dos demais setores. Os líderes dos diferentes departamentos podem ajudar a garantir que o programa de treinamento de conscientização sobre segurança receba a prioridade que merece. 

Para ajudar o departamento de TI (Tecnologia da Informação), os membros de outros departamentos podem ser treinados e colaborar com o fornecimento de suporte ou nos esforços de treinamento. Departamentos, como o de marketing, podem desenvolver conteúdo para boletins e outros materiais de treinamento. O departamento de RH (Recursos Humanos) pode ajudar com a definição de políticas e procedimentos. 

 

Criação de conteúdo para treinamento e conscientização de segurança 

Fala-se, cada vez mais, sobre a segurança da informação. Com o passar do tempo, os dados tornaram-se mais valorizados devido ao avanço das pesquisas em áreas como a de ciências de dados, por exemplo. Então, não é complicado encontrar cursos sobre esse assunto, que podem ser adaptados para a realidade das empresas, gerando, provavelmente, menor custo de produção interna de material de treinamento. 

 

Diversidade de treinamento 

O treinamento efetivo é um importante instrumento para criar uma cultura de segurança da informação dentro da organização. Nesse sentido, deve-se perceber que as pessoas respondem de maneira distinta aos diferentes métodos de treinamento. Alguns aprendem melhor com treinamento em sala de aula, outros podem precisar de treinamento individual e há aqueles que serão mais beneficiados com seminários periódicos de treinamento. 

O programa de treinamento, portanto, deve incluir uma ampla variedade de métodos tendo em vista os diferentes estilos de aprendizado. Quanto mais envolvente for o programa, maior será a retenção de conhecimento. Com a divulgação de material informativo por e-mail, jogos e questionários, haverá grandes melhorias na conscientização sobre segurança entre os funcionários. 

 

Exercícios de simulação 

A divulgação de conhecimento é uma etapa muito importante do treinamento. Por isso, é necessário garantir a capacitação dos funcionários para que eles possam aplicar os conhecimentos adquiridos a situações de seu cotidiano. A única maneira de determinar a eficácia do programa de treinamento é por meio de simulações de ataques. 

Exercícios de simulação de phishing e de outros cenários de ataque devem ser realizados em todas as etapas de treinamento. Com a aplicação desses exercícios, é possível medir a eficácia dos assuntos que foram tratados no programa de treinamento e fornecer o feedback necessário para identificar os pontos fracos e tomar medidas para a melhoria do treinamento. 

 

Periodicidade na realização do treinamento de conscientização de segurança 

O treinamento de conscientização de segurança deve ser feito periodicamente. Ao longo do ano, os funcionários devem estar envolvidos em diferentes atividades que os ajudem a fixar conhecimento, identificar pontos de melhoria e, principalmente, aplicar as boas práticas adquiridas ao seu cotidiano. O objetivo deve ser garantir que os problemas de segurança estejam sempre atualizados e contextualizados na realidade da organização. 

 

O treinamento é um importante instrumento para fortalecer o corpo funcional com o conhecimento necessário para evitar armadilhas que exponham a segurança da organização. 

 

Espera-se que os conhecimentos adquiridos nos treinamentos sejam traduzidos em ações diárias que priorizem o uso racional dos recursos com o objetivo de proteger os sistemas, os dados e os ambientes. Estamos falando dos mecanismos de proteção que serão abordados a seguir. 

 

### Mecanismos de proteção 

 

Trata-se do **conjunto de ações e recursos** que visa a **proteger um sistema ou uma organização**. Esses mecanismos são definidos considerando o ponto de vista da organização e dos sistemas. Vejamos: 

*Do ponto de vista da organização* 

Referem-se às restrições de comportamento de seus membros e de possíveis atacantes por meio de mecanismos como **portas, fechaduras, chaves e paredes**. 

 

*Do ponto de vista dos sistemas* 

A política de segurança aborda restrições de funções e de fluxo, entre elas, **restrições de acesso por sistemas externos e adversários**, incluindo programas e acesso a dados por pessoas. 

 

A seguir estão alguns exemplos de princípios que se aplicam aos mecanismos de proteção: 

1. Economia de mecanismo (objetividade do mecanismo): O projeto de um sistema deve ser o mais simples e pequeno possível para que possa ser facilmente analisado, testado e validado. Esse princípio se aplica a qualquer aspecto de um sistema, mas merece ênfase nos mecanismos de proteção, pois erros de processos e de implementação resultam em caminhos de acesso indesejados, ou seja, não serão notados durante o uso normal, uma vez que tentativas para fazer acessos inadequados não fazem parte do uso normal de um projeto.

2. Padrões à prova de falhas: O tipo de acesso que um usuário deve ter em um sistema deve ser feito com base na permissão e não na exclusão. Esse princípio significa que o padrão é a falta de acesso e o esquema de proteção identifica as condições sob as quais o acesso é permitido. Portanto, trata-se de um equívoco tentar identificar as condições sob as quais o acesso a um sistema deve ser recusado. Um projeto conservador deve ser baseado em argumentos sobre os motivos em que os objetos devem estar acessíveis e não por que não deveriam. Por exemplo, o servidor Apache ou Servidor HTTP Apache é o mais bem-sucedido servidor web livre que existe. Ele possui um arquivo de configuração chamado de **.htaccess**. A omissão de um parâmetro de uma chamada do sistema do controle de acesso no **.htaccess** do Apache deve resultar em menos permissão.

3. Mediação completa: todos os acessos a recursos, tanto diretos quanto indiretos, devem ser verificados pelos mecanismos de segurança. Eles devem ser organizados de forma a ser impossível contorná-los. Esse princípio, quando aplicado sistematicamente, é o principal fundamento do sistema de proteção. Ele dá uma visão geral do controle de acesso que, além de uma operação normal, inclui o início, a recuperação, o desligamento e a manutenção. Isso implica o desenvolvimento de um método para identificar a fonte de cada solicitação. Se ocorrer uma mudança de acesso, esses resultados deverão ser aualizados no sistema.

4. Projeto aberto: os mecanismos de segurança não devem depender da ignorância de possíveis invasores, mas da posse de chaves criptográficas ou de senhas, que garantem mais proteção para os sistemas. Essa dissociação permite que os mecanismos sejam exameinas opor muitos revisores sem a preocupação de que a própria revisão comprometa o que deve ser protegido. Além disso, qualquer usuário cético pode se convencer de que o sistema que ele está prestes a usar é adequado para seu objetivo. Por fim, não é realista tentar manter o sigilo de qualquer sistema que receba ampla distribuição.

5. Separação de privilégios: segundo Saltzer e Schroeder (1975), um mecanismo de proteção que requer duas chaves para desbloqueá-lo é mais robusto e flexível do que aquele que permite o acesso ao apresentador de apenas uma única chave. A relevância dessa observação para os sistemas de computador foi apontada por Roger Needham (1935-2003). O motivo é que, uma vez bloqueado o mecanismo, as duas chaves podem ser separadas fisicamente e diferentes programas, organizações ou indivíduos são responsáveis por elas. Assim, nenhum acidente, engano ou quebra de confiança é suficiente para comprometer as informações protegidas. Esse princípio é frequentemente usado em cofres de bancos. Também está em ação no sistema de defesa que dispara uma arma nucler apenas se duas pessoas diferentes derem o comando correto. Em um sistema de computador, chaves separadas se aplicam a qualquer situação em que duas ou mais condições sejam atendidas antes que o acesso seja permitido. Por exemplo, sistemas que fornecem tipos de dados protegidos extensíveis ao usuário geralmente dependem da separação de privilégios para sua implementação.

6. Privilégio mínimo: um privilégio define uma permissão individual associada a um nome autorizado, habilitando-o a acessar ou modificar um recurso do sistema. Os privilégios também podem ser concedidos a grupos de usuários. Por exemplo, o gerencimento de privilégios em um banco de dados é feito através da execução do comando GRANT no SQL. O princípio de privilégio mínimo diz que todos os programas e todos os usuários do sistema devem operar usando o menor conjunto de privilégios necessários para concluir o trabalho. Portanto, esse princípio limita os danos que podem resultar de um acidente ou erro. Desse modo, se for necessário investigar o uso indevido de um privilégio, o número de programas que deve ser auditado é reduzido.

7. Compartilhamento mínimo: diz respeito à minimização de recursos compartilhados entre diferentes programas, pois, se um programa pode corromper um recurso compartilhado, então ele pode corromper outros programas que dependem dele. Por exemplo, caso uma funcionalidade do sistema operacional possa ser implementada, como chamada ao núcle (system call), ou como função de biblioteca, deve-se preferir a última forma, já que envolve menos compartilhamento.

8. Aceitação psicológica: é essencial que a interface de um sistema seja projetada para facilitar o uso, para que os usuários apliquem rotineira e automaticamente os mecanismos de proteção. Além disso, à medida que o usuário associe o sistema aos mecanismos que ele deve usar, os erros serão minimizados. Por exemplo, alguns sistemas obrigam o usuário a cadastrar senhas muito complicadas que eles esquecem ou anotam, gerando uma vulnerabilidade para o sistema.

### Controles de acesso 

 

Imagine que uma empresa decidiu adquirir serviços de computação em nuvem e precisa determinar os níveis de acesso dos usuários aos recursos contratados. 

Como realizar esse procedimento? 

Através do controle de acesso, que é uma maneira de **limitar a abordagem** a um sistema ou a recursos físicos ou virtuais. Na computação, o controle de acesso é um modo pelo qual os **usuários recebem acesso** e certos privilégios a **sistemas, recursos ou informações**. 

Nos sistemas de controle de acesso, os usuários devem apresentar credenciais antes de obter o acesso. Essas **credenciais** podem ser de várias formas como, por exemplo, físicas, biométricas, senhas, portas eletrônicas. Existem **três tipos de sistemas de controle de acesso**: 

CONTROLE DE ACESSO DISCRICIONÁRIO (DAC): Nesse método, o administrador do sistema, dos dados ou de recursos protegidos define as políticas de quem tem permissão de acesso, ou seja, o sistema responsabiliza o proprietário da empresa por decidir quais pessoas são permitidas em um local específico, física ou digitalmente. 

O DAC é menos restritivo em comparação aos outros sistemas, pois permite, essencialmente, um controle completo individual sobre quaisquer objetos que se possua, bem como sobre os programas associados a esses objetos. A desvantagem do controle de acesso discricionário é o fato de fornecer ao usuário final o controle completo para definir configurações de nível de segurança para outros usuários. Além disso, as permissões concedidas ao usuário final são herdadas em outros programas usados, o que pode levar à execução de malware, ainda que o usuário final não esteja ciente disso. 

 

CONTROLE DE ACESSO OBRIGATÓRIO (MAC): De acordo com Red Hat (2020), esse mecanismo de segurança restringe o nível de controle dos usuários (sujeitos) sobre os objetos que eles criam. Diferentemente da implementação do DAC, em que os usuários têm controle total sobre seus próprios arquivos, diretórios etc., o MAC acrescenta rótulos ou categorias adicionais a todos os objetos do sistema de arquivos. Usuários e processos devem ter acesso apropriado a essas categorias antes de interagir com os objetos. 

Para entender melhor, o **sujeito** é normalmente um processo ou thread enquanto **objetos** são construções, como arquivos, diretórios, portas TCP/UDP, segmentos de memória compartilhada, dispositivos de entrada e saída. Sujeitos e objetos possuem um conjunto de atributos de segurança. Sempre que um sujeito tenta acessar um objeto, uma regra de autorização imposta pelo kernel do sistema operacional examina esses atributos de segurança e decide se o acesso pode ocorrer. 

CONTROLE DE ACESSO BASEADO EM FUNÇÃO (RBAC): Concede acesso com base em funções de negócios definidas e não na identidade do usuário. A meta é fornecer aos usuários somente o acesso a dados considerados necessários para exercer sua função nas organizações. Esse método é baseado em uma combinação de atribuições de funções, autorizações e permissões. 

 

Quando se trata da proteção dos recursos computacionais, os itens que devem ser contemplados são: **aplicativos e arquivos de dados**, além de **utilitários e o sistema operacional** das máquinas tanto dos usuários como da rede institucional.

*Aplicativos* 

Caso um usuário não autorizado tenha acesso ao código-fonte dos aplicativos, ele pode alterar o comportamento esperado do programa. Alguns exemplos desse tipo de fraude podem ocorrer em transações financeiras, onde o aplicativo é modificado para beneficiar o fraudador. 

 
 

*Arquivos de dados* 

As bases de dados, os arquivos ou as transações só podem ser alterados ou excluídos por usuários credenciados. Ainda assim, é muito importante que sejam implementados recursos de rastreabilidade para saber quem realizou cada operação no sistema. 

 
 

*Utilitários e sistema operacional* 

O acesso a utilitários deve ser restrito. Essas ferramentas são utilizadas para desenvolver e dar manutenção aos aplicativos e para configurar o sistema operacional. Caso um atacante tenha acesso a essas ferramentas e não haja mecanismos de proteção, comprometerá a segurança de todos os aplicativos, arquivos e sistema operacional. 

 
 

*Arquivos de senha* 

Os arquivos que armazenam as senhas precisam de um esquema de proteção adequado. Na ausência dessa proteção, uma pessoa não autorizada pode causar danos ao sistema. 

 
 

*Arquivos de log* 

São usados como mecanismos de rastreabilidade das ações realizadas pelos usuários nos sistemas. Portanto, é uma fonte de informação importante para auditorias futuras. Nos arquivos de logs estão os registros de quem acessou os recursos computacionais, quando isso foi feito e que tipo de operações foram realizadas. Uma pessoa mal-intencionada pode tentar acessar o sistema, apagar ou alterar dados, acessar aplicativos, alterar a configuração do sistema operacional para facilitar futuras invasões e, posteriormente, alterar os arquivos de log para que suas ações não possam ser identificadas, fazendo com que o administrador do sistema não perceba a invasão. 

 
Podemos dizer, então, que os objetivos dos controles de acesso são garantir: 

* O acesso aos recursos apenas por usuários autorizados. 

* Correspondência entre os recursos necessários e as atividades dos usuários. 

* Monitoramento e restrição do acesso a recursos críticos. 

* Execução de transações compatíveis com as funções e responsabilidades dos usuários. 

 

Diante de tudo o que vimos, podemos definir o controle de acesso em termos de: 

* Funções de identificação e autenticação de usuários 

* Alocação, gerência e monitoramento de privilégios 

* Limitação, monitoramento e desabilitação de acessos 

* Prevenção de acessos não autorizados 

Em relação à **identificação e autenticação** dos usuários nos sistemas, essas ações são feitas durante o **logon**. Esse processo permite conceder acesso aos dados e aplicativos em um sistema computacional e envolve a entrada de um **ID** (identificação do usuário), normalmente chamado de login, e uma **senha** (autenticação do usuário). 



1 A identificação define para o sistema **quem é o usuário**. 

2 A senha é um **autenticador**, ou seja, é o modo como o sistema verifica que o usuário é realmente quem ele diz ser. 



Devido à importância de entrar no sistema, o procedimento de logon deve divulgar o mínimo de informações que possam ser utilizadas por um invasor para conseguir identificar um usuário legítimo. Nesse sentido, um procedimento de logon eficiente deve: 

1- Informar que o **sistema** só deve ser **acessado por pessoas autorizadas**. 

2- **Não apresentar informações sobre o sistema** até que o processo de logon esteja completamente concluído. 

3- Não fornecer, durante o processo de logon, **mensagens de ajuda** que possam auxiliar um usuário não autorizado a acessar o sistema. 

4- **Validar os dados de entrada só após a conclusão do processo de logon**. O sistema não deve indicar qual parte do dado de entrada está correta ou incorreta, como, por exemplo, ID ou senha, caso ocorra algum erro. 

5- **Limitar a quantidade de tentativas** de logon sem sucesso, como, por exemplo, um máximo de três tentativas. 

6- **Guardar as tentativas de acesso inválidas** para futura verificação. 

7- **Forçar um tempo de espera antes de permitir novas tentativas** de entrada no sistema ou **rejeitar qualquer tentativa posterior de acesso** sem autorização específica. 

8- **Terminar as conexões** com o sistema. 

9- **Limitar o tempo para o procedimento de logon**. Se demorar, o sistema deverá encerrar o procedimento. 

10- Quando o procedimento de logon no sistema finalizar corretamente, mostrar as seguintes informações: 
  * **Data e hora** do último logon com sucesso; 
  * **Detalhes de qualquer tentativa de logon sem sucesso**, desde o último procedimento realizado com sucesso. 

A identificação do usuário deve ser única e pode ser composta por um código de caracteres (que é o caso mais comum, chamado de login), ou cartão inteligente (Smart Card), por exemplo. Desse modo, é possível fazer um controle das ações praticadas pelos usuários por meio dos logs. Após a identificação do usuário por meio do login, deve-se proceder à sua autenticação, isto é, o sistema deve confirmar se o usuário é realmente quem ele diz ser. 

 

### Política contra vírus 

 

Um **vírus de computador** é um **programa** carregado em qualquer computador — incluindo computadores pessoais e servidores — sem que o proprietário tenha o conhecimento da sua existência, sendo executado contra a sua vontade. Além disso, é um programa malicioso que faz cópia de si mesmo e infecta o computador e os arquivos. 

 

Atualmente, os vírus se dividem em várias categorias e cada uma apresenta diferentes objetivos e formas de ataques. A seguir, são apresentados alguns dos principais tipos de vírus de computador (GEEKS FOR GEEKS, 2020): 

* Vírus de arquivo: infecta o sistema anexando-se ao final de um arquivo e altera o início de um programa pra controlar o código do vírus, o controle retorna ao programa principal. Sua execução nem é notada. Também chamado de vírus parasitário, porque danifica os arquivos atacados.

* Vírus de boot: atinge o setor de inicialização do sistema, sendo executado durante essa estapa, antes do carregamento do sistema operacional. Esse vírus infecta outras mídias inicializáveis, como disco rígidos.

* Vírus de macro: é acionado quando um programa executa macro. Por exemplo, esse tipo de vírus pode estar contido em arquivos de planilha.

* Código-fonte vírus: procura o código-fonte e o modifica para incluir vírus e ajudar a espalhá-lo.

* Mutante: vírus programado para dificultar a detecção por antivírus, pois se altera a cada execução do arquivo contaminado.

* Polimórfico: é uma variação do vírus mutante que tenta dificultar a ação do antivírus ao mudar sua estrutura interna ou suas técnicas de codificação.

* Cavalo de troia (trojan): trata-se de programas aparentemente inofensivos que trazem embutido em si outro programa malicioso, ou seja, o vírus.

* Vírus multipartite: esse tipo de vírus é capaz de infectar várias partes de um sistema, incluindo o setor de inicialização, memória e arquivos. Isso dificulta a sua detecção e contenção.

* Vírus stealth: é um vírus muito complicado, pois altera o código usado para detectá-lo. Portanto, a sua detecção se torna muito difícil. Por exemplo, ele pode alterar a chamada do sistema de leitura para, sempre que o usuário solicite a leitura de um código modificado por vírus, a forma original do código ser mostrada em vez do código infectado.

* Vírus de encapsulamento: esse vírus tenta ignorar a detecção pelo antivírus, instalando-se na cadeia do manipulador de interrupções. Os programas de interceptação, que permanecem no fundo de um sistema operacional e capturam vírus, ficam desabilitados durante o curso de um vírus de encapsulamento. Vírus semelhantes instalam-se nos drivers de dispositivo.

* Vírus criptografado: usado para evitar a detecação por antivírus. Esse tipo de vírus existe na forma criptografada e carrega consigo um algoritmo de descriptografia. Assim, o vírus primeiro descriptografa e depois executa.

* Vírus blindado: é codificado para dificultar a identificação e o entendimento do antivírus. Usa uma variedade de técnicas para fazer isso, como enganar o antivírus e fazê-lo acreditar que o arquivo malicioso está em outro lugar que não seja a sua localização real. Também pode usar a compactação para complicar seu código.

Atente-se para as seguintes orientações: 

1- **Todos os computadores** conectados à rede de uma instituição devem ter um **antivírus padrão instalado**, programado para ser **executado em intervalos regulares**. Além disso, o software antivírus e os arquivos de definição de vírus devem ser sempre atualizados 

2- **Todos os computadores** devem ser **configurados** de forma a **agendar atualizações regulares** dos servidores antivírus centralizados dos serviços de rede 

3- **Todos os arquivos de dados e programas** que foram transmitidos eletronicamente para um computador de outro local, interno ou externo, devem ser **verificados** quanto à existência de vírus imediatamente após o recebimento. 

4- **Todos os dispositivos de armazenamento**, como, por exemplo, pen drives e HDs externos, são uma fonte potencial de vírus de computador. Portanto, eles devem ser **verificados** quanto à infecção por vírus antes de usá-los em um computador ou servidor da rede 

5- Os **computadores** e **servidores** de rede **nunca devem ser inicializados** a partir de um **dispositivo externo** recebido de uma fonte externa. 

6- O **software de proteção contra vírus** deve ser **carregado em cada computador e servidor** de rede como um programa residente para **monitorar constantemente** possíveis ataques de vírus e impedir que infectem a rede.

### Sistemas de Backup 

 

**Backup** é a criação de **cópias redundantes de informações**. Os sistemas de backups são utilizados como cópia de segurança de arquivos e dados. 

 

O ideal para uma empresa ou usuário é realizar o backup de todos os dados em tempo real, para garantir que não haverá a perda de dados. Na prática, no entanto, quase sempre é inviável aplicar essa recomendação devido à concorrência de atividades que fazem parte do cotidiano de uma empresa. No entanto, é muito importante que haja uma política específica para isso com a definição de responsáveis, periodicidade, locais de armazenamento e procedimentos de restauração, caso seja necessário. 

A organização também deve ter uma **periodicidade para a manutenção dos backups**, ou seja, por quanto tempo devem ser guardados e se existe alguma legislação que seja aplicável de forma específica. Por exemplo, no caso de instituições de ensino, um questionamento comum é sobre o período que o histórico escolar de um aluno será guardado. 

 

É importante que as empresas realizem **testes com os backups** a fim de garantir que os dados salvos possam ser restaurados e disponibilizados quando for preciso. 

 

Os backups são apenas um recurso de segurança usado para minimizar os problemas de uma companhia ou de um usuário em caso de perda de dados ou indisponibilidade nos sistemas. Quanto melhor for a política de backup (armazenamento e restauração de dados), menores serão os problemas para que a companhia possa continuar suas atividades. De acordo com Mayer (2017), existem alguns tipos de sistemas de backups, conforme apresentados a seguir: 

*Backup __completo__* 

Faz cópias de todos dados, inclusive dos logs de transações associadas para outro conjunto de mídia, como, por exemplo, disco rígido, DVDs, CDs, pen drives, entre outros, independentemente de terem sido modificados ou não. 

*Backup __incremental__*

Grava somente arquivos alterados desde o último backup, por isso é mais rápido que o backup completo e ocupa menos espaço. O último backup pode ser completo, diferencial ou incremental. No início, é feito um backup completo e nos subsequentes são copiados apenas os dados que foram alterados ou criados desde o último backup. 

*Backup __diferencial__* 

É a cópia dos dados criados e modificados desde o último backup. Após realizar o primeiro backup completo, cada backup diferencial compara o conteúdo a ser copiado com o do último backup completo e copia todas as alterações realizadas. Esse tipo de backup também é chamado de backup incremental cumulativo. 

 

Para garantir que as organizações possam continuar trabalhando em caso de perdas de dados, é extremamente recomendável possuir ferramentas conhecidas como Disaster Recovery. Essa infraestrutura tecnológica possibilita a operação da companhia em caso de falha de sistema. 

 

### Criptografia 

 

Criptografia consiste no ato de codificar dados para que apenas pessoas autorizadas consigam ter acesso às informações. 

 

Segundo Stallings (2008), a criptografia das informações pode ser classificada em três tipos: 

 

Criptografia de chave simétrica 

 

Também conhecida por **criptografia de chave privada ou secreta**. Aqui, o receptor da informação e o remetente usam uma única chave para criptografar e descriptografar a mensagem. O tipo frequente de criptografia usada nesse método é AES (Advanced Encryption System). Alguns exemplos de tipos de criptografia de chave simétrica são: Block, Block cipher, DES (Data Encryption System), RC2, IDEA, Blowfish e Stream cipher. A figura a seguir ilustra esse processo: 

![Chave simétrica](media/introducao-a-seguranca-da-informacao/chave-simetrica.png)


Criptografia de chave assimétrica 

 

Também denominada como **criptografia de chave pública**. Usando duas chaves, o remetente e o destinatário seguem os processos de criptografia e descriptografia. Uma chave privada é armazenada com cada pessoa e a chave pública é compartilhada na rede para que uma mensagem possa ser transmitida através de chaves públicas. O algoritmo mais comum de criptografia usado nesse método é o RSA. O método da chave pública é mais seguro do que o da chave privada. Alguns tipos de criptografia de chave assimétrica são: RSA, DAS, PKCs e técnicas de curva elíptica. A figura a seguir ilustra esse processo: 

![Chave assimétrica](media/introducao-a-seguranca-da-informacao/chave-assimetrica.png)


Função hash 

 

Usa uma função matemática para criptografar irreversivelmente as informações, fornecendo uma impressão digital delas. Esse tipo de criptografia é usada, principalmente, para garantir a integridade da mensagem. Alguns exemplos de algoritmos de hash são: Message Digest 5 (MD5), RIPEMD, Whirlpool e SHA (Secure Hash Algorithm). A figura a seguir ilustra esse processo: 

![Hash](media/introducao-a-seguranca-da-informacao/hash.png)

*Por que existem tantos tipos diferentes de criptografia? Por que não é possível fazer tudo o que é necessário com apenas um?* 

Porque cada esquema é **otimizado para aplicações criptográficas específicas**. 

 

*Você quer garantir a integridade dos dados?*

Use as **funções de hash**. Elas são adequadas para garantir a integridade dos dados, porque qualquer alteração feita no conteúdo de uma mensagem fará com que o receptor calcule um valor de hash diferente daquele colocado na transmissão pelo remetente. Como é altamente improvável que duas mensagens diferentes produzam o mesmo valor de hash, a integridade dos dados é garantida com muita confiança. 

 

*Você quer garantir a privacidade e confidencialidade?* 

Use a **criptografia de chave secreta**. Ela é ideal para criptografar mensagens, proporcionando privacidade e confidencialidade. O remetente pode gerar uma chave de sessão para criptografar a mensagem e o receptor precisará da mesma chave de sessão para descriptografá-la. 

 

*Você quer realizar a troca de chaves?* 

Use a **criptografia de chave pública**. Essa é uma importante aplicação desse tipo de criptografia. Esquemas assimétricos também podem ser usados para não repúdio e autenticação de usuário; se o destinatário puder obter a chave da sessão criptografada com a chave privada do remetente, somente esse remetente poderá ter enviado a mensagem. 

A criptografia de chave pública também poderia, teoricamente, ser usada para **criptografar mensagens**, embora isso raramente seja feito, pois os valores de criptografia de chave secreta geralmente podem ser calculados muito mais rápido que os valores de criptografia de chave pública. 

 

*Quais são as principais diferenças entre criptografia simétrica, assimétrica e de função hash?*

![Tabela de chaves](media/introducao-a-seguranca-da-informacao/tabela-chaves.png)

É recomendável a utilização de métodos criptográficos para proteger documentos confidenciais — cujo conteúdo seja de grande importância para a empresa — com o objetivo de garantir que apenas pessoas autorizadas tenham acesso a eles. Além de arquivos, também é possível criptografar mensagens de e-mail como forma de evitar o acesso de conteúdo sigiloso por terceiros não autorizados. A expectativa para o futuro é de maior aprimoramento dos métodos de criptografia para tornar os dados pessoais mais seguros e seus padrões mais confiáveis. 

 

### Certificado digital 

 

O **certificado digital** é um **documento eletrônico** que **identifica pessoas e instituições**, provando identidades e permitindo o acesso a serviços informatizados que garantam: 

AUTENTICIDADE 

INTEGRIDADE 

NÃO REPUDIO 

 

O certificado digital também é usado para assinar documentos digitalmente. Ele é destinado a qualquer pessoa, **física ou jurídica**, sendo emitido por uma **Autoridade Certificadora (AC)**. Com ele, pode-se anexar a chave pública, também chamada de infraestrutura de chave pública − do inglês Public Key Infrastructure (PKI) −, a um indivíduo ou entidade específica. Um certificado digital criptografado deve conter: 

* O nome do sujeito (a organização ou indivíduo certificado) 

* A chave pública do sujeito (usada para descriptografar mensagens e assinaturas digitais) 

* Um número de série (para identificar exclusivamente o certificado) 

* Uma data de validade 

* A assinatura digital da autoridade emissora do certificado e a mensagem 

* Qualquer outra informação relevante 

 

O caminho vinculado de verificação e validação de um certificado digital da entidade final para uma AC que atua como uma âncora de confiança é chamado de **cadeia de confiança**. Vejamos um exemplo de utilização de certificado digital: 

Os bancos possuem certificado para autenticar-se perante o cliente, assegurando que o acesso está realmente ocorrendo com o servidor deles (aqui cabe lembrar o nome dessa característica de segurança da informação: autenticidade). 

Em contrapartida, o cliente, ao solicitar um serviço, como, por exemplo, acesso ao extrato da conta corrente, pode utilizar o seu certificado para autenticar-se perante o banco. 

 

A figura a seguir mostra como os certificados digitais podem ser usados para validar a identidade de um provedor de conteúdo. Observe que os usuários de certificados digitais têm um vínculo de confiança comum com uma AC. Nele, é possível ver como o proprietário e o usuário do conteúdo trocam informações de identificação com a AC. Ambos possuem um relacionamento de confiança entre si. 

O usuário do conteúdo se registra na AC e recebe um certificado; o proprietário do conteúdo se registra na AC e recebe um par de chaves e um certificado assinado pela AC. Quando o usuário solicita informações de um proprietário do conteúdo, ele envia sua chave pública presente no certificado assinado. Como o usuário pode validar a assinatura no certificado usando a chave pública da AC, ele pode confiar no certificado e usar a chave pública fornecida pelo proprietário do conteúdo. 

![Certificado digital](media/introducao-a-seguranca-da-informacao/certificado-digital.png)

A certificação digital no Brasil tomou impulso a partir de 2001 quando o governo federal criou a **Infraestrutura de Chaves Públicas Brasileira (ICP-Brasil)**/*, que teve um grande crescimento desde então. Os certificados são utilizados em diversas aplicações: 

 

*É uma cadeia hierárquica de confiança que viabiliza a emissão de certificados digitais para identificação virtual do cidadão. 

 

* Automatização da prestação de informações fiscais à Receita Federal do Brasil 

* Nota fiscal eletrônica 

* Informatização do Poder Judiciário 

* Informatização de serviços cartoriais 

* Informatização de processos para abertura de empresas 

* Informatização de prontuários médico-odontológicos 

* Compras governamentais por meio de pregão eletrônico 

 

Os regulamentos sobre os quais se alicerça a ICP-Brasil são: Medida Provisória 2.200-2 (BRASIL, 2001), **decretos, resoluções do Comitê Gestor da ICP-Brasil, instruções normativas da AC Raiz, documentos complementares**. 

A Medida Provisória 2.200-2 (BRASIL, 2001) é o principal marco legal da ICP-Brasil. Publicada em 24 de agosto de 2001, tem força de lei, mesmo não tendo sido analisada no Congresso Nacional, uma vez que o mecanismo de caducidade das MPs não analisadas somente foi instituído pela Emenda Constitucional 32, de 11 de setembro de 2001. (BERTOL; SOUSA; PEOTTA, 2009) 

 

Cada usuário é responsável pela guarda e utilização de seu certificado digital, portanto, o **usuário nunca deve fornecer o certificado digital a terceiros**, pois é um documento pessoal e intransferível. Assim como outros documentos pessoais (CPF, RG e passaporte), não deve ser fornecido a terceiros por questões de segurança. 

 

Com o objetivo de forçar os usuários a atualizarem seus pares de chaves periodicamente, os certificados digitais possuem data de validade. Caso uma chave privada seja comprometida antes da data de vencimento, o certificado digital pode ser cancelado e o usuário poderá obter um novo par de chaves e certificado digital. Os certificados cancelados e revogados são colocados em uma lista de certificados de revogação − do inglês Certificate Revocation List (CRL) −, mantida pela autoridade de certificação que emitiu os certificados. (DEITEL; DEITEL; CHOFFNES, 2005) 

O comércio eletrônico ainda é considerado inseguro por uma grande parcela da população, principalmente pela falta de conhecimento e inexperiência no uso dos recursos computacionais e, com especial destaque, da internet. Mas é necessário entender que as transações que usam certificados digitais são mais seguras do que informações pessoais trocadas através de meios que não garantam segurança por si mesmos, como comprar por telefone, ou entregar um cartão de crédito a um vendedor. 

O avanço da ciência no desenvolvimento de algoritmos de criptografia mais robustos usados na maioria das transações on-line aumenta a segurança nas operações realizadas no mundo virtual. Cabe destacar que o usuário continua a ser o centro de todo esse desenvolvimento e é por meio da conscientização e educação nas boas práticas de segurança da informação que pode se sentir seguro e usufruir melhor das facilidades que a tecnologia pode fornecer no cotidiano. 
