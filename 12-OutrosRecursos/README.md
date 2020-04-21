### 12-Outros Recursos Importantes

Além dos recursos vistos até aqui, o git ten inúmeros outros recursos. Mostraremos apenas os mais importantes.

#### 1- Revertendo um commit

Pode ser que em algum momento seja necessário reverter um commit. Para isso iremos usar o comando `revert`.

> A sintaxe do comando é a seguinte > git revert <hash do commit>

Então vamos testar:

````
git log --oneline
fc3be9d (HEAD -> master, origin/master) Adicionado o lab2
cb0d1f5 Atualização em Arquivo 1
f5e8cb0 Adicionada mais uma linha no commit anterior
5d98f23 commit inical
````

Vamos fazer uma pequena mudança em Lab2/Arquivo2.java

```java
package lab2;

import java.text.DateFormat;
import java.text.SimpleDateFormat;
import java.util.Date;

public class Arquivo2 {
    public static void main(String[] args) {
        DateFormat dateFormat = new SimpleDateFormat("dd/MM/yyyy HH:mm:ss");
        Date date = new Date();
        // Imprime a data formatada
        System.out.println("Hoje é "+dateFormat.format(date)); 
    }
}

```

```
$ git commit -am "coloca um comentário para imprimir a data formatada"

$ git log --oneline

b7b2bf6 (HEAD -> master) coloca um comentário para imprimir a data formatada
fc3be9d (origin/master) Adicionado o lab2
cb0d1f5 Atualização em Arquivo 1
f5e8cb0 Adicionada mais uma linha no commit anterior
5d98f23 commit inical

```

OK. Vamos então reverter o commit de hash `b7b2bf6`

```
git revert b7b2bf6 --no-edit
git log --oneline
99fffb1 (HEAD -> master) Revert "coloca um comentário para imprimir a data formatada"
b7b2bf6 coloca um comentário para imprimir a data formatada
fc3be9d (origin/master) Adicionado o lab2
cb0d1f5 Atualização em Arquivo 1
f5e8cb0 Adicionada mais uma linha no commit anterior
5d98f23 commit inical
```

Vamos explicar tudo:

a.  --no-edit significa que você deseja aceitar a mensagem padrao do git. Essa mendagem é "Rrevert + mensagem do último commit"

b. O revert desfaz o commit solicitado mas não apaga nada. Isso significa que ele acrescenta um novo commit (no nosso caso o `99fffb1`) e, esse commit, contém os mesmos arquivos do commit anterior ao revertido (b7b2bf6). Ou seja, você está agora nas mesma situação quando fez o commit  `fc3be9d` 

Posso fazer o revert do revert? Sim, é que vamos fazer agora.

```
git revert 99fffb1 --no-edit
git log --oneline
9dd3aa4 (HEAD -> master) Revert "Revert "coloca um comentário para imprimir a data formatada"
99fffb1 Revert "coloca um comentário para imprimir a data formatada"
b7b2bf6 coloca um comentário para imprimir a data formatada
fc3be9d (origin/master) Adicionado o lab2
cb0d1f5 Atualização em Arquivo 1
f5e8cb0 Adicionada mais uma linha no commit anterior
5d98f23 commit inical
```

#### 2- Reset (Cuidado! Use com cautela pois é muito poderoso)

git reset

    Opções:
    --soft
      Não altera nem o staging nem o working

    --mixed (default)
      Altera o stagin para coincidir com o repository
      Não altera o working

    --hard
      Altera o staging e o working para coincidir com o repositório 


 Como dissemos o `git reset` só deve ser usado em condições muito especiais. Se possível faça uma cópia do seu trabalho em outra pasta antes de usar o comando se você não tiver certeza do que está fazendo.         

```
git reset <hash do commit para onde se deseja ir>
```







