### 3.Configurando o GIT

Existem 3 tipos de configuração:

#### 3.1-System
Esta configuração é válida para todos os usuários do sistema em todos os seus repositórios. 
Use o comando abaixo para configurar para todo o sistema.

````
git config --system
````

#### 3.2-User

Esta configuração é válida para o seu usuário  em todos os seus repositórios. 
Use o comando abaixo para configurar para o seu usuário.

````
git config --global
````
#### 3.3-Project

A última configuração é válida apenas para um projeto específico.

Use o comando abaixo para configurar para o projeto corrente.

````
git config 
````

::: :pushpin: Importante :::

>Use, de preferência, a configuração `git config --global`

#### 3.4-Configuração de exemplo

````
git config --global user.email "jbbfreitas@gmail.com"
git config --global user.name "João Bosco de Barros Freitas"
````

#### 3.5-Exibindo a configuração atual
```
git config user.email
````

::: :pushpin: Importante :::

>As configurações de usuário e email são obrigatórias para indentificar os seus commits


#### 3.6-Obtendo ajuda 
````
git help

git help <command> 
Ex git help commit
Ou 
man git-commit
````

Próximo Passo [Iniciando com o GIT](../Iniciando/README.md)


