---
node_id: 2039
title: Rackspace Cloud Backup - View backup information
permalink: article/rackspace-cloud-backup-backup-information-0
type: article
created_date: '2012-08-22 19:06:31'
created_by: David Hendler
last_modified_date: '2015-05-18 18:1346'
last_modified_by: rose.contreras
products: Cloud Backup
categories: Backups
body_format: markdown_w_tinymce
---

### Getting Started with Rackspace Cloud Backup - Part 3

The previous article explained [how to create a backup](/knowledge_center/node/2038). After your backup is set up, you might want to
confirm its settings, ensure that a cleanup or restore action finished successfully, or even manually start a job before it's
scheduled. You might also want to quickly view all of your backup activity at once. This article describes how to perform these
activities.

You can view either [a single backup's
activities](https://admin.rackspace.com/knowledge_center/article/rackspace-cloud-backup-backup-information-0#single) or [all
activities for all backups](https://admin.rackspace.com/knowledge_center/article/rackspace-cloud-backup-backup-information-0#all).

## View information for a single backup

In the [Cloud Control Panel](https://mycloud.rackspace.com), click **Backups &gt; Backups** in the top navigation bar.

The list of all the backup processes that you currently have on your account is displayed.

<p><img alt="" height="170" src="/knowledge_center/sites/default/files/field/image/1842-2039-IMG-1.png" width="476" border="1"
/></p>

### Find a backup

The list of backups has three columns: Name, System, and Last Run. You can sort by each column by clicking its title.

If you have a long list of backups, you can search for the one that you want in the **Search** box.


### View the settings and activity for a backup

To view the settings for a particular backup, click its name in the list of backups. The backup details page is displayed.

<p><img alt="" height="379" src="/knowledge_center/sites/default/files/field/image/1842-2039-IMG-2.png" width="474" border="1"
/></p>

The Configuration Details section displays the configuration details for the backup.

The Activity list displays all the actions that a backup has performed (such as Backup, Cleanup, and Restore) listed historically.
The most recent actions are at the top.

If the list of activities is long, you can limit the list by performing a search. Enter your search term in the **Search** box. You can
search with the following terms:

- Backup

- Restore

- Cleanup - Fail | Complete | Skipped

View the details of a backup's activity by clicking **View Details** in its entry.

You can also view the server details by clicking the name of the server, or you can redisplay the backup details page by clicking
the backup's name in the activity entry.


### Perform a backup

If you do not want to wait for the next scheduled backup, you can trigger a manual backup by clicking the **Perform
Backup** button in the Activity section.

## View activity for all backups

You can view the backup activity for all of your systems by selecting the Backups > Activity from the top navigation bar of the
control panel. The Activity list displays all the actions that the backups have performed (such as Backup, Cleanup, and Restore)
listed historically. The most recent actions are at the  top.

<p><img alt="" height="323" src="/knowledge_center/sites/default/files/field/image/1842-2039-IMG-3.png" width="666" border="1"
/></p>

If the list of activities is long, you can limit your list by performing a search. Enter your search term in the Search box. You can
search by the following terms:

- Backup

- Restore

- Cleanup

- [Backup Name]

- [System Name]

- Fail | Complete | Skipped

You can view the details of a backup's activity by clicking **View Details** in its entry.

You can also view the server details by clicking the name of the server, or you can display the details page for the backup by
clicking the backup's name in the activity entry.
