---
node_id: 3854
title: Managing Backups for Cloud Databases
type: article
created_date: '2014-01-15 18:54:37'
created_by: Rackspace Support
last_modified_date: '2014-01-21 00:5534'
last_modified_by: ross.diaz
product: Cloud Databases
body_format: tinymce
---

You can perform the following operations on your Rackspace Cloud
Databases instances.

-   [Create a backup](#CreateBackup)
-   [List details of all backups for the account](#ListDetails)
-   [List details of all backups for an instance](#ListDetailsInstance)
-   [Delete a backup](#DeletingBackups)
-   [Restore a backup](#RestoringBackups)

### 

### Create a Backup

To create backup of a database instance, click the Actions cog next to
the name of the instance you want to backup, and select **Create
Backup**.  Once selected, a dialogue box will open, asking for a backup
name and description.<br>
<br>
![](/knowledge_center/sites/default/files/field/image/CreateBackup.png)<br>
You can also create a backup by clicking on the instance name and
selecting the **Create Backup... **link on under the **Instance
Details** section.

![](/knowledge_center/sites/default/files/field/image/InstanceDetails.png)

-   The name of the backup is required, and the maximum length for the
    name is 64 characters.
-   Backups are stored directly in your Cloud Files account and you will
    be charged for the storage used.  Standard rates for Cloud Files
    storage fees apply. 

<br>
**WARNING**:  The behavior of your instance during a backup depends on
the storage engine that you are using for tables.  If you use only
InnoDB, write access to your database instance is not suspended. 
Conversely, if you have MyISAM tables, those databases are write-locked
during the backup process.<br>
<br>
**Things to Consider**

-   While the instance is being backed up you will not be able to
    add/delete databases, add/delete users, or delete/stop/reboot the
    instance.
-   You can only run one backup at a time. Duplicate requests will
    receive a 422 error.
-   Backups are not deleted when the instance is deleted. You must
    delete any backups that are not required.
-   During a backup, the backup files will be saved directly to your
    Cloud Files account. The process creates a container called
    z\_CLOUDDB\_BACKUPS and places all the files in it. In order for the
    restore and deletion of backups to work properly, you should not
    move, rename, or delete any of the files from this container.

### List Details of all backups for the account

To view list of all the backups, you can click on the **Backups** link
in the top menu row next to **MySQL Instances**. You will see the
following details for your backups:<br>
<br>

-   The Backup Name assigned by the user.
-   The instance that was backed up.
-   The date the backup was created. 
-   The most recent date the backup was updated.

<br>
![](/knowledge_center/sites/default/files/field/image/ListBackup.png)<br>
<br>
You can also filter the backups for different regions by clicking on the
**Regions** filter from the drop-down.<br>

### List Details of All Backups for an Instance

To view all the backups for an instance, click on the instance name to
view the Instance Details page.  there is a link for all the backups
associated for that instance.

![](/knowledge_center/sites/default/files/field/image/ListDetailsInstance.png)

### Delete a Backup

To delete a backup you can click on the Actions cog next to the backup
name.<br>
<br>
![](/knowledge_center/sites/default/files/field/image/InstanceBackups.png)

You can also delete any backups for an instance from the **Instance
Details** page.

### Restore a Backup

To restore a backup, click on the Actions cog next to the backup name.<br>
<br>
![](/knowledge_center/sites/default/files/field/image/RestoreBackup.png)

You can also restore any backup for an instance from within the Instance
Details page.<br>
<br>
Once the option to restore a backup has been selected, you will be
prompted to enter the instance name, flavor, and volume size of the
backup that needs to be restored.  The volume size will be set by
default to the value of the original size of the database before the
backup.  You must specify a volume greater than that of the original
size of the database.<br>
<br>
All user accounts, credentials, and access permissions that were saved
on the instance at the time of the backup will be restored along with
the databases. Once restored, you can create new users or databases, but
they cannot be the same as the ones from the instance that was backed
up.<br>
<br>


