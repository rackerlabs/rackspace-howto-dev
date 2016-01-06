---
node_id: 90
title: CentOS - Hostname Change
permalink: article/centos-hostname-change
type: article
created_date: '2011-03-09 17:19:45'
created_by: RackKCAdmin
last_modified_date: '2014-05-15 20:4021'
last_modified_by: rose.contreras
products: Cloud Servers
body_format: tinymce
---

This article will cover a simple server hostname change in CentOS. By
default your server will be kicked with the server's given name as the
hostname. Some software such as CPanel require a valid Fully Qualified
Domain Name or FQDN for the hostname to be used during their Licensing
verification system.

+--------------------------------------------------------------------------+
| Contents                                                                 |
| --------                                                                 |
|                                                                          |
| -   [1 Hostname Change](#Hostname_Change)                                |
|     -   [1.1 Sysconfig/Network](#Sysconfig.2FNetwork)                    |
|     -   [1.2 Hosts File](#Hosts_File)                                    |
|     -   [1.3 Run Hostname](#Run_Hostname)                                |
|     -   [1.4 Restart Networking](#Restart_Networking)                    |
+--------------------------------------------------------------------------+

Hostname Change
---------------

There are 4 steps in a hostname change, luckily all the steps are easy.

### Sysconfig/Network

Open the */etc/sysconfig/network* file with your favorite text editor.
Modify the **HOSTNAME=** value to match your FQDN host name.

    # sudo nano /etc/sysconfig/network

    HOSTNAME=myserver.domain.com

### Hosts File

Change the host that is associated to your main IPaddress for your
server, this is for internal networking (found at /etc/hosts):

![hosts.png](http://cdn.cloudfiles.rackspacecloud.com/c42672/CentOS%20-hostname%20change/hosts.png)

### Run Hostname

The 'hostname' command will let you change the hostname on the server
that the commandline remembers, but it will not actively update all
programs that are running under the old hostname.

\

![hostname.png](http://cdn.cloudfiles.rackspacecloud.com/c42672/CentOS%20-hostname%20change/hostname.png)

### Restart Networking

At this point all the necessary changes that needed to be made have been
made, you will want to restart networking on your server to make sure
that changes will be persistent on reboot:

    # /etc/init.d/network restart

 

