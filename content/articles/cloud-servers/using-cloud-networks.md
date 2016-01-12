---
node_id: 2163
title: Create an isolated Cloud Network and attach it to a server
permalink: article/using-cloud-networks
type: article
created_date: '2012-09-17 19:30:03'
created_by: Susan Million
last_modified_date: '2016-01-05 16:2004'
last_modified_by: rose.contreras
products: Cloud Servers
body_format: tinymce
---

With Cloud Networks you can create a virtual layer 2 network that you
can attach to a new cloud server. This feature lets you keep your Cloud
Server separate from the Rackspace network, the Internet, or both.

Cloud Network limitations
-------------------------

-   The Cloud Network must exist in the same region as the server.

-   You can create up to 10 isolated networks with up to 250 servers
    attached to each network.

-   A network cannot be renamed after it is created.

Attach an isolated network to a cloud server
--------------------------------------------

1.  In the [Cloud Control Panel](https://mycloud.rackspace.com).\
     The Cloud Servers page is displayed by default.

2.  Click **Create Server**.

3.  Enter a name for the server and select the region.

4.  Under Advanced Options, click **Select Networks**.

5.  Click **Create Network** to create a new isolated network.

6.  In the Create Network popup menu, enter a name for the network and
    click **Create Network**.

    **Note:** You cannot rename the network after it is created.

7.  Select the network for your server and click **Select Network**.

8.  *(Optional)* Clear the check box next to a network in the Networks
    table to remove it from the server.

    **Warning:** Before you remove ServiceNet or PublicNet from your
    Cloud Server, read [Removing Networks from a Cloud
    Server](http://www.rackspace.com/knowledge_center/article/removing-networks-from-a-cloud-server "Disabling Networks from a Cloud Server")
    for a complete description of the limitations that will be placed on
    your new server.

9.  Click **Select Networks**.
10. Click **Create Server**.

Your new cloud server is created and attached to the new isolated
network. When the server build is complete, you can scroll down to see
the Networks table. The table displays each network the server is
attached to with the corresponding IP address. Following is an example
Networks table for a server that is attached to PublicNet (Internet),
ServiceNet (the Rackspace data center network), and an isolated Cloud
Network named My Private Network: 

![Cloud Networks
List](http://www.rackspace.com/knowledge_center/sites/default/files/field/image/Cloud%20Networks%20List.png)

More information about Cloud Networks
-------------------------------------

[Attach an Isolated Network to an Existing Cloud
Server](http://www.rackspace.com/knowledge_center/article/attach-an-existing-cloud-server-to-a-cloud-network "Attach an Isolated Network to an Existing Cloud Server")

[Removing Networks from a Cloud
Server](http://www.rackspace.com/knowledge_center/article/rmoving-networks-from-a-cloud-server "Removing Networks from a Cloud Server")

[CIDR
Notation](http://www.rackspace.com/knowledge_center/article/using-cidr-notation-in-cloud-networks "CIDR Notation")

[Cloud Networks Developer
Guide](http://docs.rackspace.com/servers/api/v2/cn-devguide/content/ch_overview.html "Cloud Networks Developer Guide")

 

