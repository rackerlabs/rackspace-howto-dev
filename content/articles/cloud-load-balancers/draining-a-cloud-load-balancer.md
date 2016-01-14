---
node_id: 3552
title: Draining a load balanced server
type: article
created_date: '2013-06-26 20:43:07'
created_by: kyle.laffoon
last_modified_date: '2016-01-08 18:3445'
last_modified_by: kyle.laffoon
product: Cloud Load Balancers
body_format: tinymce
---

Server&ldquo;drainin&rdquo; is the redirection of incoming calls and new
connections from the specified server to other servers connected to the
same load balancer.  This is used to minimize service interruption when
taking a server offline for needed maintenance.  Sessions started before
the server is put into draining status will continue until they
naturally end.  When all sessions have ended, the server is considered
drained and can then be taken offline. The following steps help to
ensure minimal service interruption when removing a cloud server from an
active load balancer.

1.  Select the **Load Balancers** tab.
2.  Click the name of the applicable load balancer to view the connected
    servers.
3.  Click Action Cog next to server to be drained.
4.  Select **Edit Node Condition**from the options presented.

    ![Edit Node
    Connection](/knowledge_center/sites/default/files/field/image/EditNodeConditionwitharrow.jpeg)

5.  Select **Draining Connections** for the server condition and click
    **Save Condition**.

    ![](/knowledge_center/sites/default/files/field/image/Drainingconnections_0.jpg)

6.  Monitor the applicable port of the currently draining node for
    continued activity (for a Linux server check
    [netstat](http://www.rackspace.com/knowledge_center/article/checking-listening-ports-with-netstat)
    for new connections).
7.  When activity has ceased, repeat the first 5 steps above (as needed)
    and select **Disabled** in the repeated 5th step.

Once disabled, the server can be removed from the load balancer and the
application can be stopped or the instance deleted, depending on your
needs.

![Remove from Load
Balancer](/knowledge_center/sites/default/files/field/image/Removefromloadbalancer.jpeg) 

