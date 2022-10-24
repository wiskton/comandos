# Git - Principais comandos

Meu helper de comandos para consulta rápido sobre git.

## Dicas

Ao criar um projeto prefira escolher a licensa MIT.

## Baixar um novo repositório

```bash
git clone <url> <nome-pasta>
```

## Alterar o origin do projeto

1. Deletar o origin do repositório

```bash
git remote rm origin
```

2. Verificar se o origin foi removido

```bash
git remote -v
```

3. Adicionar o novo origin

```bash
git remote add origin <url>
```

## Comandos mais usados

Adicionar todos os arquivo a serem enviados

```bash
git add .
```

Submeter todos os arquivos modificados
  
```bash
git commit -am "<mensagem>"
```
  
Baixar modificações da branch atual
  
```bash
git pull
```
  
Enviar modificações para branch atual
  
```bash
git push
```

Baixa todas as modificações do repositório da branch master

```bash
git pull origin master
```

Enviar todas as alterações para branch master

```bash
git push origin master
```

## Voltar versões

Mostrar passa a passo do repositório (expira em 30 dias)

```bash
git reflog
```

Mostrar todos os commits de um branch
    
```bash
git log
```

Recuperar arquivos com reflog

1. Podemos avançar e também retroceder nas hashs do reflog
2. Para isso utilizamos o comando
    
```bash
git reset --hard <hash>
```

## Branches

Criar uma nova branch apartir da branch atual

```bash
git checkout -b <nova-branch>
```

Atualizar todas as branches da sua maquina

```bash
git fecth -a
```

Alterar de branch

```bash
git checkout <nome>
```

## Merge

Atualiza a branch atual com a branch master

```bash
git merge master
```

## Stash

Coloca todas as alterações em uma lista na memória

```bash
git stash
```

Listar todas as alterações na lista

```bash
git stash list
```

Recuperar os dados do stash com o comando

```bash
git stash <nome>
```

## Tags

Criar uma nova tag

```bash
git tag -a v2.0 -m "iniciando melhorias no pagamento"
```

Enviar uma nova tag
```bash
git push origin <nome-tag>
```

Enviar todas as tags

```bash
git push origin --tags
```

Listar todas as tags

```bash
git tag
```

Mostrar tudo sobre uma tag

```bash
git show <nome-tag>
```

Alterar para uma tag especifica

```bash
git checkout <nome-tag>
```

### Exemplo de como usar

```bash
git commit -am "enviar alterações"
git tag -a v2.0 -m "iniciando melhorias no pagamento"
```

## Submodulo - Quando precisa utilizar um repositório dentro de outro

Mostrar os submodulos

```bash
git submodule
```

Adicionar um submodulo do seu repositório

```bash
git submodule add <url> <pasta>
```

Atualizar o submodulo

```bash
git push --recurse-submodules=on-demand
```

## Diff

Verificar diferenças de arquivos

```bash
git diff <arquivo1> <arquivo2>
```

Verificar diferenças da sua branch com a master

```bash
git diff master
```

Verificar diferenças de um arquivo depois de modificado

```bash
git diff HEAD:a.txt a.text
```

## Melhorias no repositório

Analisar as últimas modificações do repositório em resumo

```bash
git shortlog
```

Limpar arquivos não enviados

```bash
git clean -f
```

Garbage collector - Limpar arquivos desnecessários

```bash
git gc
```

Verificar a integridade dos arquivos

```bash
git fsck
```

Compactar projeto para enviar para alguém

```bash
git archive --format zip --output arquivo_master.zip master
```

### Removendo os commits com frases ruins 

Comando para alterar commits com textos indesejados em cima de duas branches

```bash
git rebase dev release
```
 
Para remover o texto de um commit altere de "pick" para "squash"
Para alterar o texto de um commit altere de "pick" para "reword"

Agora basta sair

```bash
:x!
```
