---
node_id: 113
title: Controlling access to Linux Cloud Sites based on the client IP address
permalink: article/how-do-i-deny-certain-ip-addresses-from-accessing-my-site-on-cloud-sites
type: article
created_date: '2011-03-10 17:13:30'
created_by: RackKCAdmin
last_modified_date: '2014-07-25 18:3124'
last_modified_by: jered.heeschen
products: Cloud Sites
body_format: tinymce
---

On Cloud Sites, due to our unique hosting environment, we require an
addition to the **Allow/Deny** instruction in the .htaccess file when
controlling access to a site based on IP address. The issue is that the
requesting IP address coming into a server is the IP address of our load
balancing server instead of the visitor's IP address. This means
limiting access on an IP address level through .htaccess becomes
problematic. To work around that, we provide an environment variable
called **X-Cluster-Client-Ip** that contains the visitor's IP address.

In the .htaccess file containing your rules, make the appropriate change
from the list below based on your requirements.

#### Allowing only a certain IP/IP Addresses:

    order deny,allow
    deny from all
    allow from env=allowclient
    SetEnvIf X-Cluster-Client-Ip 000.000.000.000 allowclient

#### Allowing only a certain IP/IP Addresses when your site is using SSL:

    order deny,allow
    deny from all
    allow from env=allowclient
    SetEnvIf X-FORWARDED-FOR ^000.000.000.000$ allowclient

Replace **000.000.000.000** with your IP address. This will only allow
your IP address to access your site, and is a great way to develop your
site without the risk of someone reaching it before it's ready.\
 **You can repeat line 1 to allow multiple IPs.**

#### Denying an IP/Multiple IP addresses:

    Order Allow,Deny
    Deny from env=DenyAccess
    Allow from all
    SetEnvIf X-Cluster-Client-Ip "^000\.000\.000\.000" DenyAccess

#### Denying an IP/Multiple IP addresses when your site is using SSL:

    Order Allow,Deny
    Deny from env=DenyAccess
    Allow from all
    SetEnvIf X-FORWARDED-FOR "^000\.000\.000\.000" DenyAccess

Replace **000\\.000\\.000\\.000** with the IP address you want to deny.
This will deny the IP address specified/multiple IP addresses (If you
use multiple lines, as specified below).\
 **You can repeat line 1 to deny multiple IP addresses.**

**Important note:** Implementing this code may prevent images from
loading on your cloud site. To address this you can add the following
code do your .htaccess file:

    <FilesMatch "\.(gif|jpe?p|png)$">
    order deny,allow
    allow from env=allowclient
    </FilesMatch>

