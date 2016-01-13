---
node_id: 92
title: CentOS 6 - Apache and PHP Install
type: article
created_date: '2011-03-09 18:24:07'
created_by: RackKCAdmin
last_modified_date: '2015-12-29 17:0049'
last_modified_by: stephanie.fillmon
products: Cloud Servers
body_format: tinymce
---

undefined&rdquo;.

Now just reload Apache:

    sudo /usr/sbin/apachectl restart

And the warning has gone.

Firewall
--------

Notice that in some versions of CentOS, a firewall is installed by
default which will block access to port 80, on which Apache runs. The
following command will open this port:

    sudo iptables -I INPUT -p tcp --dport 80 -j ACCEPT

Remember to save your firewall rules after adding that instruction so
your web server will be accessible the next time you reboot:

    sudo service iptables save

Default Page
------------

If you navigate to your Cloud Server IP address:

    http://123.45.67.89

You will see the default CentOS Apache welcome screen:

![
centos\_apache\_welcome.jpg](http://c458924.r24.cf2.rackcdn.com/Cent0SWelcome01.png)

This means the Apache install is a success.

Chkconfig
---------

Now that we have Apache installed and working properly, we need to make
sure that it's set to start automatically when the Cloud Server is
rebooted.

    sudo /sbin/chkconfig httpd on

Let's check our work to confirm:

    sudo /sbin/chkconfig --list httpd
    httpd           0:off        1:off  2:on    3:on    4:on    5:on    6:off

The setting works.

PHP5 Install
------------

Let's move on to the PHP5 install. I'm not going to install all the
modules available, just a few common ones so you get the idea.

As before, due to using yum to install PHP5, any dependencies are taken
care of:

    sudo yum install php-mysql php-devel php-gd php-pecl-memcache php-pspell php-snmp php-xmlrpc php-xml

Once done, reload Apache:

    sudo /usr/sbin/apachectl restart

 
-

