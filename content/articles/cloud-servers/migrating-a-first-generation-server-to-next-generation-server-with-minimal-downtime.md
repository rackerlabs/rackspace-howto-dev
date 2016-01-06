---
node_id: 4782
title: Migrate a First Generation server to a Next Generation server with minimal downtime
permalink: article/migrating-a-first-generation-server-to-next-generation-server-with-minimal-downtime
type: article
created_date: '2015-08-10 16:29:18'
created_by: Rackspace Support
last_modified_date: '2016-01-04 17:4040'
last_modified_by: Nate.Archer
products: Cloud Servers
body_format: full_html
---

This article describes the process of migrating an existing First
Generation (First Gen) cloud server to a Next Generation (Next Gen)
cloud server with little to no downtime by using Cloud Load Balancers
and server imaging. To learn more about the Next Generation Cloud
Servers platform and the migration process, see [Next-Generation Cloud
Servers migration considerations and
options](http://www.rackspace.com/knowledge_center/article/next-generation-cloud-servers-migration-considerations-and-options).

**Note:** This article assumes that you host your Cloud Servers and DNS
with Rackspace. However, if you host DNS elsewhere, you will need to
perform the steps in the [Repoint your DNS to the load balancer](#rept)
section of this article via your DNS portal of where it is hosted.

+--------------------------------------------------------------------------+
| ### Contents                                                             |
|                                                                          |
| -   [Create a load balancer](#create)                                    |
| -   [Configure the load balancer](#config)                               |
| -   [Repoint your DNS to the load balancer](#rept)                       |
| -   [Create a Next Gen image](#image)                                    |
| -   [Create a Next Gen server](#nexgen)                                  |
| -   [Switch the servers](switch)                                         |
+--------------------------------------------------------------------------+

Create a load balancer
----------------------

The load balancer makes a seamless migration from First Gen server to
Next Gen server possible. You use it to update your DNS entries by
having your stale DNS entry traffic continue to reach your cloud server
while allowing the updated traffic to continue being passed on through
the load balancer.

1.  Log in to your Cloud Control Panel.\
    \
2.  From the **Networking** menu, select **Load Balancers**.\
    \
3.  Click **Create Load Balancer**.\

    ![](/knowledge_center/sites/default/files/field/image/1941-2_0.png)

4.  In the Identification section, enter a name and select the same
    region your server is in for your load balancer.\
    \
5.  In the Configuration section, select **Accessible on the Public
    Internet** for Virtual IP.\
    \
6.  Click **Create Load Balancer**.\
    \

Configure the load balancer
---------------------------

After you create the load balancer, click on it to view the advanced
configuration options. To configure the load balancer, go to the Nodes
section and add the First Gen server to the load balancer.

**Note:** If you have SSL termination on your server, you will need
additional configuration. Enable SSL termination through the load
balancer or have two load balancers sharing the same IP to direct HTTP
and HTTPS traffic to your server.

![](/knowledge_center/sites/default/files/field/image/4782-3_8.png)

Repoint your DNS to the load balancer
-------------------------------------

1.  Go to the Cloud DNS section of the [Cloud Control
    Panel](https://mycloud.rackspace.com/).\

    ![](/knowledge_center/sites/default/files/field/image/4782-DNS-1_1.png)

2.  Select the domain that is currently pointing to your First Gen
    server.\
    ![](/knowledge_center/sites/default/files/field/image/4782-4-New_0.png)
3.  Click the gear next to your A record and select **Modify Record**.\
    \
4.  Type your load balancer IP address directly in to your browser's
    address bar to verify that your website is loading correctly.\
    \

Create a Next Gen server image
------------------------------

Follow the steps in this section to create an image of the First Gen
server that you will then use to create a Next Gen server.

**Note:** If you are on a Linux server with under 40 GB of disk in use,
you can resize down to a 1 GB flavor before taking the image. This will
allow you to boot to any Next Generation flavors that can take advantage
of our [Boot From Volume
Offering](http://www.rackspace.com/knowledge_center/article/boot-a-server-from-a-cloud-block-storage-volume).

1.  On the Cloud Servers page, click the gear icon next to the First Gen
    server that you are imaging and select **Create Image**.\

    ![](/knowledge_center/sites/default/files/field/image/4782-5_0.png)

2.  Enter a name for the image in the **Saved Image Name** field.\
    \
3.  Choose **Next Generation Cloud Server Image**.\

    ![](/knowledge_center/sites/default/files/field/image/4782-6_0.png)

4.  Click **Create Image**.

Create a Next Gen server
------------------------

Follow the steps below to create a Next Gen server.

1.  On the Cloud Servers page of the Cloud Control Panel, click **Saved
    Images**.\

    ![](/knowledge_center/sites/default/files/field/image/4782-7_0.png)

2.  Look for the image you just created and select **Create Server with
    Image**.\

    ![](/knowledge_center/sites/default/files/field/image/4782-8_0.png)

3.  Name your server and choose your preferred flavor.\

    ![](/knowledge_center/sites/default/files/field/image/4782-9_0.png)

4.  Click **Create Server** at the bottom of the page.\
    \

Switch the servers
------------------

After the server has been created, you attach it to your load balancer
by performing the following steps.

1.  On the Load Balancer Details page, click **Add Cloud Servers**.\
    \
2.  Select the server that you just created and click **Add Selected
    Servers**.\

    ![](/knowledge_center/sites/default/files/field/image/4782-11_0.png)

3.  Click the gear icon next to the First Gen server and select **Remove
    from Load Balancer**. Click **Remove Node**.\

    ![](/knowledge_center/sites/default/files/field/image/4782-13_0.png)

    **Note:** You can remove the First Gen server by using the Edit Node
    Condition feature instead. With this option, anyone currently on the
    server will be unaffected by the transition but will not be allowed
    to start new connections.

    1.  Click the gear icon next to the server and select **Edit Node
        Condition**.\

    2.  Select **Draining Connections**.\

        ![](/knowledge_center/sites/default/files/field/image/4782-14_1.png)

    3.  Click **Save Condition**.

Your server traffic will now use your Next Gen server.

Optional synchronization tools
------------------------------

You can use a tool to synchronize new data to your server.

-   FTP is the recommended tool for synchronizing data on a Windows
    server.\
    \


