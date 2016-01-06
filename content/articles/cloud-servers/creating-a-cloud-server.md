---
node_id: 1468
title: Getting Started with Cloud Servers
permalink: article/creating-a-cloud-server
type: article
created_date: '2012-07-17 00:27:22'
created_by: RackKCAdmin
last_modified_date: '2015-12-31 20:3914'
last_modified_by: kyle.laffoon
products: Cloud Servers
body_format: tinymce
---

This Getting Started Guide covers everything you'll need to know as a
new Rackspace customer&mdash;including how to manage your account, create
servers, set up security, and schedule server imaging.\
 Use the following steps to set up a Cloud Server through the Cloud
Control Panel interface.

1.  Log in to the [Cloud Control
    Panel](https://mycloud.rackspace.com). The Cloud Servers list opens
    by default.
2.  Click the **Create Server** button.
3.  In the** Identity **section enter a name for your server in
    the **Server Name** field.

    ![](/knowledge_center/sites/default/files/field/image/Screen%20Shot%202015-01-14%20at%209.12.15%20AM.png)

4.  From the Region list, select the region in which you want to create
    the server.\
     \

    ![](/knowledge_center/sites/default/files/field/image/Screen%20Shot%202015-01-14%20at%209.13.25%20AM.png)\
      
5.  In the **Image** section, select which operating system you want to
    use.\
     \

    ![](/knowledge_center/sites/default/files/field/image/Screen%20Shot%202015-01-14%20at%209.15.30%20AM.png)\
      
6.  In the **Flavor**section, choose the appropriate configuration for
    the server.\
     \

    ![](/knowledge_center/sites/default/files/field/image/Screen%20Shot%202015-01-14%20at%209.16.55%20AM.png)
7.  *(Optional)* Assign a public key to the server by selecting an
    existing key.\
      
    -   To assign an existing public key, under Advanced Options, select
        a public key from the drop down list.\
         \

        ![](/knowledge_center/sites/default/files/field/image/Screen%20Shot%202015-01-14%20at%209.18.41%20AM.png)\
          
    -   Select the public key from the list and continue with the next
        step.

8.  To add a new public key, click **Manage SSH Keys** and:\
     
    -   On the SSH Keys page, click **Add Public Key**
    -   If you are adding a public key, give your new public key a name
    -   In the Region field, confirm or select the region in which your
        key will be used
    -   Paste your public key into the Public Key field.\
         **Note:** If you do not have a public key yet, click [How to
        get a public
        key](http://www.rackspace.com/knowledge_center/article/connecting-to-a-server-using-ssh-on-linux-or-mac-os)
        and follow the instructions in that article.\
                   For more information on how to generate a public and
        private key pairs, see\
                   [Manage SSH Keypairs for Cloud Servers
        with-python-novaclient](http://www.rackspace.com/knowledge_center/article/manage-ssh-key-pairs-for-cloud-servers-with-python-novaclient).
    -   Once you have your entered your Key Name, Region, and the Public
        Key, click **Add Public Key**.

    \

    ******![](/knowledge_center/sites/default/files/field/image/Screen%20Shot%202015-01-14%20at%209.30.59%20AM.png)\
      
9.  Confirm that your key is listed in the SSH Key list for your new
    server.\
      
10. As needed, create a new network and select the PublicNet and
    ServiceNet options.\
      
11. Click **Create Server**.

\
 Your server is built. After it is done being provisioned, your server
displays the status **Running** and is now available for remote
connection. Specific remote connection instructions for your server are 
displayed in the side bar on the right of the Cloud Control Panel.

 

### Next steps

### 1. Saving server images {#list-area-2}

-   [Saving a Cloud Server
    Image](http://www.rackspace.com/knowledge_center/article/rackspace-cloud-essentials-4-restoring-cloud-server-saved-image)
-   [Restoring a Server From a
    Snapshot](http://www.rackspace.com/knowledge_center/article/rackspace-cloud-essentials-4-restoring-cloud-server-saved-image)
-   [Snapshot
    Limitations](http://www.rackspace.com/knowledge_center/article/rackspace-cloud-essentials-4-cloud-server-snapshot-limitations)

### 2. Remote access {#list-area-3}

-   [Remote Connection from Windows to a Linux
    Server](http://www.rackspace.com/knowledge_center/index.php/Logging_in_via_Putty)
-   [Remote Connection from Mac to a Linux
    Server](http://www.rackspace.com/knowledge_center/Mac_to_Linux_using_iTerm)
-   [Remote Connection to a Windows Cloud Server Using
    RDP](https://admin.rackspace.com/knowledge_center/article/log-in-to-your-server-via-rdp-windows)

### 3. Cloud Server security {#list-area-4}

-   [Basic Linux Cloud Server
    security](http://www.rackspace.com/knowledge_center/content/rackspace-cloud-essentials-3-basic-cloud-server-security)
-   [Creating an inbound predefined Allow Rule for Windows Firewall
    2008](http://www.rackspace.com/knowledge_center/index.php/Creating_an_Inbound_Predefined_Allow_Rule_for_Windows_Firewall_%28Windows_2008%29)
-   [Creating an Inbound Port Allow Rule for Windows Firewall
    2008](http://www.rackspace.com/knowledge_center/index.php/Creating_an_Inbound_Port_Allow_Rule_for_Windows_Firewall_%28Windows_2008%29)

### 4. Uploading your content {#list-area-5}

-   [CentOS - Installing
    vsftpd](http://www.rackspace.com/knowledge_center/index.php/CentOS_-_Installing_vsftpd)
-   [CentOS - Configuring a user in
    vsftpd](http://www.rackspace.com/knowledge_center/index.php/CentOS_-_Configuring_a_user_in_vsftpd)
-   [Ubuntu - Installing
    vsftpd](http://www.rackspace.com/knowledge_center/index.php/Ubuntu_-_Installing_vsftpd)
-   [Secure File Transfer Protocol
    (SFTP)](http://www.rackspace.com/knowledge_center/index.php/Secure_File_Transfer_Protocol_%28SFTP%29)
-   [Creating an FTP site in IIS
    7.0](http://www.rackspace.com/knowledge_center/index.php/Creating_an_FTP_Site)

### 5. DNS & domain management {#list-area-6}

-   [What Are Your
    Nameservers?](http://www.rackspace.com/knowledge_center/index.php/nameservers)
-   [Transferring Your Domain to the Rackspace
    Cloud](http://www.rackspace.com/knowledge_center/content/transferring-your-domain-to-Rackspace-Cloud)
-   [Managing
    DNS](http://www.rackspace.com/knowledge_center/index.php/Managing_DNS)
-   [Using Dig for DNS
    Troubleshooting](http://www.rackspace.com/knowledge_center/index.php/DNS_-_Introduction_to_dig)

### 6. Managing your account

-   [Billing services
    overview](https://admin.rackspace.com/knowledge_center/article/rackspace-cloud-essentials-1-billing-services-overview)
-   [Getting fanatical
    support](https://admin.rackspace.com/knowledge_center/article/rackspace-cloud-essentials-1-getting-fanatical-support-0)
-   [Navigating the Cloud Control
    Panel](https://admin.rackspace.com/knowledge_center/video/navigating-the-cloud-control-panel)
-   [Generating your API
    key](https://admin.rackspace.com/knowledge_center/article/rackspace-cloud-essentials-1-generating-your-api-key-0)

### 7. [Managing your server](https://www.rackspace.com/knowledge_center/article/rackspace-cloud-essentials-managing-your-server)

-   [Start a Console
    session](https://www.rackspace.com/knowledge_center/article/managing-your-server-start-a-console-session)
-   [Reboot your
    server](https://www.rackspace.com/knowledge_center/article/managing-your-server-reboot-your-server)
-   [Recue
    mode](https://www.rackspace.com/knowledge_center/article/managing-your-server-rescue-mode)
-   [Rebuild a Cloud
    Server](https://www.rackspace.com/knowledge_center/article/managing-your-server-rebuild-a-cloud-server)
-   [Resize standard
    servers](https://www.rackspace.com/knowledge_center/article/managing-your-server-resizing-standard-servers)
-   [Reset your server
    password](https://www.rackspace.com/knowledge_center/article/managing-your-server-reset-your-server-password)
-   [Deleting your
    server](https://www.rackspace.com/knowledge_center/article/managing-your-server-deleting-your-server)


