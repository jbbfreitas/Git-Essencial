### 11-Emendando um commit

Em algumas situações pode ser necessário emendar um commit, isto é, gravar um commit que corrige o commit anterior.

É o que vamos aprender nesta lição.

1. Primeiro faça:

```
git log --oneline

$ b9544f7 (HEAD -> master) modificado o Arquivo1.java
  5d98f23 commit inical
````

Vamos imaginar que queiramos emendar o commit b9544f7.

2. Abra o arquivo Arquivo1.java e modifique-o conforme abaixo:


```
package lab1;
public class Arquivo1 {
    public static void main(String[] args) {
        System.out.println("Olá mundo! Este é minha primeira classe modificada");
        System.out.println("Esta linha não havia sido incluída");
    }
}
```

3. Agora obtenha o status do git

```
git status
$ On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	modified:   lab1/Arquivo1.java

````

Observe que o git detectou a modificação.

4. Agora faça 

````
git add .
git commit --amend -m "Adicionada mais uma linha no commit anterior"
git log --oneline
````


````
f5e8cb0 (HEAD -> master) Adicionada mais uma linha no commit anterior
5d98f23 commit inical
````


> O que aconteceu aqui? Bem fizemos uma emenda (amend em inglês). Observe que continuamos com apenas 2 commits. O commit anteior , `b9544f7`, teve sua mensagem "emendada" e agora tem um novo hash `f5e8cb0`

Facil não?
Isso é tudo por hoje.

Próximo Passo [12-Outros Recursos](../12-OutrosRecursos/README.md)
