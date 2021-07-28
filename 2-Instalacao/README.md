### 2.Instalando o GIT

#### 2.1-Instalando no  Linux

Se você deseja instalar o Git no Linux através de um instalador binário, você pode geralmente fazê-lo através da ferramenta básica de gerenciamento de pacotes que vem com sua distribuição. Se você usar Fedora por exemplo, você pode usar o yum:

` $ sudo yum install git-all`

Se você usar uma distribuição baseada em Debian como o Ubuntu, use o apt-get:

`$ sudo apt-get install git-all`

Para mais opções de instruções de como instalar o Git em outros vários sistemas Unix, veja na página do Git, em http://git-scm.com/download/linux.

#### 2.2-Instalando no Mac
No Mavericks (10,9) ou acima, você pode fazer isso simplesmente digitando git a partir do Terminal pela primeira vez. Se você não tiver o Git instalado, ele irá pedir-lhe para instalá-lo.

Se você quiser uma versão mais atualizada, você também pode instalá-lo através de um instalador binário. Um instalador OSX Git é mantido e disponível para download no site do Git, pelo http://git-scm.com/download/mac.

#### 2.3-Instalando no Windows
 Basta ir ao http://git-scm.com/download/win e o download começará automaticamente. Note que este é um projeto chamado Git para Windows (também chamado msysGit), que é algo separado do Git; para mais informações sobre isso, vá para https://gitforwindows.org/.

Para fazer uma instalação automatizada, você pode usar o pacote Git do Chocolatey. Note que o pacote Chocolatey é mantido pela comunidade.

Outra forma fácil de obter Git instalada é através da instalação de GitHub para Windows. O instalador inclui uma versão de linha de comando do Git, bem como a GUI. Ele também funciona bem com o PowerShell, e configura o cache de credenciais sólidas e as devidas configurações CRLF.  Você pode baixá-lo da página GitHub para Windows, em http://windows.github.com.

#### 2.4-Testando se a instalação foi bem sucedida

Para testar se o git está corretamente instalado, no prompt de comando, digite:

````
$ git --version
````


#### 2.5-Habilitando um token para commit

Caso você não seja o proprietário do repositório, e for convidado a fazer commit, você deverá habilitar no GitHub um token para fazer o commit de seu repositório local. Não se preocupe que depois falaremos o que vem a ser exatamente um commit para o git.

Para habilitar um token no github proceda assim:

1-Clique na seta para baixo que está à direita de sua foto (ou ícone se vc ainda não inseriu uma);
2-No menu que abre, selecione "Settings";
3-No menu, que se abre do lado esquerdo da janela, selecione a opção "Developer settings";
4-No submenu dessa opção, selecione "Personal access tokens";
5-Clique no botão (que fica no lado superior direito da janela), "Generate new tokwn";
6-No campo "Note" digite um texto explicativo da razão para a qual este token está sendo criado;
7-No combo "Expiration" selecione o número de dias para que este token expire. O padrão é 30 dias;
8-Selecione os escopos (direitos de acesso);
9-Clique no botão que fica no canto esquerdo inferior, "Generate token"
10-Anote o token gerado em um local seguro pois vc precisará informá-lo quando fizer o commit pela primeira vez.


Próximo Passo [3-Configurar o GIT](../3-Configuracao/README.md)
