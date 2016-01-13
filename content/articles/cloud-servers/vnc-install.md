---
node_id: 502
title: VNC Install
type: article
created_date: '2011-03-16 21:57:40'
created_by: RackKCAdmin
last_modified_date: '2015-12-29 18:0701'
last_modified_by: stephanie.fillmon
products: Cloud Servers
body_format: tinymce
---

This page explains how to install VNC on your Cloud Server. This article
was based upon the CentOS 5 distribution. This tutorial assumes you have
root access to your server and are running on a clean installation.

**Note: In order to use this you must have at least 512MB of RAM or X
Windows will not run.**

**WARNING: Running VNC on your Cloud Server will consume large amounts
of bandwidth. Please use wisely!**

If you would like information about tunnelling VNC over SSH please visit
[http://martybugs.net/smoothwall/puttyvnc.cgi](http://martybugs.net/smoothwall/puttyvnc.cgi "http://martybugs.net/smoothwall/puttyvnc.cgi")

* * * * *

+--------------------------------------------------------------------------+
| Contents                                                                 |
| --------                                                                 |
|                                                                          |
| -   [1 Install the Necessary Packages](#Install_the_Necessary_Packages)  |
|     -   [1.1 Install Perl](#Install_Perl)                                |
|     -   [1.2 Install X Windows](#Install_X_Windows)                      |
|     -   [1.3 Install a Window Manager](#Install_a_Window_Manager)        |
|         -   [1.3.1 KDE](#KDE)                                            |
|         -   [1.3.2 GNOME](#GNOME)                                        |
|         -   [1.3.3 TWM](#TWM)                                            |
|     -   [1.4 Install VNC Server](#Install_VNC_Server)                    |
| -   [2 Configuration](#Configuration)                                    |
|     -   [2.1 Configure VNC](#Configure_VNC)                              |
|     -   [2.2 Firewall](#Firewall)                                        |
|     -   [2.3 Test the Server](#Test_the_Server)                          |
|         -   [2.3.1 Switch to your User](#Switch_to_your_User)            |
|         -   [2.3.2 Create a .vnc directory](#Create_a_.vnc_directory)    |
|         -   [2.3.3 Create the xstartup file](#Create_the_xstartup_file)  |
|         -   [2.3.4 Setup your VNC user](#Setup_your_VNC_user)            |
|         -   [2.3.5 Start the VNC server](#Start_the_VNC_server)          |
|         -   [2.3.6 Connect to your VNC](#Connect_to_your_VNC)            |
|         -   [2.3.7 Stopping the VNC Server](#Stopping_the_VNC_Server)    |
+--------------------------------------------------------------------------+

Install the Necessary Packages
------------------------------

This article will assume you know how to use the YUM Update Manager.

### Install Perl

    # yum install perl

### Install X Windows

We will need to install the X-Windows platform to run the graphical
portion of this project. X11 is a graphical display server, and will
server and will sit above the Window Manager.

To install run the following as root:

    # yum groupinstall "X Window System"

### Install a Window Manager

[KDE](http://www.kde.org/ "http://www.kde.org/"),
[GNOME](http://www.gnome.org./ "http://www.gnome.org./") and
[TWM](http://xwinman.org/vtwm.php "http://xwinman.org/vtwm.php") are all
Window Managers and are the human usable layer that you are probably
familiar with. This gives you the access to use a mouse and send calls
to the X11 server.

#### KDE

    # yum groupinstall "KDE Desktop"

Also, this may be needed:

    # yum install kde-session

#### GNOME

    # yum groupinstall "GNOME Desktop Environment"

Also, this may be needed:

    # yum install gnome-session

#### TWM

TWM is the default X-Window Manager and you don't have to install any
additional packages, it is light and will run on almost anything, but is
also not very user friendly and almost requires a power-user.

### Install VNC Server

VNC is the service that display your X output to a tcp connection over
the internet.

    # yum install vnc-server

Configuration
-------------

### Configure VNC

-   Modify the **/etc/sysconfig/vncservers** configuration file by
    performing the following commands:

<!-- -->

    # nano /etc/sysconfig/vncservers

Insert the following lines into the file:

    VNCSERVERS="1:someguy"
    VNCSERVERARGS[1]="-geometry 800x600 -depth 16"

This will create a VNC session for one user with the username of
**someguy**. If you would like to setup multiple users you will need to
add additional users to that line. For example...

    1:someguy 2:someperson 3:somegirl

You will also need to add additional VNCSERVERARGS lines to correspond
to each user. Change the [1] to match the session number.

### Firewall

If you have a firewall running, you will need to open port 5901. For
example, on CentOS, run:

    # iptables -I INPUT 1 -p tcp --dport 5901 -j ACCEPT

If needed, replace 5901 with a range, depending on the number of
sessions required (e.g. 5901:5905).

Save the new iptables rule:

    # service iptables save

### Test the Server

#### Switch to your User

    # su username
    $ cd ~

#### Create a .vnc directory

*take note of the '.' in front of the name*

    $ mkdir .vnc
    $ cd .vnc

#### Create the xstartup file

Insert the configuration below (this is for a KDE-VNC session):

    #!/bin/sh
    unset SESSION_MANAGER
    exec /etc/X11/xinit/xinitrc
    [ -x /etc/vnc/xstartup ] && exec /etc/vnc/xstartup
    [ -r $HOME/.Xresources ] && xrdb $HOME/.Xresources
    xsetroot -solid grey
    vncconfig -iconic &
    xterm -geometry 80x24+10+10 -ls -title "$VNCDESKTOP Desktop" &

    startx &
    exec kde-session &

-   If you are using GNOME, change 'kde-session' to 'gnome-session'

Make the file executable:

    $ chmod u+x xstartup

#### Setup your VNC user

Set the user's private VNC connection password

    # vncpasswd

-   You will be required to confirm your password.

#### Start the VNC server

Make sure you exit out of your user session and go back to 'root'.

start the server:

    # service vncserver start

-   You may see some error messages here stating 'unexpected EOF' or
    syntax errors -- these are normal. If you see **[ OK ]** then the
    service has started properly.

#### Connect to your VNC

Open up your VNC client and type in your external IP address, colon,
then your session ID configured in **/etc/sysconfig/vncservers**. The
session number must correspond to the user name or it will not connect.

Example: 64.25.25.25:1

-   Type in the password you chose with vncpasswd and you will be
    connected.

\
 To close the connection simple close the window.

#### Stopping the VNC Server

To stop the VNC server type the following:

    # service vncserver stop


