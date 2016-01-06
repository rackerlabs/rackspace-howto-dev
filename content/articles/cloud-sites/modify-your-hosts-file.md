---
node_id: 629
title: Modify your hosts file
permalink: article/modify-your-hosts-file
type: article
created_date: '2011-03-16 21:57:40'
created_by: RackKCAdmin
last_modified_date: '2015-09-18 21:0739'
last_modified_by: kyle.laffoon
products: Cloud Sites
body_format: tinymce
---

La modificaci&oacute;n de su archivo de hosts le permitir&aacute; anular el DNS para
un dominio, en esa m&aacute;quina en particular. Esto se puede utilizar para
evaluar su sitio sin el enlace de prueba, antes de salir en vivo con
SSL, verificar que el alias de un sitio funcione antes de los cambios de
DNS, o para otras razones relacionadas con el DNS. Esto hace que su
m&aacute;quina local solo busque directamente en el IP especificado.

Su archivo de hosts necesitar&aacute; dos entradas agregadas que contendr&aacute;n la
direcci&oacute;n de IP que quiere que el sitio resuelva y la direcci&oacute;n. Agregar
las siguientes dos l&iacute;neas, por ejemplo, dirigir&aacute; www.dominio.com y
dominio.com a nuestro cl&uacute;ster PHP5-ITK (PHP5 "actualizado") actual:

    64.49.219.194 www.domain.com
    64.49.219.194 domain.com

A continuaci&oacute;n se detalla c&oacute;mo ubicar y editar el archivo de hosts en
plataformas de varios sistemas operativos. Una vez que se agregue la
informaci&oacute;n de dominio adecuada, guardar&aacute; el archivo y su sistema
comenzar&aacute; a resolver el IP especificado. Luego de que finalicen las
evaluaciones, estas entradas deber&iacute;an eliminarse.

-   [Windows 8, Windows 7, y Windows Vista](#Windows_Vista)
-   [Windows NT, Windows 2000, and Windows XP](#Windows_NT2000XP)
-   [Linux](#Linux)
-   [Mac OS X 10.0 - 10.1.5](#Mac_OS_X_100_through_1015)
-   [Mac OS X 10.6 - 10.8](#macosx10.6)

Windows 8, Windows 7 y Windows Vista {#Windows_Vista}
------------------------------------

Windows 8, Windows 7 y Windows Vista usan el Control de cuentas de
usuario (UAC, por sus siglas en ingl&eacute;s), as&iacute; que el Bloc de notas debe
ejecutarse como Administrador.

### Para Windows 8

1.  Presione la tecla Windows.
2.  Escriba Bloc de notas en el campo de b&uacute;squeda.
3.  En el campo de b&uacute;squeda, presione con el bot&oacute;n derecho del rat&oacute;n el
    Bloc de notas y seleccione **Ejecutar como administrador**.
4.  En el Bloc de notas, abra el siguiente archivo:\
     c:\\Windows\\System32\\Drivers\\etc\\hosts
5.  Realice los cambios necesarios para el archivo de hosts.
6.  Presione **Archivo**-\> **Guardar**para guardar los cambios.

### For Windows 7 and Windows Vista

1.  Presione **Iniciar**-\> **Todos los programas**-\> **Accesorios**.
2.  Presione con el bot&oacute;n derecho del rat&oacute;n el Bloc de notas y
    seleccione **Ejecutar como administrador**.
3.  Presione **Continuar** en la ventana de UAC "Windows necesita su
    permiso".
4.  Cuando el Bloc de notas se abra, presione **Archivo**-\> **Abrir**.
5.  En el campo de nombre de archivo, escriba:\
     C:\\Windows\\System32\\Drivers\\etc\\hosts
6.  Presione **Abrir**.
7.  Realice los cambios necesarios para el archivo de hosts.
8.  Presione **Archivo**-\> **Guardar**para guardar los cambios.

Windows NT, Windows 2000, and Windows XP {#Windows_NT2000XP}
----------------------------------------

1.  Presione **Iniciar**-\> **Todos los programas**-\> **Accesorios**-\>
    **Bloc de notas**.
2.  Presione **Archivo**-\> **Abrir**.
3.  En el campo de nombre de archivo, escriba:\
     C:\\Windows\\System32\\Drivers\\etc\\hosts
4.  Presione **Abrir**.
5.  Realice los cambios necesarios para el archivo de hosts.
6.  Presione **Archivo**-\> **Guardar**para guardar los cambios.

Linux {#Linux}
-----

1. Abra una ventana de terminal.

2. Abra el archivo de hosts en un editor de texto (puede utilizar
cualquier editor de texto):

    sudo nano /etc/hosts

3. Ingrese su contrase&ntilde;a

4. Realice los cambios necesarios para el archivo de hosts.

5. Presione**control X** (mantenga control y presione X), luego
conteste **y** cuando le pregunten si quiere guardar los cambios.

Mac OS X 10.0 through 10.1.5 {#Mac_OS_X_100_through_1015}
----------------------------

1.  1. Abra **/Aplicaciones/Utilidades/Gestor NetInfo**.

    2. Para permitir la edici&oacute;n de la base de datos de NetInfo,
    presione el candado en la esquina inferior izquierda de la ventana.

    3. Ingrese su contrase&ntilde;a y presione **OK**.

    4. En la segunda columna de la ventana del navegador, seleccione el
    nodo llamado `machines`. Ver&aacute; entradas para `-DHCP-`,
    `broadcasthost`, y `localhost` en la tercera columna.

    5. Seleccione el elemento `localhost` en la tercera columna.

    6. Elija **Duplicar**en el **men&uacute;**Editar (la manera m&aacute;s r&aacute;pida de
    crear una nueva entrada es duplicar una existente). Aparecer&aacute; una
    alerta de confirmaci&oacute;n.

    7. Presione **Duplicar**. Una nueva entrada llamada
    `localhost copy` y sus propiedades se muestran debajo de la ventana
    del navegador.

    8. Presione dos veces el valor de la propiedad `ip_address` e
    ingrese la direcci&oacute;n de IP de la otra computadora.

    9. Presione dos veces el valor de la propiedad `name` e ingrese el
    nombre de host que desea para la otra computadora.

    10. Presione la propiedad `serves` y elija **Eliminar**desde el
    men&uacute; **Edici&oacute;n**.

    11. Elija **Guardar**en el men&uacute; **Archivo**. Aparecer&aacute; una alerta
    de confirmaci&oacute;n.

    12. Presione **Actualizar esta copia**.

    13. Repita los pasos 6 al 12 para cada entrada host adicional que
    desee agregar.

    14. Seleccione **Salir**del men&uacute; de Gestor NetInfo. No es necesario
    que reinicie la computadora.

Mac OS X 10.6 - 10.8 {#macosx10.6}
--------------------

1. Abra **Aplicaciones**\> **Utilidades**\> **Terminal**.

2. Abra el archivo de hosts ingresando lo siguiente en la ventana
Terminal:

    sudo nano /private/etc/hosts

Escriba su contrase&ntilde;a de usuario cuando sea solicitada.

3. Edite el archivo de hosts. El archivo de hosts contiene algunos
comentarios (las l&iacute;neas que comienzan con el s&iacute;mbolo `#` ), y algunos
mapeos de nombres de hosts predeterminados (por ejemplo, 127.0.0.1 -
local host). Anexe sus mapeos nuevos debajo de los mapeos
predeterminados.

4. Guarde el archivo de hosts al presionar **Control+x** y contestar
**y**.

5. Para que se apliquen sus cambios, vac&iacute;e la cach&eacute; del DNS con el
siguiente comando:

    dscacheutil -flushcache

6. Ahora se aplicar&aacute;n los nuevos mapeos.

m o
    seguinte comando:\
     \
     dscacheutil -flushcache\
     \
     6. Agora, aplique o novo mapeamento.



