### 5.Melhores práticas com o GIT


#### 5.1-Nomes dos branchs

***Branchs? Mas o que é um branch?***

Para esplicar o que vem a ser um branch, pense em um árvore. Uma árvore possue raiz, tronco principal e vários ramos, não é?

A raiz é o ínicio de tudo, foi o nosso primeiro commit. Se continuarmos crescendo com o projeto, é como se a nossa árvora fosse crescendo, a cada commit, vamos crescendo com o projeto (e com a árvore).

O tronco principal da nossa "árvore git" denomina-se `master`, é como se fosse um ramo mestre, um ramo principal da árvore. 

Pois bem, se a árvore tivesse apenas um tronco principal (como uma palmeira imperial), ainda assim seria uma árvore e isso é o que ocorre em projetos muito pequenos. Ocorre que em um projeto real a "árvore-git" tem vários ramos (braços) que saem do tronco priocipal. Esses ramos são denominados de `branch`.

Qual a finalidade de um branch? Um branch é como se fosse uma variante do tronco principal, ou seja, abandona-se o tronco principal e vai-se fazendo alterações no projeto e com isso o branch vai se distanciando do tronco principal (master). Isso é feito para isolar o tronco principal das alterações que são feitas no projeto. Ao isolar evita-se que aplicações pouco testadas "contaminem" a aplicação que está funcionando e em ambiente de produção.

Em algum momento, de preferência após exaustivos testes, o branch será integrado de volta ao master e as suas *features* serão incorporadas ao master e, portanto, ao sistema que está em ambiente de produção. 

Em alguns casos, os `branchs` serão, simplesmente, descartados.

Em resumo:

> Um branch é útil em situações nas quais você deseja adicionar um novo recurso ou corrigir um erro, gerando uma nova ramificação garantindo que o código instável não seja mesclado nos arquivos do projeto principal. Depois de concluir a atualização dos códigos da ramificação, você pode mesclar a ramificação com a principal, geralmente chamada de master.

>A propósito o `master` é também um `branch`, só que um `branch`especial, o tronco principal da nossa árvore. 

::: :pushpin: Boa prática para os nomes dos branchs :::

- Nomes pequenos
- Nomes significativos (Nada de usar prjTemp ou Lixo1)
- Nomes informativos (Ex. ControleHoras)

#### 5.2-Mensagens dos commits

As mensagens de commit irão orientar você e sua equipe quando verificarem o log (registros) dos `commits`. É como se elas contassem a história do projeto, devem portanto:

- Caracterizar o contexto 
- Serem concisas e claras
- Usar uma padronização
- Não devem ter mais que 50 caracteres
- Se necessitar de mais de 50 linhas, deve-se deixar um linha em branco e complementar o texto nas linhas seguintes, com um máximo de 72 caracteres por linha.
- Escreva as mensagens no tempo presente, não no passado. Por exemplo: "Resolve o bug do menu Pedido" e não "Foi resolvido o bug do menu Pedido"
- Use * ou  - como bullets
- Pode-se usar o número de uma *issue* de erro (número de registro em um sistema de *bug tracker* como o [Redmine] (https://www.redmine.org/) p. exemplo )

Próximo Passo [6-Verificando o Log do GIT](../6-LogGit/README.md)


