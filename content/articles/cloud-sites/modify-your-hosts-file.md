---
node_id: 629
title: Modify your hosts file
type: article
created_date: '2011-03-16 21:57:40'
created_by: RackKCAdmin
last_modified_date: '2015-09-18 21:0739'
last_modified_by: kyle.laffoon
product: Cloud Sites
body_format: tinymce
---

Modificar seu arquivo hosts permite que vo&ecirc; substitua o do&iacute;nio DNS em
uma determinada &aacute;quina. Isso pode ser usado para avaliar o seu site sem
o link de teste antes de ir ao vivo com o SSL, verificar se o alias de
um local funciona antes de alter&ccedil&otilde;es de DNS, ou por outros motivos
relacionados com o DNS. Isso faz com que sua &aacute;quina local somente se
conecte diretamente com o IP especificado.\
 \
 Seu arquivo hosts precisa de duas entradas secun&aacute;rias que con&ecirc;m o
ender&ccedil;o IP do site que vo&ecirc; deseja mostrar e o ender&ccedil;o. Adicionar as
duas linhas a seguir, por exemplo,
[www.dominio.com](http://www.dominio.com) e dominio.com aponta direto ao
nosso PHP5-ITK cluster ("Refreshed" PHP5))

    64.49.219.194 www.domain.com
    64.49.219.194 domain.com

Abaixo detalhes de como localizar e editar o arquivo hosts em diferentes
sistemas operacionais. Uma vez que as inform&ccedil&otilde;es de um do&iacute;nio &atilde;o
adicionadas, salve o arquivo e o sistema com&ccedil;a&aacute; a enviar ao IP
especificado. A&oacute;s os testes, estas entradas devem ser removidas.

-   [Windows 8, Windows 7, and Windows Vista](#Windows_Vista)
-   [Windows NT, Windows 2000, and Windows XP](#Windows_NT2000XP)
-   [Linux](#Linux)
-   [Mac OS X 10.0 through 10.1.5](#Mac_OS_X_100_through_1015)
-   [Mac OS X 10.6 through 10.8](#macosx10.6)

Windows 8, Windows 7, e Windows Vista {#Windows_Vista}
-------------------------------------

Windows 8, Windows 7 e Windows Vista usam o Controle de Conta de Us&aacute;rio
(UAC, sua sigla em Ing&ecirc;s), de modo que o notebook deve ser executado
como Administrador.

### Para Windows 8

1.  Pressione a tecla Windows.\
         Escreva notepad no campo de pesquisa.\
         No campo de pesquisa, pressione o bo&atilde;o direito do mouse sobre
    Bloco de notas e selecione Executar como administrador.\
         No bloco de notas, abra o arquivo a seguir:\
         C: \\ Windows \\ System32 \\ drivers \\ etc \\ hosts\
         F&ccedil;a as alter&ccedil&otilde;es neces&aacute;rias no arquivo hosts.\
         Pressione Arquivo -\> Salvar para salvar as alter&ccedil&otilde;es.\
      

### For Windows 7 and Windows Vista

    Clique Iniciar\> Todos os Programas\> Aces&oacute;rios.\
     Clique com o bo&atilde;o direito do mouse Bloco de notas e selecione
Executar como administrador.\
     Clique em Continuar na janela do UAC "Windows precisa da sua
permis&atilde;o".\
     Quando o bloco de notas abrir, clique em Arquivo -\> Abrir.\
     No campo Nome do arquivo, digite:\
     C: \\ Windows \\ System32 \\ drivers \\ etc \\ hosts\
     Clique Abrir.\
     F&ccedil;a as alter&ccedil&otilde;es neces&aacute;rias no arquivo hosts.\
     Clique Arquivo -\> Salvar para salvar as alter&ccedil&otilde;es.

Windows NT, Windows 2000, and Windows XP {#Windows_NT2000XP}
----------------------------------------

1.  Clique Iniciar -\> Todos os Programas\> Aces&oacute;rios -\> Bloco de
    Notas.\
         Clique File-\> Open.\
         No campo Nome do arquivo, digite:\
         C: \\ Windows \\ System32 \\ drivers \\ etc \\ hosts\
     Clique Abrir.\
         F&ccedil;a as alter&ccedil&otilde;es neces&aacute;rias  no arquivo hosts.\
         Clique Arquivo -\> Salvar para salvar as alter&ccedil&otilde;es.

Linux {#Linux}
-----
1. Abra uma janela de terminal.\
 \
 2. Abra o arquivo hosts em um editor de texto (vo&ecirc; pode usar qualquer
editor de texto):\
 \
 sudo nano / etc / hosts\
 \
 3. Digite sua senha\
 \
 4. F&ccedil;a as alter&ccedil&otilde;es neces&aacute;rias no arquivo hosts.\
 \
 5. Pressione control X (Clique CTRL e pressione X) e, em seguida,
clique quando perguntado se vo&ecirc; deseja salvar as alter&ccedil&otilde;es.\
  

Mac OS X 10.0 through 10.1.5 {#Mac_OS_X_100_through_1015}
----------------------------

1.  1. Abra **/Applications/Utilities/NetInfo Manager**..\
     \
     2. Para permitir a ed&ccedil&atilde;o do banco de dados do NetInfo, clique no
    cadeado no canto inferior esquerdo da janela.\
     \
     3. Digite sua senha e pressione OK.\
     \
     4. Na segunda coluna da janela do navegador, selecione o &oacute;(node)
    chamado `machines`. Vo&ecirc; ve&aacute; -DHCP-, BroadcastHost, e localhost na
    terceira coluna.\
     \
     5. Selecione o elemento de localhost na terceira coluna.\
     \
     6. Escolha Duplicar no menu Editar (o caminho mais &aacute;pido para
    criar uma nova entrada&eacute; duplicar uma existente). Um alerta de
    confirm&ccedil&atilde;o aparece.\
     \
     7. Pressione Duplicar. Uma nova entrada chamada **localhost copia**
    e suas propriedades &atilde;o mostradas abaixo da janela do browser.\
     \
     8. Pressione duas vezes o valor da propriedade ip\_address e digite
    o ender&ccedil;o IP do outro computador.\
     \
     9. Prima duas vezes o valor da propriedade de nome e digite o nome
    do host que vo&ecirc; deseja para o outro computador.\
     \
     Serve 10. Pressione a propriedade e escolha Excluir no menu
    Editar.\
     \
     11. Clique em Salvar no menu Arquivo. alerta de confirm&ccedil&atilde;o
    aparece.\
     \
     12. Clique em Atualizar essa &oacute;pia.\
     \
     13. Repita os passos de 6 a 12 para cada entrada de host adicional
    que vo&ecirc; deseja adicionar.\
     \
     14. Selecione Sair do menu de NetInfo Manager. &atilde;o &aacute; necessidade
    de reiniciar o computador.\
      

Mac OS X 10.6 - 10.8 {#macosx10.6}
--------------------

1. 1. Abra Aplicativos\> Utili&aacute;rios\> Terminal.\
     \
     2. Abra o arquivo hosts, digitando o seguinte na janela Terminal:\
     \
     sudo nano / privado / etc / hosts\
     \
     Digite sua senha quando solicitado.\
     \
     3. Edite o arquivo hosts. O arquivo hosts con&eacute;m comen&aacute;rios
    (linhas que com&ccedil;am com \#), e alguns nomes de host de mapeamento
    pad&atilde;o (por exemplo, 127.0.0.1 - host local). Fixe seus novos
    mapeamentos abaixo os mapeamentos pad&atilde;o.\
     \
     4. Salve o arquivo hosts pressionando Control + xy e resposta.\
     \
     5. Para que as alter&ccedil&otilde;es tenham efeito, esvaziar o cache DNS com o
    seguinte comando:\
     \
     dscacheutil -flushcache\
     \
     6. Agora, aplique o novo mapeamento.



