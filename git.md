# Git - principais comandos

## Dicas

Ao criar um projeto prefira escolher a licensa MIT.

## Baixar um novo repositório

git clone <url> <nome-pasta>

## Alterando origin do projeto

Alterando a url do repositório

deleta a url raiz do repositório
git remote rm origin

verifica se tem origin
git remote -v

adiciona uma url nova
git remote add origin <nova-url>

## Comandos mais usados

Adiciona todos os arquivo a serem commitados
  
  git add .

Submeter todos os arquivos modificados
  
  git commit -am "<mensagem>"


Baixa todas modificações do repositório na branch master

    git pull origin master

Enviando todas as alterações para branch master

    git push origin master
  
Baixando dados da branch atual
  
    git pull
  
Enviando arquivos para branch atual
  
    git push

## Voltar versões

Mostra todos os passos do repositório (expira em 30 dias)

    git reflog

Mostra todos os commits de um branch
    
    git log

Recuperando arquivos com reflog

1. Podemos avançar e também retroceder nas hashs do reflog
2. Para isso utilizamos o comando
    
    git reset --hard <hash>

## Branches

Cria uma nova branch apartir da branch atual
    git checkout -b <nova-branch>

Atualiza todas as branches da sua maquina
    git fecth -a

Altera de branch
    git checkout <nome>

## Merge

Atualiza a branch atual com a branch master
    git merge master

## Stash

Coloca todas as alterações em uma lista na memória
    git stash

Listar todas as alterações na lista
    git stash list

podemos recuperar a stash com o comando
    git stash <nome>

## Trabalhando com tags no git

Cria uma nova tag
    git tag -a v2.0 -m “iniciando melhorias no pagamento”

Envia uma nova tag
    git push origin <nome-tag>

Envia todas as tags
    git push origin --tags

Lista todas as tags
    git tag

Mostra tudo sobre uma tag
    git show <nome-tag>

Alterar de tag
    git checkout <nome-tag>

Exemplo
    git commit -am "enviar alterações"
    git tag -a v2.0 -m "iniciando melhorias no pagamento"

## Submodulo - para utilizar um repositório dentro de outro

Mostra os submodulos
    git submodule

Adicionar um submodulo no seu repositório
    git submodule add <url> <pasta>

Atualiza o submodulo
    git push --recurse-submodules=on-demand

## git diff

Verificar diferenças de arquivos
    git diff <arquivo1> <arquivo2>

Verificar diferenças da sua branch com a master
    git diff master

Verificar diferenças de um arquivo depois de modificado
    git diff HEAD:a.txt a.text

## Melhorias no repositório

Verificar as últimas modificações do repositório
    git shortlog

Limpar arquivos não enviados
    git clean -f

Garbage collector - limpar arquivos desnecessários
    git gc

Verificar integridade dos arquivos
    git fsck

Compactar projeto para enviar para alguém
    git archive --format zip --output arquivo_master.zip master

### Removendo os commits com frases ruins 

Comando
    git rebase dev release
 
Para remover o texto de um commit altere de "pick" para "squash"
Para alterar o texto de um commit altere de "pick" para "reword"

Agora basta sair
    :x!
