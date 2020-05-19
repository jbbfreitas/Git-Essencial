# Este projeto tem por finalidade o aprendizado das funções básicas do Git


## Usando uma linguagem fácil e com aplicações práticas, a idéia é simplificar ao máximo o uso de uma poderosa e indispensável ferramenta.

## 1.Introdução

### Por que indispensável?

Bom, se você vai desenvolver um sistema, certamente terá que lidar com inúmeros arquivos (classes, configurações, scripts etc) em um processo de desenvolvimento incremental. 

Como o desenvolvimento de um sistema pode ser  algo relativamente complexo, uma ótima prática é usar a teoria do exército romano "dividir para conquistar". Isso siginifica que  à medida que o sistema vai sendo construído, novos arquivos serão inseridos e, outros, serão alterados ou até mesmo excluídos. É o que se denomina de `desenvolvimento incremental`. 

Nesse processo, em pouquíssimo tempo você terá um conjunto de 40, 100 e talvez 1000 arquivos e vai acabar descobrindo  que lidar com um conjunto grande de arquivos é bastante complicado. 

Pense nas seguintes questões:

- Quais as alterações foram feitas hoje ou ha uma hora atrás?
- As mudanças que fiz ontem não deram certo, teria como voltar à versão anterior?
- Sem querer deletei um arquivo inteiro, tem como recuperá-lo?
- Qual as diferenças entre este  arquivo e aquele? Por que um funciona e o outro não?  

Agora imagine que, além de tudo isso, você está trabalhando com mais 3 ou 4 colegas que estão em outros locais e fazendo inclusão, alteração e exclusão de arquivos o tempo todo!

#### Está convencido que é indispensável o uso de uma ferramenta para te ajudar a gerenciar versões de arquivos?
Se ainda não, continue lendo. Você vai se convencer logo logo.

### Por que poderosa?

Toda ferramenta VCS é poderosa!

`VCS`? Mas o que é isso?

`Um VCS nada mais é do que a sigla em inglês para "*Version Control System*" ou "Sistema de Controle de Versões". 

#### Quais as mais conhecidas ferramentas de VCS?

> Sim. Existem vários, vou citar alguns:

1. CVS - A CVS é uma das ferramentas de controle de software mais antigas no mercado. A primeira versão dela foi desenvolvida em 1968. Essa ferramenta é considerada como uma tecnologia defasada, porém, ainda é bastante utilizada por equipes de desenvolvedores.

2. Subversion - É uma ferramenta de controle de versão ainda bastante utilizada com uma curva de aprendizgem bastante suave. Um dos problemas do Subversion é o fato de ser uma ferramenta de controle de versão centralizada. Isso significa que  é indicada apenas para as equipes  que estão reunidas em um mesmo espaço físico.

3. TFS  — sigla para "*Team Foundation Server*" traz uma série de características interessantes, principalmente se for utilizasa metodologias por meio de SCRUM. Permite a utilização de forma centralizada ou distribuída, sendo adequado tanto para equipes que compartilham o mesmo espaço físico quanto aquelas que trabalham à distância.

4. GIT - O GIT é uma das ferramentas de controle de versão de software mais populares, principalmente em projetos *open source*. As principais vantagens dessa ferramenta são o design interno e interface, a eficácia e o desempenho do software. Isso significa que ele é agradável de ser utilizado, consegue atingir todos os objetivos de um bom controle de software e é rápido. É a principal ferramenta de controle de versão de software disponível no mercado, entretanto, possui controles um pouco mais complexos quando comparada a outras VCS. É uma ferramenta de controle de versão distribuída, o que significa que é adequada para a utilização em pequenas ou grandes equipes, nas quais os desenvolvedores não estão localizados geograficamente no mesmo local.

5. Mercurial- É uma ferramenta de controle de versão de software utilizada por grandes empresas como o Facebook e Google. Rápida na execução dos comandos e adequada para equipes grandes, isso porque ela é uma ferramenta de controle de versão distribuída.

#### Principais vantagens do GIT

- **Distribuída**. Isso significa que **não há um servidor central** . Cada desenvolvedor tem uma versão instalada em sua estação de trabalho e vai fazendo o seu próprio controle de versão (*commit*) até que seja necessário enviar para um ponto central onde todos tenham acesso (*push*). Se isso lhe parece pouco pense que a aplicação está replicada em diversos pontos (não há o risco de um desastre em um único servidor) e a rede não é sobrecarregada com os *commits* locais.

- **Encoraja a participação**. Como não há um servidor central, os desenvolvedores são encorajados a "deixar suas idéias fluir" sem o risco de danificar o projeto como um todo, submentendo as suas mudanças para que sejam incluídas ou rejeitadas.

#### Quem deveria usar o GIT?

- Os que desejam rastrear as edições de seus arquivos
    - revisar histórico e os reigstros com as mudanças realizadas
    - comparar versões de arquivos
    - recuperar versões anteriores
- Aqueles que desejam compartilhar mudanças com os seus colegas
- Programadores e desenvolvedores para gerenciar arquivos 
    - HTML,CSS, JavaScript
    - PHP, Ruby, TypeScript
    - Java, C, C#
- Também deve ser usado (com limitações) para
    - Processadores de texto, planilhas e PDF
-Não deveria ser usado para
    - Arquivos de mídia (fotos, filmes, música)


Próximo Passo [2-Instalar o GIT](/2-Instalacao/README.md)


