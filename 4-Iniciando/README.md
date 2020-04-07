### 4.Iniciando com o GIT

1. Crie uma pasta denomninada "Grupo de Estudos"

> Esta pasta será utilizada muitas outras vezes, então crie-a em um local de fácil acesso.

2. Dentro da pasta recém-criada, crie um segunda pasta denominada "Git-Essencial"

3. Vá para a pasta "Git-Essencial" e inicialize o git nessa pasta digitando:

````
git init
````


::: :pushpin: Importante :::

>O comando `git init` inicia um repositório nessa pasta, ou seja, todos os arquivos que forem criados nesta pasta ou nas suas subpastas, serão automaticamente gerenciados pelo git. Simples, não?


#### 4.1 O que faz o git init?

Quando você digita `git init` o `GIT`inicializa um repositório na pasta atual. Para isso são criadas diversas pastas dentro de uma pasta denominada `.git` . Todas essas pastas  serão utilizadas pelo GIT.

>Essas pastas ficam ocultas por default. Mas você pode vêlas digitando:

````
ls -la .git
````

ou, se estiver utilizando o Windows, digite no prompt

````
dir .git
````
>Observe que foram criados 3 arquivos e 4 pastas (outros/arquivos pastas podem ser criados dependendo do seu sistema operacional)

#### 4.2 Vamos fazer o nosso primeiro commit?

1. Na pasta "Git-Essencial" crie um arquivo denominado `primeiro.txt`
2. Digite neste arquivo o texto "Primeiro arquivo com o git" .
3. Salve o arquivo
4. No prompt de comandos digite:

````
git commit add .
git commit -m "Commit inicial"
````

````
$ [master (root-commit) 27731e8] Commit Inicial
 1 file changed, 1 insertion(+)
 create mode 100644 primeiro.txt
````

:thumbsup: Se apareceu a mensagem acima para você, parabéns! Você fez o seu primeiro `commit`

 
Próximo Passo [5-Melhoras práticas com o GIT](../5-MelhoresPraticas/README.md)





