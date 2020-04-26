### 16- Outros Recursos do Remote

#### Push

O `push` serve para enviar os dados do(s) commit(s) ao repositório remoto.

Antes de usar o "git push", verifique se você está no branch local correto usando um check-out. Em seguida, para executar o envio, basta especificar para qual branch remoto você deseja enviar. 
Por exemplo, se você estiver trabalhando em uma branch denominada `develop`, então poderia usar:

```
git checkout develop
git push origin develop

```
Se você estiver publicando um repositório local pela primeira vez em um repositório remoto, a opção "-u" deverá ser utilizada. Ela garante que uma conexão entre os repositórios remoto e local:

```
git push -u origin develop
```
Depois de configurar uma conexão, você poderá executar futuros envios sem fornecer opções adicionais - já que a conexão usará valores padrão para o comando push, assim basta digitar:

```
git push 
```

#### Pull e Fetch

O `pull` e o `fetch` são parecidos porém com funcionalidades distintas. Antes de falarmos sobre as diferenças entre esses dois comandos, destacamos suas semelhanças: ambos são usados ​​para baixar novos dados de um repositório remoto.

Fazer o download de dados é uma etapa essencial no seu trabalho diário - porque os dados remotos que você está vendo no seu repositório local são apenas um "instantâneo". Os dados foram atualizados  a última vez em que você baixou explicitamente usando `fetch` ou `pull`. É essencial ter esse fato em mente ao inspecionar branchs remotos!

Vejamos agora as diferenças, mais importantes, entre `fetch` e `pull`.

O `git fetch` realmente baixa apenas novos dados de um repositório remoto - mas não integra nenhum desses novos dados aos seus arquivos de trabalho. O `fetch` é excelente para obter uma nova visão de todas as coisas que aconteceram em um repositório remoto.
Devido à sua natureza "inofensiva", você pode ter certeza: a busca nunca manipulará, destruirá ou estragará nada. Isso significa que você usá-lo quantas vezes quiser sem o menor receio.
Sintaxe:

```
git fecth origin
```
Observações:

- O fetch não altera o master, apenas altera o origin/master
- Por isso deve-se adotar as seguintes práticas:
    - Faça o fetch antes de começar a trabalhar
    - Faça o fetch antes de fazer um push
    - Faça o fetch sempre
    - Para sincronizar é preciso fazer um merge

Lembre-se desta equação:

`git pull = git fetch + git merge`


O `git pull`, por outro lado, é usado com um objetivo diferente em mente: atualizar o HEAD de seu branch com as alterações mais recentes do servidor remoto. Isso significa que o `pull` não baixa apenas novos dados; ele também os integra diretamente aos seus arquivos de  trabalho atuais. Isso tem algumas consequências:

> Como o "git pull" tenta mesclar alterações remotas com as locais, pode ocorrer um chamado "conflito de mesclagem". Confira a lição  [14-Fazendo um true merge](../14-TrueMerge/README.md) sobre como lidar com conflitos de mesclagem para obter mais informações.

Como em muitas outras ações, é altamente recomendável iniciar um "git pull" apenas com uma cópia de trabalho limpa. Isso significa que você não deve ter nenhuma alteração local não confirmada (comitada) antes de executar. Use o recurso `stash` do Git para salvar suas alterações locais temporariamente.(Mais tarde falaremos do `stash`)

Sintaxe:

```
git pull origin develop
```

#### Clone

O comando "clone" baixa um repositório Git existente no seu computador local.

Você terá uma versão local completa desse repositório Git e poderá começar a trabalhar no projeto.

Normalmente, o repositório "original" está localizado em um servidor remoto, geralmente de um serviço como GitHub, Bitbucket ou GitLab). O URL desse repositório remoto é posteriormente chamado de "origin".

Opções importantes
<repositório>
Especifica a URL do repositório remoto. Normalmente, isso apontará para um servidor remoto, usando um protocolo como HTTP, HTTPS, SSH ou GIT.

<diretório>
O nome da pasta na sua máquina local para a qual o repositório será baixado. Se essa opção não for especificada, o Git simplesmente criará uma nova pasta com o nome do repositório remoto.

--recurse-submódulos
Clona e inicializa todos os submódulos contidos. Se o seu projeto contiver submódulos, o uso desse parâmetro garantirá que todos os submódulos sejam clonados e inicializados depois que o projeto principal tiver sido clonado. Isso evita que você precise inicializar e atualizar manualmente os submódulos posteriormente.

Exemplos:

Neste exemplo simples (mas o mais usual), apenas a URL do repositório é especificada:

```
cd pasta/para/receber/clone
git clone https://github.com/seuLogin/seuRepositorio.git
```

Este comando fara o download do projeto para uma pasta especificada com o nome `seuRepositorio`. Se desejar clonar para uma pasta diferente, simplesmente especifique o nome da pasta de destina como último parâmetro.

```
git clone https://github.com/seuLogin/seuRepositorio.git
```
#### Fluxo de trabalho para o uso do git

Papel: Colaborator

Suponha que você esteja desenvolvendo um aplicativo web e deseja criar um formulário para que os usuários do aplicativo possam dar um "fedd-back".

Veja o que deveria fazer:

```
git checkout master
git fetch // o pull poderia ser usado aqui
git merge origin/master // dispensada se usar o pull
git checkout -b feedback_form //cria o branch 
git add feedback.html //adiciona o formulário ao stagin
git commit -m "Adicionado o formulário de feedback"
git fetch //Verifica se houve mudança no repo remoto 
git push -u origin feedback_form //envia para o branch remoto
```








