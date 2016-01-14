---
node_id: 2038
title: Rackspace Cloud Backup - Create a backup
type: article
created_date: '2012-08-22 19:00:02'
created_by: David Hendler
last_modified_date: '2016-01-04 20:0828'
last_modified_by: rose.contreras
product: Cloud Backup
body_format: full_html
---

The following steps show how to use the Cloud Backup service to create a
backup of the data on your cloud server.

### Previous sections

-   [Rackspace Cloud Backup -
    Overview](http://www.rackspace.com/knowledge_center/article/rackspace-cloud-backup-overview)
-   [Rackspace Cloud Backup - Install the agent on
    Linux](http://www.rackspace.com/knowledge_center/article/rackspace-cloud-backup-install-the-agent-on-linux)
-   [Rackspace Cloud Backup - Install the agent on
    Windows](https://www.rackspace.com/knowledge_center/article/rackspace-cloud-backup-install-the-agent-on-windows)

**Note:** You can use the Cloud Backup tool to back up your data files
but not to back up a full operating system. To restore your data, you
need to restore only your files; you do not need to restore all of the
operating system files. To back up the operating system, create an image
of your server. For more information about restoring a server from an
image, see [Create an image of a server and restore a server from a
saved
image](http://www.rackspace.com/knowledge_center/article/create-an-image-of-a-server-and-restore-a-server-from-a-saved-image).

Create a server backup
----------------------

1.  Log in to the [Cloud Control
    Panel](https://mycloud.rackspace.com/).\
    \
2.  In the top navigation bar, select **Backups \> Systems**.\

    ![](/knowledge_center/sites/default/files/field/image/2038-1_0.png)

3.  On the Cloud Backup Systems page, click the name of the server for
    which you want to create a backup.

    **Note:** If you do not see your server listed on this page, you
    must install the backup agent on the server. If you have an account
    with the Managed Operations service level, check with your account
    manager to install the agent. If your account has a different
    service level, follow the instructions in [How to Install the
    Agent](https://admin.rackspace.com/knowledge_center/article/rackspace-cloud-backup-install-the-agent).

4.  On the Configure Backup page, configure the following items and then
    click **Next Step:**\
    \
    -   Enter a name for the backup.\
        \
    -   In the **Schedule** section, specify a schedule for the backup
        and select how many prior backup versions to retain.\
        \
    -   In the **Notifications** section, specify the email address for
        notifications and select whether you want to receive
        notifications of successful backups.\
        \

5.  On the Select Items to Backup page, select the files and folder to
    back up, and then click **Next Step**.\
    \
6.  Confirm that the backup agent is set up correctly, and then click
    **Save**.\
    \

### Next steps

[Rackspace Cloud Backup - View backup
information](http://www.rackspace.com/knowledge_center/article/rackspace-cloud-backup-view-backup-information)

