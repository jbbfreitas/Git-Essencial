### 6.Principais comando do GIT

O git foi concebido para ser uma ferramenta de `linha de comando`, ou seja, para ser usada no `terminal` ou `console` ou no `command` do windows. Mas para aqueles que odeiam as aplicações de linha de comando, fiquem tranquilos por que existem inúmeras ferramentas gráficas que irão auxiliar no uso do git.

Mas lembre-se: `TI não é para os fracos`. :flushed: 

Vamos passar então para os primeiros comando do Git:

#### 6.1 Log

O `log`como dissemos anteriormente, mostra os registros dos commits realizados. Existem varias possibilidades de se usar o log, vejamos algumas.

##### 6.1.1 Log sem parâmetros

Digite:

````
git log
````

Confira o resultado:

````
(base) jbbf:~/Documents/Grupo de Estudo/Git-Essencial $ git log
commit 302f3c49a55b65eb3b2655dcbdcb693afa1b4ab3 (HEAD -> master, origin/master, origin/HEAD)
Author: João Bosco de Barros Freitas <jbbfreitas@gmail.com>
:...skipping...
commit 302f3c49a55b65eb3b2655dcbdcb693afa1b4ab3 (HEAD -> master, origin/master, origin/HEAD)
Author: João Bosco de Barros Freitas <jbbfreitas@gmail.com>
Date:   Sun Mar 29 17:18:01 2020 -0400
````

> Meio confuso, não. Muita informação.  As vezes, entretanto, pode ser necessário usar esse comando.


::: :pushpin: Importante :::

>Veja esse número longo (escrito em hexadecimal). É o que se chama de `hash do commit`. Esse `hash` é um resumo matemático (que usa o algorítmo  SHA-1) e que funciona como um ponteiro para um determinado `commit`. Em geral os 7 primeiros caracteres são suficientes para identificar um `commit`, mas o `hash` completo tem 40 caracteres.

##### 6.1.2 Log em uma única linha

Se desejar um log menos "verboso" digite:


````
git log --oneline
````

Veja como ele é mais compacto.
````
(base) jbbf:~/Documents/Grupo de Estudo/Git-Essencial $ git log --oneline
302f3c4 (HEAD -> master, origin/master, origin/HEAD) update
0a29f3e update
93603c4 update
f05c40f update
````

##### 6.1.3 Log until

````
git log --until=2020-03-29
````

Veja como fica o resultado.
````
Irá mostrar todos os commit até a data de 29/03/2020
````

##### 6.1.4 Log grep

````
git log --grep="comm"
````

Veja como fica o resultado.
````
(base) jbbf:~/Documents/Grupo de Estudo/Git-Essencial $ git log --grep="com"
commit dafd3e6aa2a13158ad402564abd09cd13494efa9
Author: João Bosco de Barros Freitas <jbbfreitas@gmail.com>
Date:   Sun Mar 29 11:05:19 2020 -0400

    first commit
````
##### 6.1.5 Log author

````
git log --author="Bosco"
````

Veja como fica o resultado.
````
Mostra todos os commits contendo como parte do nome do autor "Bosco"
````
