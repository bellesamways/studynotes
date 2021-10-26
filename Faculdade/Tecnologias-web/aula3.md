# Aula 3 - Segurança na internet

**Hackers**: São grandes administradores de sistemas, especialistas com habilidade suficiente para descobrir problemas de segurança e operação em aplicativos ou em sistemas operacionais que se divertem em atacar uma rede. Eles se justificam dizendo trabalharem pelo prazer na superação dos limites. Existem diversos sub-tipos de hackers: White hat, Grey hat, Black hat, Newbie, Phreaker, Cracker e Lammer.

**Crackers**: Eles utilizam suas habilidades para o mal. Se aproveitam da falha dos sistemas para roubarem, chantagearem ou darem prejuízo a terceiros sejam estes pessoas físicas ou jurídicas. São os “quebradores” de sistemas. Um termo genérico para “Black hat”.

**Lammers**: São iniciantes na arte da invasão que se apropriam de códigos ou táticas explicitados em revistas e sites para atacarem computadores sem saber, às vezes, o que estão fazendo. Eles simplesmente executam algo que não sabem como funciona. Quando as tentativas de invasão são bem-sucedidas se auto-denominam hackers.

## Tipos de ataque

### Cavalo de Tróia

Este é um dos ataques mais comuns que há. Você pode receber um arquivo anexo em seu e-mail, por exemplo, indicando um link e acabar baixando um programa invasor ou, ainda, executar um programa anexo ao e-mail acreditando ser uma apresentação ou uma imagem.

São do tipo **Backdoor** que utilizam conexão direta ou reversa entre a máquina alvo e o servidor do invasor.

Outro tipo de cavalo de tróia, ou **trojan**, se destina a roubar senhas de bancos e aplicativos dos usuários da máquina alvo. Eles conseguem até monitorar a sequência do mouse nos teclados de senhas. Estes são do tipo **Keylogger**.

Alguns trojans populares são NetBus, Back Orifice e SubSeven.

### Quebra de Senha

Este tipo de invasão trabalha com a missão de crackear, ou seja, quebrar as senhas de sistemas e usuários, utilizando técnicas de dicionários de palavras ou, ainda, uma técnica chamada “força bruta”. A quebra de senhas é uma das tarefas que mais divertem os lammers, pois muitos scripts rodam durante dias e noites até encontrarem a senha desejada.

### Denial Of Service (DOS)

Este ataque se caracteriza pela utilização de computadores de usuários comuns para em um determinado momento sobrecarregarem um servidor com uma quantidade excessiva de solicitações de serviços tirando-os do ar.

Este tipo de ataque traz uma vantagem ao atacante, pois pulveriza as pistas que levariam ao autor principal. Sites como CNN, Yahoo!, ZD Net, AOL, Twitter, Facebook, Google blogs já sofreram este tipo de ataque.

Os invasores implantam, nas máquinas dos usuários, programas zumbis que ficam aguardando a ordem de atacar coletivamente em uma determinada data.

### Mail Bomb

Esta técnica é muito popular. O invasor sobrecarrega o servidor de mensagens de correio eletrônico com mensagens, fazendo com que este pare de responder pelo acúmulo de carga de serviço.

### Phreaking

No passado, este tipo de invasão era bastante comum. Muitos usuários divulgavam métodos para burlar as empresas telefônicas e garantir ligações gratuitas ou a baixo custo.

Ainda hoje, estas técnicas são utilizadas em diversos países tanto para fixos quanto para celulares, mas ficaram restritas a especialistas.

### Spoofing

Esta técnica consiste em atacar um computador através de outro, fazendo com que o administrador do sistema pense que o computador que está atacando é aquele no final da comunicação, escondendo as informações do endereço IP do computador de origem.

### Scamming

O intuito deste ataque é roubar senhas de bancos enviando ao usuário uma página simulando o site do banco do mesmo.

Este é um dos ataques que mais logra êxito, pois muitos usuários não reparam no endereço da URL, nem mesmo no cadeado do site.

## COMO DIFICULTAR A QUEBRA DE SENHAS

  - Nunca utilize senhas com menos de 6 caracteres, pois a combinação destes já dá mais trabalho ao invasor.

  - Não utilize dados pessoais em suas senhas, tais como nomes de pessoas, animais de estimação, ou datas de aniversário.

  - Utilize letras Maiúsculas combinadas com Minúsculas para dificultar a vida dos invasores. Ex: AlOjPpKj.

  - Inclua números em suas senhas. Ex: A0l2yu7sIa.

  - Inclua caracteres especiais. Ex: Al156@ty%67

  - Utilizar um gerenciador de senhas é uma ótima opção, nele dá pra gerar senhas dificílimas que jamais seriam quebradas.

## COMO DIFICULTAR O ROUBO DE INFORMAÇÕES VIA E-MAIL

O e-mail é uma carta e, desta forma, deve ser revisada antes de ser encaminhada.

Muitas pessoas demonstram, ao responder um e-mail, total displicência com relação à forma, ao conteúdo e às informações nele contidas.

O invasor se vale desta pressa para poder levantar dados dos usuários a serem atacados.

1. Não divulgue seu e-mail corporativo em listas, correntes ou outros locais fora do ambiente de trabalho.

2. Preste atenção na assinatura automática do seu e-mail.

3. Preencha seu e-mail com calma.

4. Utilize CCO ou BCC, isto é, poste com cópia oculta para não revelar aos invasores a lista dos copiados.

5. Utilize assinaturas digitais.

6. Utilize e-mails, principalmente para dentro da empresa, criptografados.

## CRIPTOGRAFIA

É a tecnologia que tenta manter em segredo mensagens em trânsito.

Os objetivos da criptografia é manter a confiabilidade da mensagem, mantendo-a íntegra, autenticando, dessa forma, o remetente que não poderá negar a autenticidade da mesma.

**Chave Simétrica**: Onde tanto o emissor quanto o receptor compartilham a mesma chave. O aspecto negativo dessa técnica é o gerenciamento seguro da chave.

**Chave Pública**: A criptografia assimétrica procura corrigir o problema do gerenciamento seguro da chave utilizado pela chave simétrica, pois nela a chave de criptografia é diferente da chave de descriptografia. O PGP pode ser utilizado por qualquer pessoa que cria uma chave pública e uma chave privada para si, divulgando somente a chave pública. Existem servidores que armazenam esta chave pública gratuitamente como o servidor da RNP.
