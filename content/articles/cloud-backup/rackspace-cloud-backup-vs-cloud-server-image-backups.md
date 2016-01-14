---
node_id: 1427
title: Rackspace Cloud Backup vs. Cloud Server Image Backups
type: article
created_date: '2012-06-06 06:05:15'
created_by: RackKCAdmin
last_modified_date: '2015-12-31 20:2708'
last_modified_by: stephanie.fillmon
product: Cloud Backup
body_format: tinymce
---

Some users are used to taking snapshots of their Cloud Server ([product
page](http://www.rackspace.com/cloud/servers)) as a backup. If you have
a solution where you want to save the server&rsquo;s state or configuration,
or want to keep gold copies of your system, then you can create an image
backup of the server. Because it is an image of the whole server, there
is really no control over the individual files. You cannot, say, recover
a single file from that image, or update a single file. But, on the
other hand, having a single file to manage (the image) allows you to
easily recreate a new server with that identical configuration and
state.<br>
 **Note:** You can learn more about scheduling images from the
[Scheduled Images
FAQ](http://www.rackspace.com/knowledge_center/article/scheduled-images-faq).

Rackspace Cloud Backup, on the other hand, is a **FILE-BASED backup**.
This means that you can specify what folders or files to backup or
restore. As usual, you can choose to backup or restore the whole system
with all its folders, but the distinction with image backups is that the
granularity of Rackspace Cloud Backup is at the file level, as opposed
to it being at the whole server image level.

Moreover, Rackspace Cloud Backup is also an **INCREMENTAL backup** tool
in that it only copies the portion of the files that changed for those
files that actually changed. This gives you some flexibility because,
with the exception of your first complete backup, every subsequent
backup is just a &ldquo;delta&rdquo; of the previous backup, which makes for faster
backup and restores operations and also reduces the storage required. As
you probably know, image backups are not incremental: they copy the
whole system every time.

Rackspace customers now have two options for backing up their Cloud
Servers. Below is a summary of both:

-   **Rackspace Cloud Backup** - Rackspace Cloud Backup is a fully
    integrated, file-based backup solution that helps protect your data
    on cloud servers. For additional information, check out our
    Rackspace Cloud Backup Overview - [Rackspace Cloud Backup
    Overview](http://www.rackspace.com/knowledge_center/article/rackspace-cloud-backup-overview)

-   **Cloud Server Image Backup** - Cloud Server Image Backup is a copy
    of the entire state of a Cloud Server stored either on Cloud Files
    or on the Cloud Server's host, depending on the environment. Images
    can be scheduled or created on-demand. For additional information,
    check out Cloud Server Image Backup - [Creating A New Cloud Server
    From A Saved
    Image](http://www.rackspace.com/knowledge_center/article/create-an-image-of-a-server-and-restore-a-server-from-a-saved-image)

**NOTE:** With General Purpose and I/O-optimized Cloud Servers, only the
system disk is captured when using an Image Backup. If you require
backups of your data disk or disks, use Cloud Backup so you configure
your backup to include the specific drives and directories you want to
retain. To determine which product best suits your backup needs, visit
the links below:

-   **[Cloud Block Storage
    Overview](http://www.rackspace.com/knowledge_center/article/cloud-block-storage-overview)**
-   **[Best Practices for Backing Up Your Data: Cloud Block Storage
    versus Cloud
    Backup](http://www.rackspace.com/knowledge_center/article/best-practices-for-backing-up-your-data-cloud-block-storage-versus-cloud-backup)**


