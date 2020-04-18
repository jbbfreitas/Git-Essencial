### 9-Adicionando Arquivos ao Staging

Resumidamente, o  que fizemos até agora foi colocar arquivos no `staging`, usando o comando `git add . `. Mas você se lembra quando dissemos em [7-Arquitetura e Fluxo do GIT](/7-ArqFlux/README.md)
que o `staging` é uma área temporária e que você poderia incluir e remover do `staging` a vontade?  Mas que outras formas o git dispõe para incluir no `staging` além do `git add .`?  Para mostrar isso vamos fazer um pequeno tutorial.

####  A primeira forma

1. Crie um pasta denominada `lab2`
2. Nessa pasta crie um arquivo denominado `Arquivo2.java` (não se preocupe com a sintaxe java, é só um exemplo)
3. Digite no `Arquivo2.java` o conteúdo da Listagem 1

````java
package lab2;

import java.text.DateFormat;
import java.text.SimpleDateFormat;
import java.util.Date;

public class Arquivo2 {
    public static void main(String[] args) {
        DateFormat dateFormat = new SimpleDateFormat("dd/MM/yyyy HH:mm:ss");
        Date date = new Date();
        System.out.println("Hoje é "+dateFormat.format(date)); 
    }
}
````
4. Após salvar o arquivo, no `prompt` execute o comando para mostrar o status

````
$ git status

````

:thumbsup: Se apareceu a mensagem abaixo é por que você seguiu os passos corretamente até aqui. 

````
> $ Untracked files:
  (use "git add <file>..." to include in what will be committed)
        lab2/
`````

> A mensagem do Git, acima, está dizendo que existem arquivos `Untracked`, ou seja, que não estão sendo rastreados (gerenciados) ainda.

5. Agora vamos adicionar o `Arquivo2.java` na área de `staging`
````
$ git add lab2/Arquivo2.java

````
:thumbsup: Se apareceu a mensagem abaixo é por que você seguiu os passos corretamente até aqui. 

````
On branch master
Your branch is up to date with 'origin/master'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	new file:   lab2/Arquivo2.java

`````
> A mensagem do Git, acima, está dizendo que agora o `Arquivo2.java` está sendo rastreado, pois acaba de ser incluído na área de `staging`.

> Você entendeu a diferença do `git add . ` para  o `git add lab2/Arquivo2.java` ?

Bom é meio óbvio não é? O primeiro adiciona todos os arquivos na área de `staging` enquanto que o segundo adiciona apenas 1 arquivo (`Arquivo2.java`). 

####  A segunda forma

Essa é a forma geralmente usada quando estamos fazendo commit com muita frequencia. É muito simples, é só usar o parâmetro `-a` no `commit`. Então fica assim:

````
git commit -a -m "Mensagem do seu commit"
````


ou, simplesmente

`````
git commit -am "Mensagem do seu commit"

````

> O parâmetro `-a` é uma abreviação de `add .`

Você poderia usar ainda:

````
git commit -a "lab2/Arquivo2.java" -m "Mensagem do seu commit"

Próximo Passo [10-Diferença entre dois arqvuos](../10-Diferença entre dois arqvuos/README.md)









