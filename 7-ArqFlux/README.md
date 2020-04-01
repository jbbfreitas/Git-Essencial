### 7.Arquitetura do GIT

Peço que você se detenha o quanto for necessário nesse tópico, pois é aqui que a maioria das pessoas tropeça no uso do Git.

#### 7.1 Arquitetura de 3 árvores (Three tree architecture)


Veja a figura abaixo:


<p align="center">
  <img src="../imagens/Arquitetura3Arvores.png" alt="Arquitetura de 3 árvores do Git">
</p>
<p align="center">
   <strong>Figura 1- Arquitetura de 3 árvores do Git</strong> 
</p>

Como o próprio nome já diz o Git trabalha não apenas com uma árvore, mas com 3! Vamos detalhar isso.

O que significa o nome das árvores: "Working", "Stagin index" e  "Repository" ? 

Antes de explicar o significado de cada um deles vamos supor que você tenha criado um arquivo denominado `file.txt`. A  explicação do significado de cada árvore será dada em função do estado desse arquivo em cada uma das árvores. 

#### 7.1.1-Working
Na árvore `Working` o arquivo `file.txt` está sendo editado, ou seja, o `Working` é o ambiente de trabalho e contém sempre a versão mais recente do arquivo.


#### 7.1.2-Staging index
Nessa árvore estão os arquivos que serão transferidos para o `Repository`. É um estado intermediário, antes dos arquivos serem transferidos para o `Repository`. Pense nisso como um cesto que recebe produtos que serão posteriormente despachados para entrega.  

Mas por que um "cesto" ? Por que o Git não envia direto do `Working` para o `Repository` ? 

Há duas explicações para isso: a primeira é que o `Stagin`, como um área intermediária, permite selecionar os arquivos serão transferidos para o `Repository`, sem ter que transferir todos de uma vez, a segunda é que pode-se "desistir" da transferência para o `Repository` retirando-se o arquivo do `Stagin`.   

Para que o nosso arquivo exemplo, passe da árvore `Working` para o `Staging`, deve-se usar o comando `git add`.
O comando `git add` deve ser seguido pelo nomes dos arquivos que serão transferidos, podendo-se usar nesse caso * e ? (wilcards).

Exemplos de `git add` 

````
git add *.txt

git add .

````
O comando `git add .`, adiciona todos os arquivos que estão no `Working` ao `Stagin`.

::: :pushpin: Importante :::

> Lembra quando lhe dissemos que você pode tirar coisas da sua cesta imaginária? O Git também pode tirar as coisas da cesta removendo arquivos dessa área. Para remover arquivos do `Stagin`, use o seguinte comando:

````
git rm --cached file.txt
````
> Em nosso exemplo, especificamos o comando "rm", que significa remover. A opção "--cached" indica arquivos na área de `Stagin`. Por fim, passamos um arquivo que queremos excluir dessa área. O Git emitirá a seguinte mensagem para nós:

````
rm 'file.txt'
````

#### 7.1.3-Repository

Para que os arquivos sejam "versionados" é preciso transferir da área `Stagin` para `Working`. Na área `Stagin` os nosso arquivo exemplo foi "congelado" no último estado em que se encontrava na `Working` antes de ser transferido para `Stagin`. Isso significa que o arquivo `file.txt` pode continuar sendo alterado na `Working` sem que a sua cópia no `Stagin` seja alterada. O que será transferido para o repositório é a versão do `file.txt` que está no `Stagin`.

Para transferir os arquivos que estão no `Stagin` deve-se utilizar o comando `git commit`.

A sintaxe completa do comando `git commit` é seguinte:

````
git add -m "Mensagem do Commit"
````

#### 7.2 Como o GIT referencia os Commits

Observe a figura abaixo:


<p align="center">
  <img src="../imagens/RerefenciaACommits.png" alt="Como o Git referencia os commits">
</p>
<p align="center">
   <strong>Figura 2- Como o Git referencia os commits</strong> 
</p>







