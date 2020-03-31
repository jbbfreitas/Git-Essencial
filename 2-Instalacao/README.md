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

Próximo Passo [3-Configurar o GIT](../3-Configuracao/README.md)
