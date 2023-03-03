# Principais comandos do GIT

***

## Nome e email cadastrados
Podemos saber qual email ou nome de usuario foi cadastrado no git com os seguintes comandos:

```
git config user.name   //retorna o nome de usuario cadastrado
git config user.email  //retorna o email cadastrado 
```

***

## Iniciando um repositório
Para iniciarmos um repositório local, vamo utilizar o seguinte comando:
```
git init  //vai inicializar o repositório
```

***

## Commit

Os commits são basicamente o estado em que o projeto se encontra na linha do tempo. Ou seja, a versão do projeto naquele momento em que o commit foi criado.
 
Antes do commit, precisamos usar o comando ``git add 'arquivo'``(ou ``git add .`` para adicionar tudo) para pegar os arquivos não trackeados e prepará-los para serem commitados

Podemos então dar nosso commit com o seguinte comando:

```
git commit -m 'explique seu commit'  //Note que devemos deixar a informação sobre o commit o mais claro possivel 
```

 Com o comando ``git status`` vamos ver a situação atual do nosso projeto. esse comando trará informações uteis, como arquivos que já foram ou não commitados

Para ver a lista de todos os commits feitos na branch, usamos o comando ``git log``

Caso queira adicionar e fazer o commit de uma só vez, podemos usar o comando ``git commit -am 'comments'``

***
## Voltando atrás na história

Caso você queira voltar para a versão anterior do código, ou por acaso seu código que foi commitado gerou algum erro, você pode voltar atrás com o comando ``git reset``. Esse comando pode ser usado de 3 formas, dependendo da sua necessidade.
```
git reset --soft 'hash do commit'
git reset --mixed 'hash do commit'
git reset --hard 'hash do commit'
```

soft: volta para o estado anterior, porem com as modificações não commitadas
mixed: similar ao soft, porem antes das adições de arquivos (``git add``)
hard: vai ignorar todo o commit e adição anterior. tudo irá sumir do mapa

***
## Branchs

Com o comando ``git branch`` podemos nos situar em qual branch estamos

Para criar uma nova branch tambem é bem simples. Basta usar o comando ``git branch 'name_new_branch'``

Para trocar de branch, vamos usar ``git checkout 'branchName``. o nome da branch é aquela que queremos ir 

Para vermos o que foi mudado nos arquivos, podemos usar o comando ``git diff``

Caso queira mudar o nome da branch, basta usar o comando:
```
git branch -m nome_antigo nome_novo
```
*** 

## Conectando ao repositório do GitHub

Quando já tivermos nosso trabalho pronto, podemos mandá-lo para nosso repositório remoto no gitHub. Para fazer isso é bem simples, vamos usar o seguinte comando:

```
git remote add origin https://github.com/italo-vinicius/Git-Conceitos-Basicos //conecta ao repositório remoto
git push -u origin main //envia os arquivos para o repositório
```

***

## Git Ignore

Caso você não queira que algum dado sensivel vá para o repositório remoto, você pode usar o arquivo ``.gitignore`` . Nesse arquivo, podemos colocar arquivos que serão ignorados ao darmos o commit

Podemos escrever os arquivos que queremos ignorar de algumas formas diferentes. Segue exemplos:
```
index.php  //ignora o arquivo index.php em especifico
*.php  //ignora todos os arquivos php
Users/ //ignora o diretório Users
```

***

## Git revert

O grande salvador das sextas-feiras, esse comando pode ser usado para 'dar um commit descommitando' no projeto. Caso você queira voltar um commit por algum motivo, mas sem perder o commit atual, você pode estar utilizando o git revert da seguinte forma:

```
git revert --no-edit hash_do_commit_desejado 
```

Ou seja, vai voltar para o commit que foi passado a hash, porem o commit que estava vai permanecer para ser acessado depois

***

## Deletar branchs remotas e locais

Caso queira deletar alguma branch remota, use o comando ``git push origin :namebranch``

E caso queira deletar uma branch local, primeiro saia dela e depois use o comando ``git branch -D nomeBranch``

***

## Pull

O pull serve para receber dados do repositório remoto e trazer para o local, ou seja, manter o sistema local atualizado caso o remoto tenha sofrido alguma alteração. Para fazermos o pull, usamos o comando ``git pull origin namebranch``

O pull tambem trás todas as informações de log

***

## Clone

Com o comando de clone, podemos clonar alguns projetos do github e fazer contribuições. Nesse caso, usaremos o comando ``git clone https://github.com/arquivosfodas``, especificando o link do projeto

***

## Contribuindo com projetos

Para contribuir em projetos, primeiro vamos dar um fork. Após isso, daremos o ``git clone`` no projeto e traremos ele para nossa maquina. A partir dai, podemos fazer qualquer alteração que achamos ser necessária. Após isso, vamos dar um push no projeto

```
NOTA:
Caso queira ver o nome do projeto(a grande maioria é 'Origin'), basta usar o comando git remote -v
```

Após o push, vá ao gitHub e crie um pull request no projeto
