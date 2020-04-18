### 10-Diferença entre dois arqvuos

Gerenciar de mudanças é, sobretudo, a capacitada de saber a qualquer tempo as diferencas entre duas versões de arquivos.

Mas veja, quando falamos de diferença entre versões de arquivo é preciso relembrar a arquitetura do git.

Lembra-se da arquitura de 3 árvores (three-tree architecture) ?. Então quando estamos falando de diferença entre versões podemos nos referir a qualquer uma das diferenças abaixo:

1. Diferença entre working e staging
2. Diferença enrtre staging e repository
3. Diferença entre working e repository

Vamos mostrar isso com exemplos.


### 1. Diferença entre working e staging;

- Na pasta `lab1` modifique o Arquivo1.java para e, em seguida, salve-o 

````java
package lab1;
public class Arquivo1 {
    public static void main(String[] args) {
        System.out.println("Olá mundo! Este é minha primeira classe java modificada");
    }
}
````

Agora faça 

```
$ git stauts
````
e o git responde com:
````
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   lab1/Arquivo1.java

no changes added to commit (use "git add" and/or "git commit -a")
````

Agora faça

```
$ git diff
```

e veja o que acontece

```
diff --git a/lab1/Arquivo1.java b/lab1/Arquivo1.java
index 59c3afe..147effe 100644
--- a/lab1/Arquivo1.java
+++ b/lab1/Arquivo1.java
@@ -1,6 +1,6 @@
 package lab1;
 public class Arquivo1 {
     public static void main(String[] args) {
-        System.out.println("Olá mundo! Este é minha primeira classe");
+        System.out.println("Olá mundo! Este é minha primeira classe modificada");
     }
 }
```

O git mostra a diferença entre o working e o stagin.

### 2. Diferença enrtre staging e repository

Agora faça

```
$ git add .
```

Este comando está enviando o Arquivo1.java modificado para a área de staging. 

Agora faça

```
git diff --staged
```
Bingo! Você acertou o git agora mostra a diferença entre o staging e o repository

```
diff --git a/lab1/Arquivo1.java b/lab1/Arquivo1.java
index 59c3afe..147effe 100644
--- a/lab1/Arquivo1.java
+++ b/lab1/Arquivo1.java
@@ -1,6 +1,6 @@
 package lab1;
 public class Arquivo1 {
     public static void main(String[] args) {
-        System.out.println("Olá mundo! Este é minha primeira classe");
+        System.out.println("Olá mundo! Este é minha primeira classe modificada");
     }
 }
```
Pergunto: e se fizermos o `git diff` (sem o --staged), o que acontece?

### 3. Diferença entre working e repository

Vamos verificar quais os commits realizados até agora:

Faça:

```
$ git log --oneline
```

```
b9544f7 (HEAD -> master) modificado o Arquivo1.java
```

Agora faça

```
$ git diff b9544f7 (coloque aqui o hash do seu commit)
```

```
diff --git a/lab1/Arquivo1.java b/lab1/Arquivo1.java
index 59c3afe..147effe 100644
--- a/lab1/Arquivo1.java
+++ b/lab1/Arquivo1.java
@@ -1,6 +1,6 @@
 package lab1;
 public class Arquivo1 {
     public static void main(String[] args) {
-        System.out.println("Olá mundo! Este é minha primeira classe");
+        System.out.println("Olá mundo! Este é minha primeira classe modificada");
     }
 }

```






