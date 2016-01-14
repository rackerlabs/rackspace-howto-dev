---
node_id: 3139
title: Detach and Delete Cloud Block Storage Volumes
type: article
created_date: '2012-10-22 19:25:19'
created_by: David Hendler
last_modified_date: '2015-12-31 14:3323'
last_modified_by: stephanie.fillmon
product: Cloud Block Storage
body_format: tinymce
---

### Previous section

[Create and Use Cloud Block Storage
Snapshots](https://www.rackspace.com/knowledge_center/article/create-and-use-cloud-block-storage-snapshots)

Detaching a Cloud Block Storage volume will prevent you from writing to
it when you want to take a snapshot. It is also useful when you want to
take a volume offline for archival purposes, or to move a volume to
another server. A Cloud Block Storage volume must be detached before
resizing the server to which it is mounted. You should also detach a
volume before you delete it. In all cases, you must unmount the volume
before you detach it through the Control Panel. The instructions are
below.

On this Page:

-   [Unmount a Volume](#unmount_a_volume)
-   [Detach a Volume](#detach-a-volume)
-   [Delete a Volume](#delete-a-volume)

### Unmount a Volume

There are a few reasons to detach a volume:

-   To prevent writes when you take a snapshot
-   To prevent issues when resizing the server to which it is attached
-   To move it to another Server
-   To delete it

Before you detach a Volume from a Server, you should unmount it to
prevent errors.

**Unmount Volume from a Linux Server.**

Confirm in the Control Panel how the volume is presented to the cloud
server.

![](/knowledge_center/sites/default/files/field/image/cbs_location3_0.png)

At your server, use the df -h command to see how it is mounted.

![](/knowledge_center/sites/default/files/field/image/mount_point.png)

Use the value under **Mounted On** in the unmount command.

![](/knowledge_center/sites/default/files/field/image/fstab2_0.png)

Also, comment out second line (highlighted above) in /etc/fstab to
prevent the volume from trying to mount on the next boot.

Input:

    # umount /dev/xvdb1/

Output:

The output is the prompt ready for the next command.

    #

**Unmount a Volume from a Windows Server.**

1.  In the Server Manager, Select File and Storage Services \> Disks.
2.  Under the **Disks** window, right-click the Cloud Block Storage
    Volume. Select **Take Offline** from the pop-up menu. If the **Take
    Disk Offline** warning window displays, click Yes.

    ![](/knowledge_center/sites/default/files/field/image/win_bringoffline_0.jpeg)

The Cloud Block Storage Volume no longer displays as a drive under
**Computer**.

### Detach a Volume

In the Rackspace Cloud Control Panel, click **Block Storage** in the
Servers sub-navigation to display the **Block Storage Volumes** screen.

![](/knowledge_center/sites/default/files/field/image/cbs_detachvolume_0.jpeg)

Click the Actions button (the cog) next to the Volume name. Click the
**Detach Volume** link.

![](/knowledge_center/sites/default/files/field/image/cbs_detachvolume2_0.jpeg)

Click the **Detach Volume** button.

The Volume detaches.\
 Note: It may take several minutes for your Volume to detach.

 

### Delete a Volume

 In the Rackspace Cloud Control Panel, click **Block Storage** in the
Servers sub-navigation to display the **Block Storage Volumes** screen.

![](/knowledge_center/sites/default/files/field/image/cbs_detachvolume3.jpeg)

Click the Actions button (the cog) next to the Volume name. Click the
**Delete Volume** link.\
 \
 **Note:** If a snapshot of the volume exists, you cannot delete the
volume until you delete the snapshot.

