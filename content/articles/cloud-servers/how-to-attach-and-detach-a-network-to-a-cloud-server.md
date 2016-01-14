---
node_id: 3814
title: Cloud Servers - Attaching and Detaching Networks
type: article
created_date: '2013-12-17 01:47:32'
created_by: rose.contreras
last_modified_date: '2014-11-07 20:3830'
last_modified_by: ross.diaz
product: Cloud Servers
body_format: tinymce
---

You can attach (add) or detach (disconnect) networks from existing Next
Gen Cloud Servers by using the [Cloud Networks
API](http://docs.rackspace.com/servers/api/v2/cn-devguide/content/api_virt_interfaces.html)
or the Cloud Control Panel.

This article describes how to attach and detach networks by using the
Cloud Control Panel. Please be aware that if you attach networks to or
detach them from a cloud server, you might experience a brief
interruption, usually lasting less than a minute, in traffic hitting
your cloud server while networking is reset on the server.

### To Attach (Add) a Network:

1.  Log in to the Cloud Control Panel at
    [mycloud.rackspace.com](http://mycloud.rackspace.com).\
     \
     ![](/knowledge_center/sites/default/files/field/image/attach-2.png)\
      
2.  On the Cloud Servers page, click the server to which  you want to
    attach a network. The details page for that server is displayed.\
     \
      
3.  Scroll to the Networks section and click Add Network.\
     \
     A pop-up box lists the networks that you can attach to this
    server.\
     \
      
4.  Select a network and click Add Network.    \
     \
     You can also create a new cloud network and attach it to the
    server..\
     \
     ![](/knowledge_center/sites/default/files/field/image/attach-3.png)\
     \
     ![](/knowledge_center/sites/default/files/field/image/attach-4.png)\
     \
     After the network is attached, it is displayed in the list of
    networks for that server.\
     \
     ![](/knowledge_center/sites/default/files/field/image/attach-5.png)

### To Detach (Disconnect) a Network:

You can detach a network from the server from the same page under the
Networks section. Please refer to the article below before you detach
Public or ServiceNet interfaces from cloud servers.
[http://docs.rackspace.com/servers/api/v2/cn-devguide/content/networks.html](http://docs.rackspace.com/servers/api/v2/cn-devguide/content/networks.html)

1.  Log in to the Cloud Control Panel at
    [mycloud.rackspace.com](http://mycloud.rackspace.com).\
     ![](/knowledge_center/sites/default/files/field/image/attach-6.png)\
     \
     \
     ![](/knowledge_center/sites/default/files/field/image/attach-7.png)\
      
2.  On the Cloud Servers page, click the server from which you want to
    detach a network.\
     \
     The details page for that server is displayed.\
      
3.  In the Networks section, click the gear icon next to the network
    that you want to detach.\
     \
      
4.  In the pop-up box, click Disconnect Network.

After the network is detached from the server, it is no longer displayed
in the list of networks for that server.

 

 

