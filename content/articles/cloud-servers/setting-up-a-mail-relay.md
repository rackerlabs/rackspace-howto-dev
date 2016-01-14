---
node_id: 439
title: Setting up a Mail Relay
type: article
created_date: '2011-03-16 21:57:40'
created_by: RackKCAdmin
last_modified_date: '2013-04-17 20:4218'
last_modified_by: jered.heeschen
product: Cloud Servers
body_format: tinymce
---

undefined2. Configure Postfix

Add the following to /etc/postfix/main.cf:

    relayhost = secure.emailsrvr.com 
    smtp_sasl_auth_enable=yes 
    smtp_sasl_password_maps=hash:/etc/postfix/sasl_passwd
    smtp_sasl_mechanism_filter = AUTH LOGIN
    smtp_sasl_security_options =

Add the Rackspace Email username and password to
/etc/postfix/sasl\_passwd by running these commands:

    echo 'secure.emailsrvr.com username@domain.com:secretpassword' > /etc/postfix/sasl_passwd
    chmod 600 /etc/postfix/sasl_passwd 
    postmap /etc/postfix/sasl_passwd

Restart Postfix and check the mail logs, you should see something like
this:

    Nov 23 10:46:05 web2 postfix/qmgr\[24259\]: 5497F3708AA:
    from=<orders@myawesomeecommercesite.com>, size=1762, nrcpt=1 (queue active)
    Nov 23 10:46:05 web2 postfix/smtp\[1343\]:497F3708AA:to=<customer@someisp.com>,
    relay=secure.emailsrvr.com\[98.129.185.2\]:25, delay=0.31, delays=0.02/0.01/0.19/0.1,
    dsn=2.0.0, status=sent (250 2.0.0 Ok: queued as B5E3D2D0476)

