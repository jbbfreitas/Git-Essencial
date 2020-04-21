### 13 - Branchs

Por que usar branchs?

Branchs são úteis para criar novas funcionalidades, testar algum recurso sem comprometer a versão principal da aplicação, enfim para isolar novas <features> do sistema para incoporá-las assim que forem testadas.

Uma grande vantagem da branch é que você não precisa copiar nada, nem muito menos criar uma nova pasta. O git gerencia tudo para você.

O que acontece se você criar um novo branch (ramo)? 
    
    a. Cria um novo ponteiro para você se movimentar. 
    
    b. Digamos que você queira criar um novo ramo chamado testing. 
    
Você faz isso com o comando:
```
git branch testing
```
Veja a Figura 1 

<p align="center">
  <img src="../imagens/Branch.png" alt="Uma típica árvore do Git com um Master, Branch e Head">
</p>
<p align="center">
   <strong>Figura 1-Uma típica árvore do Git com um Master, Branch e Head</strong> 
</p>

```
 git log --oneline
9dd3aa4 (HEAD -> master, testing) Revert "Revert "imprime a data formatada""
99fffb1 Revert "imprime a data formatada"
b7b2bf6 imprime a data formatada
fc3be9d (origin/master) Adicionado o lab2
cb0d1f5 Atualização em Arquivo 1
f5e8cb0 Adicionada mais uma linha no commit anterior
5d98f23 commit inical
```

> Observe a linha `9dd3aa4 (HEAD -> master, testing)``

O git está dizendo que tanto o `master` quanto o `testing` estão apontando para o mesmo hash <9dd3aa4>
