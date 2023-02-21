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

***

Com o comando ``git branch`` podemos nos situar em qual branch estamos
