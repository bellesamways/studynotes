## Aula 1 - Princípios da segurança e o ciclo de vida da informação

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