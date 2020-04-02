### 8-Como movimentar o Head

Para mostrar como movimentar o `Head` vamos fazer um pequeno tutorial.

1. Crie um pasta denominada `lab1``
2. Nessa pasta crie um arquivo denominado `Arquivo1.java` (não se preocupe com a sintaxe java, é só um exemplo)
3. Digite no `Arquivo1.java` o conteúdo da Listagem 1

````java
package lab1;
public class Arquivo1 {
    public static void main(String[] args) {
        System.out.println("Olá mundo!");
    }
}
````
<p align="center">
   <strong>Listagem 1-Conteúdo da classe Arquivo1.java</strong> 
</p>

4. No prompt digite:

```git 
$ git add .
$ git commit -m "Criada a classe Arquivo1.java"
```
5. Agora vamos verifica onde está posicionado o `Head`. Para isso digite:

```git
$ git log --oneline
```

Veja o `HEAD` está está no hash `165d656`

```git
> 
165d656 (HEAD -> master, origin/master, origin/HEAD) Criada a classe Arquivo1.java
844c6a6 update
...
```
6. Vamos agora alterar o `Arquivo1.java`. Para isso digite:

````java
package lab1;
public class Arquivo1 {
    public static void main(String[] args) {
        System.out.println("Olá mundo! Este é minha primeira classe java");
    }
}
````
<p align="center">
   <strong>Listagem 2-Alteração da classe Arquivo1.java</strong> 
</p>

7. No prompt digite:

```git 
$ git add .
$ git commit -m "Alterada a classe Arquivo1.java"
```
8. Agora vamos verifica onde está posicionado o `Head`. Para isso digite:

```git
$ git log --oneline
```

Veja o `HEAD` está está no hash `7645321`

```git
> 
7645321 (HEAD -> master, origin/master, origin/HEAD) Alterada a classe Arquivo1.java
165d656 (HEAD -> master, origin/master, origin/HEAD) Criada a classe Arquivo1.java
844c6a6 update
...
```
9. Anote o seu hash atual, no nosso exemplo seria `7645321`

10. Vamos movimentar o `Head`. Para isso digite:

```git
$ git reset 165d656  <substitua 165d656 pelo seu hash anterior>
```
10. Verifique o conteúdo do `Arquivo1.java`, veja como voltou ao conteúdo da Listagem1 

11. Agora volte para o hash anterior

```git
$ git reset 7645321  <substitua 7645321 pelo hash que você anotou>
```

12. Verifique o conteúdo do `Arquivo1.java`, veja como está idêntico ao da Listagem2 


> Em resumo: O comando `git reset` movimenta o `head` 