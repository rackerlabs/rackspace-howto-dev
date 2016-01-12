---
node_id: 3708
title: Upgrading resources for General Purpose or I/O optimized Cloud Servers
permalink: article/changing-the-size-of-your-performance-flavor-server
type: article
created_date: '2013-09-25 21:08:13'
created_by: kyle.laffoon
last_modified_date: '2016-01-05 20:5714'
last_modified_by: Mike Asthalter
products: Cloud Servers
body_format: tinymce
---

In the architecture of General Purpose Cloud Servers and I/O-optimized
servers, you may change the size of your local system storage space in
one of two ways:

-   [Increase Available Storage with Cloud Block
    Storage](http://www.rackspace.com/knowledge_center/article/upgrading-resources-for-general-purpose-or-io-optimized-cloud-servers#increasestorage)
-   [Create a new server with more
    resources](http://www.rackspace.com/knowledge_center/article/upgrading-resources-for-general-purpose-or-io-optimized-cloud-servers#changeflavor) 

Note that these instructions apply to General Purpose and I/O optimized
servers with local system disks only. Resource allocation for servers
that boot from Cloud Block Storage volumes can be changed by using the
boot volume to create a new server.

Increasing Available Storage
----------------------------

You can add to the available data storage space of your server by adding
Cloud Block Storage volumes. Cloud Block Storage volumes come in two
types: SATA for standard performance and SSD for high performance. For
more information about Cloud Block Storage, see [Create and Attach a
Cloud Block Storage
Volume](http://www.rackspace.com/knowledge_center/article/create-and-attach-a-cloud-block-storage-volume).

Creating a new server with more resources
-----------------------------------------

You can migrate your data to a new server with a larger allocation
of RAM, vCPUs, data disks, and network throughput if you require more
capacity.  Note that a saved image cannot be used to create a server
with a smaller system disk allocation than the original server.

You can migrate your data to a new server by performing the following
steps:

1.  Create an image of your system disk. (See [Create an image or
    restore a Cloud Server from an
    image](http://www.rackspace.com/knowledge_center/article/create-an-image-of-a-server-and-restore-a-server-from-a-saved-image) for
    more information.)
2.  Back up your data disk, either to a [Cloud Block Storage
    volume](http://www.rackspace.com/knowledge_center/article/create-and-attach-a-cloud-block-storage-volume)
    or with [Cloud
    Backup](http://www.rackspace.com/knowledge_center/getting-started/cloud-backup).\
     **Notes**:
    -   To decide between these options, consider your needs. For
        information about the advantages of each, see [Best Practices
        for Backing Up Your Data: Cloud Block Storage versus Cloud
        Backup](http://www.rackspace.com/knowledge_center/article/best-practices-for-backing-up-your-data-cloud-block-storage-versus-cloud-backup).
    -    If you have rsync (Linux) or xcopy/robocopy (Microsoft Windows)
        installed on your server, you can use it to migrate data from
        your data disks after you have created the new server in step 3.

3.  Use the image of your system disk to create a new server with the
    configuration that you prefer.  From the control panel select
    **Servers** then select **Create Server**.\
     **Note**: Create the server as normal, however, from the **Image**
    section you will need to select the image from the **Saved** tab
    rather than the stock Rackspace images.
4.  Copy the data from your data disk backup to your new data disk.
5.  When you are satisfied with your new server, delete the old one.

 Additional Resources
---------------------

You can use Auto Scale to accomplish server resizing keeping your IP
address, and have it happen dynamically in response to load. For
details, see the Rackspace Auto Scale tip [How to use Auto Scale to
change the size of your General Purpose or
optimized servers](http://www.rackspace.com/knowledge_center/article/rackspace-auto-scale-tips-and-how-tos#changePerfServerSize).

