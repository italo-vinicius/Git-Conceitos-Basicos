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

Caso queira adicionar e fazer o commit de uma só vez, podemos usar o comando ``git commit -ad 'comments'``

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
*** 

## Conectando ao repositório do GitHub

Quando já tivermos nosso trabalho pronto, podemos mandá-lo para nosso repositório remoto no gitHub. Para fazer isso é bem simples, vamos usar o seguinte comando:

```

```