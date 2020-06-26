# Git e Github

[Anotações do curso](https://www.udemy.com/share/1000cwBUEdeV1XRXg=/)

## Instalando o git

- git-scm.com/download
- no linux já vem instado, geralmente.

## Config inicial do git

- guarda as infos no git config do sistema todo, do usuário e do projeto.
- config global é do usuário

- `git config --global user.name "Seu nome"`
- `git config --global user.email "seuemail@gmail.com"`
- `git config --global core.editor [comando do editor]`
- `git config user.name` (responde com o seu nome)
- `git config user.email` (responde com o seu nome)
- `git config --list` (mostra uma lista de informações do seu git)

## Inicializando um repositório

- `mkdir git-course`: para criar uma pasta
- `cd git-course/`: entrar na pasta
- `git init`: inicializa um repositório vazio
- `ls -la`: mostra todos os diretórios que tem no repositório
- `cd .git/`: entra no diretório
- `ls`: lista tudo que tem no diretório
- `cd ..`: volta 1

## Ciclo de vida dos status dos arquivos

- **untracked**: arquivo acabou de ser adicionado, mas o git ainda não conhece dentro do repositório nenhuma versão
  - *adiciona arquivo no git*
- **unmodified**: existe no git, mas não tem modificação
  - *modifica o arquivo*
- **modified**: arquivo modificado
  - *jogar o arquivo para área onde vai ser criada a versão*
- **staged**: fica com todos os arquivos modificados para poder commitar
- `git status`: reporta como o repositório esta nesse momento
- `git add`: tira do modified e coloca no staged
- `git commit -m "mensagem"`: criar uma versão

## Visualizando logs

- `git log`: mostra o hash do commit, quem foi o autor dele, e a mensagem do commit
- `git log --decorate`: mostra mais detalhes
- `git log --author="nome"`: filtra por autor de commit
- `git shortlog`: mostra em ordem alfabética todos os autores, quantos commits e quais fizeram
- `git shortlog -sn`: mostra só o nome e a quantidade de commits
- `git log --graph`: mostra de forma gráfica oq ta acontecendo com os branchs e as versões
- `git show [hash]`: mostra tudo que foi feito naquele commit


## Visualizando o diff

- `git diff`: mostra a modificação que rolou naquele commit
- `git diff --name.only`: mostra só o nome do arquivo que foi modificado

## Desfazendo coisas

- `git checkout [nome do arquivo]`: retorna o que o arquivo era até antes da edição

- quando o arquivo já está no staged
  - `git reset HEAD [nome do arquivo]`: ele tira o arquivo do staged

- quando o arquivo já foi commitado
  - `git reset --soft`: mata o commit, mas o arquivo fica no staged
  - `git reset --mixed`: mata o commit, volta o arquivo para modified
  - `git reset --hard`: ignora a existencia do commit e tudo que existe nele, mata tudo

## Criando um repositório no Github

*Normal pelo github*


## Criando e adicionando uma chave SSH

Links de referência: 
- [Github help 1](https://help.github.com/en/articles/connecting-to-github-with-ssh)
- [Github help 2](https://help.github.com/en/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

### Gerando uma nova chave SSH

- Abra o terminal
- Cole o texto abaixo, substituindo o seu email do Github.

`ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`

Isso cria uma nova chave SSH, usando o email como uma label.

- Gerando um par de chave RSA publica/privada.
- "Enter a file in which to save the key," aperte Enter. Isso aceita o padrão de onde fica o arquivo.

`Enter a file in which to save the key (/home/you/.ssh/id_rsa): [Press enter]`

- Escreva uma frase de segurança. Para mais informações, veja "Working with SSH key passphrases".

`Enter passphrase (empty for no passphrase): [Type a passphrase]`

`Enter same passphrase again: [Type passphrase again]`

- Adicionando sua chave SSH no ssh-agent:

`ssh-add ~/.ssh/id_rsa`

- Para copiar MANUALMENTE sua chave SSH:

`cat ~/.ssh/id_rsa.pub`

- OU copie o SSH para a área de tranferência utilizando o xclip, para instalá-lo e copiar execute os seguintes comandos:

Linux | Ubuntu

`sudo apt-get install xclip`

- Então rode:

`xclip -sel clip < ~/.ssh/id_rsa.pub`

- Agora na sua página do GitHub vá até o menu **Settings**.
- Clique em "SSH and GPG keys" na lateral esquerda.
- Ou acesse diretamente este link: https://github.com/settings/keys
- Clique no botão "New SSH Key", preencha o título à sua escolha, geralmente o nome da máquina.
- E cole o SSH que está na sua área de transferência na caixa de texte "Key", se precisar coloque sua senha novamente.

## Ligando um repositório local a um remoto

- `git remote add origin [colar o ssh]`
- `git push -u origin master`: envia os arquivos locais para o repositório remoto

## Enviando mudanças para um repositório remoto

- `git push origin [branch]`

## Clonando repositórios remotos

- `git clone [ssh]`

## Fazendo um fork de um projeto

Fork é para projetos que não são seus, direto pelo Github.

## O que é um branch e pra que usar?

Branch é um ponteiro móvel que leva a um commit.

Vantagens:

* Poder modificar sem alterar a master
* Facilmente desligável
* Múltiplas pessoas trabalhando
* Evita conflitos

## Criando um branch

- `git checkout -b [nome da branch]`: cria a branch
- `git branch`: mostra em que branch eu tô

## Movendo e deletando branches

- `git checkout [nome da branch]`: muda de branch
- `git branch -D [nome da branch]`: apaga a branch

## Entendendo o merge

- Sempre que eu for fazer o merge de uma branch na master, ele cria um commit para juntar os dois.
- Cria um ciclo.
- Merge é uma operação não destrutiva, ele cria um commit novo para juntar tudo.
- Parte ruim é que sempre cria um commit extra sem sentido e o histórico fica poluído.

## Entendendo o rebase

- Não cria um ciclo, permanece tudo linear.
- Evita commits extras e mantém o histórico linear.
- O ruim é que perde a ordem cronológica. (Pega o commit e põe no início da fila, sem se preocupar se foi feito antes ou depois)

## Criando o .gitignore

- Ignorar e não trackear alguns arquivos.

[Git SCM](https://git-scm.com/docs/gitignore)

[Github](https://github.com/github/gitignore)

## Git stash é lindo

Guarda os arquivos que não foram commitados num arquivinho que eu posso chamar quando necessário.

- `git stash`: guarda tudo numa sacolinha
- `git stash apply`: aplica as mudanças que tinha guardado
- `git stash list`: mostra a lista de todos os stashes que eu tiver fazendo
- `git stash clear`: limpa tudo que tiver no stash

## Alias pra que te quero :heart:

Atalhos dos comandos

- `git config --global alias.[atalho] [nome do comando que ele executa]`
  - exemplo: `git config --global alias.co checkout`

## Versionando com tags

Serve para criar versões diferentes de tudo.

- exemplo: `git tag -a 1.0.0 -m "comentário"`

- para subir isso: `git push origin master --tags`

Isso fica em releases no github

## Revert

- `git revert [commit que deu pau]`

Ele reverte o commit e apaga o que você fez nele, mas não sumiu com o commit anterior.

## Apagando tags e branches de repositórios remotos

- `git push origin :[tag ou branch que quero apagar]`

## Emoticons em commits

Emoticons em commit pode trazer uma visibilidade instantânea sobre o que se trata o mesmo.

Nos commits ele pode trazer os seguintes significados:

:art: Ao melhorar o formato / estrutura do código

:rocket: Ao melhorar o desempenho

:pencil2: Ao escrever documentos

:bulb: Nova ideia

:construction: Trabalho em andamento

:heavy_plus_sign: Ao adicionar recurso

:heavy_minus_sign: Ao remover o recurso

:speaker: Ao adicionar log

:mute: Ao reduzir o log

:bug: Ao corrigir um bug

:white_check_mark: Ao adicionar testes

:lock: Quando se lida com segurança

:arrow_up: Ao atualizar dependências

:arrow_down: Ao desatualizar dependências

Para ver mais, acesse [aqui](https://gitmoji.carloscuesta.me/).

###### O.B.S.: Nem todas plataformas aceitam emojis.