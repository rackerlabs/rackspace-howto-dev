---
node_id: 105
title: Simple Load Balancing with Apache
permalink: article/simple-load-balancing-with-apache
type: article
created_date: '2011-03-09 19:22:30'
created_by: RackKCAdmin
last_modified_date: '2015-12-29 17:0500'
last_modified_by: stephanie.fillmon
products: Cloud Servers
body_format: tinymce
---

**Note: **This article was written before the introduction of [Cloud
Load
Balancers](http://www.rackspace.com/knowledge_center/getting-started/cloud-load-balancers),
which is our recommended solution for Load balancing, but customers may
still wish to try this procedure so we have left it available for legacy
support purposes.

This article will go through creating a simple software [Load
Balancer](http://www.rackspace.com/cloud/load-balancing/) using a [Cloud
Server](http://www.rackspace.com/cloud/servers/).

We'll take this as an entry level job using simple readily available
packages from any of the Distributions repositories. We'll be using
Apache as our Load Balancer (yes, apache can be used for so many things,
and yes it is a Load Balancer) in conjunction with the apache module
mod\_proxy and mod\_proxy\_balancer. Both are available through CentOS
and I'll be using this as my base install.

The main thing that I want you to take out of this is that you can use
Cloud Servers to scale horizontally. This is when you need horizontal
expansion, add drone servers behind a smart host each working a piece of
workload.

* * * * *

+--------------------------------------------------------------------------+
| Contents                                                                 |
| --------                                                                 |
|                                                                          |
| -   [1 Prerequisites](#Prerequisites)                                    |
|     -   [1.1 Hardware](#Hardware)                                        |
|     -   [1.2 Software](#Software)                                        |
| -   [2 Server Configuration](#Server_Configuration)                      |
|     -   [2.1 Web Servers](#Web_Servers)                                  |
|     -   [2.2 Load Balancer](#Load_Balancer)                              |
|         -   [2.2.1 Unwanted Requests](#Unwanted_Requests)                |
|         -   [2.2.2 The Balance](#The_Balance)                            |
|         -   [2.2.3 Balance Manager](#Balance_Manager)                    |
|         -   [2.2.4 ProxyPass](#ProxyPass)                                |
| -   [3 Summary](#Summary)                                                |
+--------------------------------------------------------------------------+

Prerequisites
-------------

### Hardware

We are going to use a total of 3 boxes to start out with, but you can
use this as a model to scale horizontally.

-   One Cloud Server to be used as the load balancer
-   Two Cloud Servers to be used as dumb web heads

### Software

The software for all three servers will be the same, technically they
will be running the same packages. We'll through in only two software
groups:

-   Update your system to all the newest goodies:

<!-- -->

    # yum update

-   Apache and all its goodies, CentOS makes this ultra simple with the
    groupinstall feature:

<!-- -->

    # yum groupinstall "Web Server"

-   Also, we are going to install links a text based web browser in case
    we ever need to check that a particular web head is displaying the
    page it is supposed to behind the load balancer. This is optional.

<!-- -->

    # yum groupinstall "Text-based Internet"

Server Configuration
--------------------

### Web Servers

This is going to be the easiest part of the whole configurations. Since
the webheads are really just drones, they're only going to be doing
grunt work, so you need no special configurations. Thats right, don't
even open the httpd.conf file, just put a file called index.html in
/var/www/html/index.html. In this file you can put any distinguishing
characteristics you want. I put "It works you looking at WebHead \#"
where \# is the numerical identifier of that particular webhead.

### Load Balancer

This is the tricky part of the operation, I'll walk through each step
and then bring it together at the end for you, so you know what the end
product should be. All of the configurations that we are going to go
through should be placed at the bottom of /etc/httpd/conf/httpd.conf in
a standard Virtual Host to work.

#### Unwanted Requests

We are not working as a Forwarding Proxy (better known as an Open Proxy,
and this is bad news as it lets people mask their identity by using your
server to view web pages for them, it has its uses but not in this
scenario), turning off ProxyRequests will help avoid any unwanted
traffic.

    ProxyRequests off

#### The Balance

In this part of the Virtual Host we will be naming our web heads and
declaring how we will be balancing. The BalanceMember directive is how
you declare the webheads, of course you can add as many as you would
like, using these as templates. The ProxySet directive declares how you
would like to balance, we're going to use a "byrequest" balancing
algorithm which is the same as a Round Robin, so for each new request
you will get a new webhead. The order is sequential, there are better
and smarter algorithms out there, but this is the easiest to configure
and you need no knowledge of networking theory. All of this will be
wrapped in \<Proxy\> tags which is how apache knows to send it to
mod\_proxy, the "balancer://mycluster" identifier is only an identifier,
you could technically call it what you want as long as you put the
"balancer://" prefix.

**Keep in mind you will want to contact your webheads from the load
balancer with their private IPs, this will keep your bandwidth charges
down to a minimum by keeping all communication between servers on the
Service Net, where bandwidth is free.**

    <Proxy balancer://mycluster>
        # WebHead1
        BalancerMember http://10.x.x.x:80
        
        # WebHead2
        BalancerMember http://10.x.x.x:80
        
        ProxySet lbmethod=byrequests

    </Proxy>

#### Balance Manager

**Optional Step**

This is a tool packaged with the mod\_proxy\_balancer tool, and allows
you to make configurations from a gui tool through the web browser.
Viewable at
"[http://domain.com/balancer-manager](http://domain.com/balancer-manager "http://domain.com/balancer-manager")",
keep in mind that these changes die after you restart apache. I won't go
over how to use this tool, but it is available to you.

    <Location /balancer-manager>

       SetHandler balancer-manager
    </Location>

 

#### ProxyPass

This is the last part of the configuration, and just adds the situations
that will need to be proxied. We don't want to proxy the
balancer-manager, but we do want to proxy everything else.

       ProxyPass /balancer-manager !
       ProxyPass / balancer://mycluster/

Summary
-------

Ok, so now if you've got all this in your httpd.conf on your load
balancer CloudServer, and start up apache you should be able to view
your domain name that is properly pointed to your load balancer. When
you hit refresh it should hop between your two webheads, saying "It
works you looking at WebHead 1" or "It works you looking at WebHead 2".
Congratulations you are now balancing.

So what I've done for you is combine all the things that we've learned
into a helpful packaged VirtualHost, just trade out all the necesary
values that are specific to your configuration like the domain name and
the IP addresses to your webheads. Also, there are some security
additions that are explained in the comments, everything is commented so
you don't have to refer back to this article to make changes later.

    <VirtualHost *:80>
            ProxyRequests off
            
            ServerName domain.com

            <Proxy balancer://mycluster>
                    # WebHead1
                    BalancerMember http://10.176.42.144:80
                    # WebHead2
                    BalancerMember http://10.176.42.148:80

                    # Security "technically we aren't blocking
                    # anyone but this is the place to make 
                    # those changes. 
                    Require all granted
                    # In this example all requests are allowed.

                    # Load Balancer Settings
                    # We will be configuring a simple Round
                    # Robin style load balancer.  This means
                    # that all webheads take an equal share of
                    # of the load.
                    ProxySet lbmethod=byrequests

            </Proxy>

            # balancer-manager
            # This tool is built into the mod_proxy_balancer
            # module and will allow you to do some simple
            # modifications to the balanced group via a gui
            # web interface.
            <Location /balancer-manager>
                    SetHandler balancer-manager

                    # I recommend locking this one down to your
                    # your office
                    Require host example.org

            </Location>

            # Point of Balance
            # This setting will allow to explicitly name the
            # the location in the site that we want to be
            # balanced, in this example we will balance "/"
            # or everything in the site.
            ProxyPass /balancer-manager !
            ProxyPass / balancer://mycluster/

    </VirtualHost>

**Note**: The preceding example is formatted for Apache 2.4. If using
2.2, replace **Require all granted** with**Order Deny,Allow | Deny from
none | Allow from all** and then replace **Require host example.org**
with **Order deny,allow | Deny from all | Allow from example.org**.

