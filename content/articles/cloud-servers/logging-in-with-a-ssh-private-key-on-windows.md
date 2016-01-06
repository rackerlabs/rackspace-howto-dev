---
node_id: 3707
title: Logging in with an SSH Private Key on Windows
permalink: article/logging-in-with-a-ssh-private-key-on-windows
type: article
created_date: '2013-09-25 15:20:06'
created_by: brint.ohearn
last_modified_date: '2015-07-23 16:1059'
last_modified_by: margaret.eker
products: Cloud Servers
body_format: tinymce
---

#### Introduction

In this example, we&rsquo;re going to demonstrate how to load a private key
into PuTTY. You&rsquo;ll need two pieces of software to complete this task:

1.  PuTTY &ndash; Client to for managing SSH sessions
2.  PuTTYgen &ndash; Tool for managing and creating SSH key pairs

Both tools can be downloaded here:

[http://www.chiark.greenend.org.uk/\~sgtatham/putty/download.html.](http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html)

**Note: ** These instructions apply to the Windows operating system. 
For information about using SSH private keys on Linux and OS X operating
systems, see [Logging in with a SSH Private Key on Linux and OS
X](http://www.rackspace.com/knowledge_center/article/logging-in-with-a-ssh-private-key-on-linuxmac).

 

#### PuTTYgen: Loading the Key

As a part of a Rackspace Deployment, you may be provided a SSH Private
Key to be used for authentication against your newly deployed Linux
servers. The first thing to do is save this private key into a file.
Here&rsquo;s an example key:

![](/knowledge_center/sites/default/files/field/image/Windows1.png)

You will need everything you see in the example above to be included in
your key file.

Now launch PuTTYgen:

![](/knowledge_center/sites/default/files/field/image/Windows2.png)

Click **load** and change the file type to search for to **All Files:**

![](/knowledge_center/sites/default/files/field/image/Windows3.png)

Select the key you saved to a text file earlier and click **Open**:

![](/knowledge_center/sites/default/files/field/image/Windows4.png)

Now PuTTYgen will confirm that your key has been loaded:

![](/knowledge_center/sites/default/files/field/image/Windows5.png)

Enter a unique key passphrase in the **Key passphrase** and **Confirm
passphrase** fields. You will be prompted for that passphrase whenever
you login to a server with this key.

![](/knowledge_center/sites/default/files/field/image/Windows6.png)

 

We strongly suggest keeping the default settings as they are, so when
you're prompted to "Enter a file in which to save the key", just press
**Enter** to continue.\
 \
 ![](/knowledge_center/sites/default/files/field/image/Windows8.png)

 

#### PuTTY: Logging in with the Private Key

Setup your session in PuTTy. You can name the session anything you would
like. In this case, we are naming the session based on the IP of the
server we are connecting to, and click **Save**:

![](/knowledge_center/sites/default/files/field/image/Windows9.png)

Now click on **Connection \>Data** and set the Auto-login username to
root:

![](/knowledge_center/sites/default/files/field/image/win9.png)

Click on **Auth** and configure the Private Key to use by clicking
Browse under Private key file for authentication:

![](/knowledge_center/sites/default/files/field/image/Windows10.png)

Navigate to the location where you saved your private key earlier,
select the file, and click **Open**:

![](/knowledge_center/sites/default/files/field/image/Windows11.png)

Now you&rsquo;ll see the private key path listed:

![](/knowledge_center/sites/default/files/field/image/Windows12.png)

Navigate back to **Session** and save this session information one more
time.

![](/knowledge_center/sites/default/files/field/image/Windows13.png)

Now click **Open** to begin your session with the server. If you saved
you key with a passphrase, you will be prompted to enter that
passphrase. You will be given an alert that the server&rsquo;s host is not
cached. Click **Yes**at this point to continue the connection.

![](/knowledge_center/sites/default/files/field/image/Windows14.png)

Now you will be in logged into your server:

![](/knowledge_center/sites/default/files/field/image/Windows15.png)

