---
node_id: 1474
title: Reboot Your Server
type: article
created_date: '2012-07-19 06:21:12'
created_by: ari.liberman
last_modified_date: '2016-01-04 19:3917'
last_modified_by: cat.lookabaugh
product: Cloud Servers
body_format: tinymce
---

### Previous section

[Getting Started with Cloud
Servers](http://www.rackspace.com/knowledge_center/article/getting-started-with-cloud-servers-0)

 

You can reboot a server in one of two ways. A *soft reboot* uses the
operating system's reboot process so that applications are shut down
gracefully. A *hard reboot* halts the instance and then restarts it,
similar to turning a computer off and then on.

We recommend attempting a soft reboot of a server whenever possible,
using a hard reboot only when the server is unresponsive.

Note: You should ensure that critical services will start at reboot and
that there are no tasks pending that could slow the reboot process.

Perform a soft reboot
---------------------

To perform a soft reboot of a server, you must be logged in to the
server using an account with superuser or administrator permissions. For
information about logging in to a cloud server, see [Connect to a cloud
server](http://www.rackspace.com/knowledge_center/article/connect-to-a-cloud-server).

**Note**: OS reboots, such as the ` sudo reboot `shown below,  do not
trigger the FG2NG migration.

For the command you should use to soft reboot your server, see the
appropriate section for your server operating system:

### Linux

    sudo reboot

### Windows

Issue a restart request by clicking **Start** \> **Shut down**.

Alternatively, you can initiate a soft reboot from the command line by
entering the following command:

    shutdown /r

Perform a hard reboot
---------------------

If your server is not responding or was shut down manually, perform a
hard reboot via the Cloud Control Panel to simulate power cycling the
server.

**Warning:** A hard reboot does not shut down applications gracefully
and can result in data loss.

1.  Log in to the [Cloud Control Panel](https://mycloud.rackspace.com/).
2.  On the Servers page, click the gear icon next to the server that you
    want to reboot.
3.  Select** Reboot**.

    ![](/knowledge_center/sites/default/files/field/image/rebootmenu_0.png)

4.  In the pop-up dialog box, click **Reboot Server**.

    ![](/knowledge_center/sites/default/files/field/image/Hard%20Reboot_0.png)

The server status on the Servers page updates while the server is
rebooting. When the reboot is complete, check your server to confirm
that everything is functioning as expected.

Halt a server
-------------

You can also shut down a server to put it in a *halted*state, in
which no operating systems or applications are running. Restoring a
halted server to operation requires you to perform a hard reboot using
the Cloud Control Panel.

To halt a server, you need remote access to the server using an account
with superuser or administrator permissions. For information about
logging in to a cloud server, see [Connect to a cloud
server](http://www.rackspace.com/knowledge_center/article/connect-to-a-cloud-server).

**Note:** Shutting down a server does *not* stop billing for the server,
because resources are still allocated to the server instance. Billing
for a server stops only when the server is deleted.

### Linux

Log in as a sudo-enabled user via SSH and enter the following command:

    sudo shutdown -h now

The command shuts down the serverm and you must perform a hard reboot to
restart the server.

### Windows

Log in to your server and issue a shutdown request by
clicking **Start** \> **Shut down**.

Alternatively, you can issue a shutdown from the command line by
entering the following command:

    shutdown /s

 

### Next section

[Recue
mode](http://www.rackspace.com/knowledge_center/article/managing-your-server-rescue-mode)

