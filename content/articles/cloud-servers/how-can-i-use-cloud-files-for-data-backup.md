---
node_id: 236
title: Back up data with Cloud Files
type: article
created_date: '2011-03-16 21:57:40'
created_by: RackKCAdmin
last_modified_date: '2015-05-12 17:1336'
last_modified_by: kelly.holcomb
product: Cloud Servers
body_format: tinymce
---

Using Cloud Files to back up your data is a straightforward process. Use
the steps in this article to set up your own data backup to your Cloud
Files service.

**Note:** If you would like for us to provide Cloud Backup as a service,
see
[http://www.rackspace.com/cloud/backup](http://www.rackspace.com/cloud/backup)
for information.

Prepare to back up {#prepare}
------------------

Before you use Cloud files to back up your data, perform the following
steps to prepare your data:

1.  Create a backup plan, identifying critical resources and necessary
    frequency.
2.  Collect all the critical resources (backup data) in a secure local
    location or directory with any needed subdirectories.
3.  *(Optional)* Compress the content of the backup directory with
    security and encryption.<br>
     This optional step saves storage and bandwidth costs and increases
    security.

Back up your data
-----------------

1.  Log in to the [Cloud Control Panel](https://mycloud.rackspace.com/).
2.  At the top of the window, click **Storage \> Files**.

    ![](/knowledge_center/sites/default/files/field/image/236.1.png)

3.  On the Cloud Files page, click **Create Container**.
4.  In the popup dialog box, name the new container, select the region
    and type, and then click **Create Container**.<br>
     For more information about selecting a region for your backup
    files, see [Multi-region support in Cloud
    Files](http://www.rackspace.com/knowledge_center/node/2157).
5.  *(Optional)* If you want to create a folder to group your uploaded
    files, perform the following steps:
    1.  On the Containers page, click **Create Folder**.
    2.  In the popup dialog box, name the folder and then click **Create
        Folder**.
    3.  To add files in the folder, click the folder name to open the
        folder before completing the following step.

6.  Individually upload the backup data files that you created in step 2
    of [Prepare to back up](#prepare) to the container, as follows:
    1.  On the Containers page, click **Upload Files**.

        ![](/knowledge_center/sites/default/files/field/image/263.4.png)

    2.  Select the files and then click **Open**.<br>
         Your files are uploaded to the container.

Next steps
----------

1.  Update your backup records with the current date as the date of the
    last backup.
2.  Perform the next backup (that is, upload files to Cloud Files)
    according to the backup plan that you created.


