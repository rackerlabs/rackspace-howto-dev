---
node_id: 71
title: Mail Server - Opening Ports in the Linux Firewall
permalink: article/mail-server-opening-ports-in-the-linux-firewall
type: article
created_date: '2011-03-08 18:21:56'
created_by: RackKCAdmin
last_modified_date: '2013-10-17 21:4717'
last_modified_by: jered.heeschen
products: Cloud Servers
body_format: tinymce
---

In the [previous
article](/knowledge_center/index.php/Mail_Server_-_Courier_Installation "Mail Server - Courier Installation") we
installed and configured the basics of Courier. Now we need to open the
ports in our firewall so we can access those services.

There are standard ports that are used to access most services.

For example, accessing a website generally uses port 80 for normal
(HTTP) web pages and port 443 for secure (HTTPS) pages.

SMTP
----

**NOTE:**  Though SMTP generally uses port 25 for connections, port 587
is actually the preferred port for outbound SMTP traffic due to the
widespread abuse of port 25.

POP and POPS
------------

POP and secure POP use ports 110 and 995 respectively.

IMAP and IMAPS
--------------

IMAP and secure IMAP use ports 143 and 993 respectively.

iptables
--------

Following from the Cloud Server setup, we need to edit the
iptables.test.rules files to allow access to those ports. We will use
port 25 for SMTP at the moment. You can change it as you see fit.

1.   Open the test rules file using the following command:

    sudo nano /etc/iptables.test.rules

2.   Just before the HTTP and HTTPS entries, add the following details:

    # Allows SMTP access
    -A INPUT -p tcp --dport 25 -j ACCEPT 

    # Allows pop and pops connections 
    -A INPUT -p tcp --dport 110 -j ACCEPT
    -A INPUT -p tcp --dport 995 -j ACCEPT
    # Allows imap and imaps connections 
    -A INPUT -p tcp --dport 143 -j ACCEPT
    -A INPUT -p tcp --dport 993 -j ACCEPT

3. Apply the new rules using the following command:

    sudo iptables-restore < /etc/iptables.test.rules

4.   Now check that the rules have been applied using the following
command:

    sudo iptables -L

This information should be in the output from the command:

    ACCEPT     all  --  anywhere             anywhere            state RELATED,ESTABLISHED 
    ACCEPT     tcp  --  anywhere             anywhere            tcp dpt:smtp 
    ACCEPT     tcp  --  anywhere             anywhere            tcp dpt:pop3 
    ACCEPT     tcp  --  anywhere             anywhere            tcp dpt:pop3s 
    ACCEPT     tcp  --  anywhere             anywhere            tcp dpt:imap2 
    ACCEPT     tcp  --  anywhere             anywhere            tcp dpt:imaps

5.   Now we have tested the rules, we need to have them applied on a
permanent basis.

You will need to have full root access for the next command so use this
command in order to enter the root shell:

    sudo -i

6.   Now use the following command:

    iptables-save > /etc/iptables.up.rules

7.   Now run this and we&rsquo;re done:

    exit

This will place you back at the admin users command prompt. Do not stay
in the root shell.

Summary
-------

Opening the default mail ports in your firewall ensures you have access
to the POP, POPS, IMAP, and IMAPS services that we have configured and
started in this procedure.

Now we are ready to add users and domains to our MySQL database and
start using the mail server.

The [next
article](/knowledge_center/index.php/Mail_Server_-_Adding_domains_and_users_to_MySQL "Mail Server - Adding domains and users to MySQL")
looks at that in detail.

[Previous
Article](/knowledge_center/index.php/Mail_Server_-_Courier_Installation "Mail Server - Courier Installation")\
 [Next
Article](/knowledge_center/index.php/Mail_Server_-_Adding_domains_and_users_to_MySQL "Mail Server - Adding domains and users to MySQL")

