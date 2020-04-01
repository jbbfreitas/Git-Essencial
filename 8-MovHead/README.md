### 8-Como movimentar o Head

Para mostrar como movimentar o `Head` vamos fazer um pequeno tutorial.

1. Crie um pasta denominada `lab1``
2. Nessa pasta crie um arquivo denominado `Arquivo1.java` (não se preocupe com a sintaxe java, é só um exemplo)
3. Digite no arquivo o conteúdo da Listagem 1

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
$ git commit -m "Commit inicial"
```
5. Agora vamos verifica onde está posicionado o `Head`. Para isso digite:

```git
$ git log --oneline
> 
```
Verique onde está o Head


