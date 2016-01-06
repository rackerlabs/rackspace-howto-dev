---
node_id: 1496
title: Prevent server overload with Cloud Load Balancers
permalink: article/preventing-server-overload
type: article
created_date: '2012-07-24 00:13:47'
created_by: RackKCAdmin
last_modified_date: '2014-10-30 16:4110'
last_modified_by: rose.contreras
products: Cloud Hosting
body_format: tinymce
---

One way that you can prevent a server from becoming overloaded is to use
the Connection Throttling feature of Cloud Load Balancers. Connection
throttling limits the number of simultaneous connections that are
allowed from each IP address. This feature helps prevent malicious or
abusive traffic to your server and its installed applications.

Before you begin
----------------

This procedure for configuring connection throttling assumes that you're
working with an existing load balancer. If you don't have a load
balancer yet, create one now by using the following instructions:
Configuring a Load Balancer.

### To configure connection throttling

1.  Log in to the Control Panel.
2.  At the top of the Control Panel, click **Load Balancers**
3.  Click onthe **Actions** cog next to your load balancer, and
    select**Edit Connection Throttling** from the menu.\
     The following pop-up window appears:\
     \
     ![](/knowledge_center/sites/default/files/field/image/827-1496.png)
4.  Enter a value for **Max. Connections**, and then click**Save
    Connection Throttling**. You can specify a value between 1 and
    100000.
5.  Enter a value for **Max. Connections. You can specify a value
    between 1 and 100000.**
6.  **Click **Save Connection Throttling**.**

** **

