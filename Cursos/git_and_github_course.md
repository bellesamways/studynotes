# Git e Github

Anotações do curso: https://www.udemy.com/share/1000cwBUEdeV1XRXg=/


## Instalando o git

git-scm.com/download

linux já vem instado


## Config inicial do git
- guarda as infos no git config do sistema todo, do usuário e do projeto.
- config global é do usuário

    - git config --global user.name "Seu nome"
    - git config --global user.email "seuemail@gmail.com"
    - git config --global core.editor [comando do editor]
    - git config user.name (responde com o seu nome)
    - git config user.email (responde com o seu nome)
    - git config --list (mostra uma lista de informações do seu git)

## Inicializando um repositório
- mkdir git-course (pra criar uma pasta)
- cd git-course/ (entrar na pasta)
- git init (inicializa um repositório vazio)
- ls -la (mostra todos os diretórios que tem no repositório)
- cd .git/ (entra no diretório)
- ls (lista todas as pastas que tem no diretório)
- cd .. (volta 1)

## Usando o editor do terminal
- vi Readme.md (iniciar o arquivo pra edição)
- aperta i e entra no modo insert
- agora escreve tudo que quer
- aperta esc, sai do modo de inserção
- aperta dois pontos (iniciar algum comando)
- w (escrever e salvar)
- q (sair)
- apertar enter e sai do modo de edição


## Ciclo de vida dos status dos arquivos
- untracked: arquivo acabou de ser adicionado, mas o git ainda não conhece dentro do repositório nenhuma versão
  - *adiciona arquivo no git*
- unmodified: existe no git, mas nao tem modificação
  - *modifica o arquivo*
- modified: arquivo modificado
  - *jogar o arquivo para área onde vai ser criada a versão*
- staged: fica com todos os arquivos modificados para poder commitar
- git status (reporta como o repositório esta nesse momento)
- git add (tira do modified e coloca no staged)
- git commit -m "mensagem" (criar uma versão)


## Visualizando logs
- git log (mostra o hash do commit, quem foi o autor dele, e a mensagem do commit)
- git log --decorate (mostra mais detalhes)
- git log --author="nome" (filtra por autor de commit)
- git shortlog (mostra em ordem alfabetica todos os autores, quantos commits e quais fizeram)
- git shortlog -sn (mostra só o nome e a quantidade de commits)
- git log --graph (mostra de forma gráfica oq ta acontecendo com os branchs e as versões)
- git show [hash] (mostra tudo que foi feito naquele commit)


## Visualizando o diff
- git diff (mostra a modificação que rolou naquele commit)
- git diff --name.only (mostra só o nome do arquivo que foi modificado)

## Desfazendo coisas
- git checkout [nome do arquivo] (retorna o que o arquivo era até antes da edição)
- quando o arquivo já está no staged
  - git reset HEAD [nome do arquivo] (ele tira o arquivo do staged)
- quando o arquivo já foi commitado
    - git reset --soft (mata o commit, mas o arquivo fica no staged)
    - git reset --mixed (mata o commit, volta o arquivo para modified)
    - git reset --hard (ignora a existencia do commit e tudo que existe nele, mata tudo)

## Criando um repositório no Github
*Normal pelo github*


## Criando e adicionando uma chave SSH
https://help.github.com/en/articles/connecting-to-github-with-ssh


https://help.github.com/en/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent


Generating a new SSH key

- Open Terminal.
- Paste the text below, substituting in your GitHub email address.
      $ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
This creates a new ssh key, using the provided email as a label.

- Generating public/private rsa key pair.
When you're prompted to "Enter a file in which to save the key," press Enter. This accepts the default file location.
      Enter a file in which to save the key (/home/you/.ssh/id_rsa): [Press enter]
At the prompt, type a secure passphrase. For more information, see "Working with SSH key passphrases".
      Enter passphrase (empty for no passphrase): [Type a passphrase]
      Enter same passphrase again: [Type passphrase again]

Adding your SSH key to the ssh-agent

Rode:

    $ ssh-add ~/.ssh/id_rsa

Copie o SSH para a área de tranferência utilizando o xclip, para instalá-lo e copiar execute os seguintes comandos:

Linux | Ubuntu

    $ sudo apt-get install xclip

Então rode:

    $ xclip -sel clip < ~/.ssh/id_rsa.pub

- Agora na sua página do GitHub vá até o menu Settings.
- Clique em "SSH and GPG keys" na lateral esquerda.
- Ou acesse diretamente este link: https://github.com/settings/keys
- Clique no botão "New SSH Key", preencha o título à sua escolha, geralmente o nome da máquina.
- E cole o SSH que está na sua área de transferência na caixa de texte "Key", se precisar coloque sua senha novamente.

## Ligando um repositório local a um remoto
- git remote add origin [colar o ssh]
- git push -u origin master (envia os arquivos locais para o repositório remoto)

## Enviando mudanças para um repositório remoto
- git push origin [branch]


## Clonando repositórios remotos
- mkdir [nome do diretório] OU cd [nome do diretório]
- git clone [ssh]

## Fazendo um fork de um projeto
Fork é para projetos que não são seus, direto pelo github

## O que é um branch e pra que usar?
Branch é um ponteiro móvel que leva a um commit
Vantagens:
* Poder modificar sem alterar a master
* facilmente desligável
* múltiplas pessoas trabalhando
* evita conflitos

## Criando um branch
- git checkout -b [nome da branch] (cria a branch)
- git branch (mostra em que branch eu to)


## Movendo e deletando branches
- git checkout [nome da branch] (muda de branch)
- git branch -D [nome da branch] (apaga a branch)

## Entendendo o merge
- Sempre que eu for fazer o merge de uma branch na master, ele cria um commit para juntar os dois.
- Cria um ciclo.
- Merge é uma operação não destrutiva, ele cria um commit novo para juntar tudo.
- Parte ruim é que sempre cria um commit extra sem sentido e o histórico fica poluído.

## Entendendo o rebase
- Não cria um ciclo, permanece tudo linear.
- Evita commits extras e mantém o histórico linear.
- O ruim é que perde a ordem cronológica. (Pega o commit e põe no início da fila, sem se preocupar se foi feito antes ou depois)
- Criando o .gitignore
- Ignorar e não trackear alguns arquivos.
https://git-scm.com/docs/gitignore
https://github.com/github/gitignore

## Git stash é lindo
Guarda os arquivos que não foram commitados num arquivinho que eu posso chamar quando necessário.
- git stash (guarda tudo numa sacolinha)
- git stash apply (aplica as mudanças que tinha guardado)
- git stash list (mostra a lista de todos os stashes q eu tiver fazendo)
- git stash clear (limpa tudo que tiver no stash)


## Alias pra que te quero
Atalhos dos comandos

- git config --global alias.[atalho] [nome do comando que ele executa]
  - exemplo: git config --global alias.co checkout

## Versionando com tags
Serve para criar versões diferentes de tudo.
- exemplo:
git tag -a 1.0.0 -m "comentário"

- para subir isso:
git push origin master --tags


isso fica em releases no github


## Revert
- git revert [commit que deu pau]

ele reverte o commit e apaga o que vc fez nele, mas não sumiu com o commit anterior.

## Apagando tags e branches de repositórios remotos
- git push origin :[tag ou branch que quero apagar]
