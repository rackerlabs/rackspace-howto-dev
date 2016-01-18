---
title: Cloud Servers
type: product
created_date: '2016-01-17'
created_by: Rackspace Support
last_modified_date: '2016-01-17'
last_modified_by: Rackspace Support
product: Cloud Servers
---

This Getting Started Guide covers everything you'll need to know as a
new Rackspace customer&mdash;including how to manage your account, create
servers, set up security, and schedule server imaging.
Use the following steps to set up a Cloud Server through the Cloud
Control Panel interface.

1.  Log in to the [Cloud Control
    Panel](https://mycloud.rackspace.com). The Cloud Servers list opens
    by default.
2.  Click the **Create Server** button.
3.  In the** Identity **section enter a name for your server in
    the **Server Name** field.

      ![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/Screen%20Shot%202015-01-14%20at%209.12.15%20AM.png){width="259"
    height="163"}

4.  From the Region list, select the region in which you want to create
    the server.

    ![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/Screen%20Shot%202015-01-14%20at%209.13.25%20AM.png){width="261"
    height="142"}
     
5.  In the **Image** section, select which operating system you want to
    use.

    ![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/Screen%20Shot%202015-01-14%20at%209.15.30%20AM.png){width="472"
    height="241"}
     
6.  In the **Flavor** section, choose the appropriate configuration for
    the server.

    ![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/Screen%20Shot%202015-01-14%20at%209.16.55%20AM.png){width="473"
    height="372"}
7.  *(Optional)* Assign a public key to the server by selecting an
    existing key.
     
    -   To assign an existing public key, under Advanced Options, select
        a public key from the drop down list.

        ![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/Screen%20Shot%202015-01-14%20at%209.18.41%20AM.png){width="379"
        height="87"}

    -   Select the public key from the list and continue with the
        next step.

8.  To add a new public key, click **Manage SSH Keys** and:

    -   On the SSH Keys page, click **Add Public Key**
    -   If you are adding a public key, give your new public key a name
    -   In the Region field, confirm or select the region in which your
        key will be used
    -   Paste your public key into the Public Key field.
        **Note:** If you do not have a public key yet, click [How to get
        a public
        key](/how-to/connecting-to-a-server-using-ssh-on-linux-or-mac-os)
        and follow the instructions in that article.
                  For more information on how to generate a public and
        private key pairs, see
                  [Manage SSH Keypairs for Cloud Servers
        with-python-novaclient](/how-to/manage-ssh-key-pairs-for-cloud-servers-with-python-novaclient).
    -   Once you have your entered your Key Name, Region, and the Public
        Key, click **Add Public Key**.


    ![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/Screen%20Shot%202015-01-14%20at%209.30.59%20AM.png){width="655"
    height="299"}
     
9.  Confirm that your key is listed in the SSH Key list for your new
    server.
     
10. As needed, create a new network and select the PublicNet and
    ServiceNet options.
     
11. Click **Create Server**.


Your server is built. After it is done being provisioned, your server
displays the status **Running** and is now available for remote
connection. Specific remote connection instructions for your server are 
displayed in the side bar on the right of the Cloud Control Panel.

 

### Next steps

### [](){#serverImages}1. Saving server images

-   [Saving a Cloud Server
    Image](/how-to/rackspace-cloud-essentials-4-restoring-cloud-server-saved-image)
-   [Restoring a Server From a
    Snapshot](/how-to/rackspace-cloud-essentials-4-restoring-cloud-server-saved-image)
-   [Snapshot
    Limitations](/how-to/rackspace-cloud-essentials-4-cloud-server-snapshot-limitations)

### [](){#remoteAccess}2. Remote access

-   [Remote Connection from Windows to a Linux
    Server](/knowledge_center/index.php/Logging_in_via_Putty)
-   [Remote Connection from Mac to a Linux
    Server](/knowledge_center/Mac_to_Linux_using_iTerm)
-   [Remote Connection to a Windows Cloud Server Using
    RDP](/how-to/log-in-to-your-server-via-rdp-windows)

### [](){#serverSecurity}3. Cloud Server security

-   [Basic Linux Cloud Server
    security](/how-to/rackspace-cloud-essentials-3-basic-cloud-server-security)[](/knowledge_center/index.php/Creating_an_Inbound_Port_Allow_Rule_for_Windows_Firewall_%28Windows_2008%29)

### [](){#uploadContent}4. Uploading your content

-   [CentOS - Installing
    vsftpd](/knowledge_center/index.php/CentOS_-_Installing_vsftpd)
-   [CentOS - Configuring a user in
    vsftpd](/knowledge_center/index.php/CentOS_-_Configuring_a_user_in_vsftpd)

### [](){#dnsDomainMGMT}5. DNS & domain management

-   [What Are Your
    Nameservers?](/knowledge_center/index.php/nameservers)
-   [Transferring Your Domain to the Rackspace
    Cloud](/how-to/transferring-your-domain-to-Rackspace-Cloud)
-   [Managing DNS](/knowledge_center/index.php/Managing_DNS)

### [](){#accountMGMT}6. Managing your account

-   [Billing services
    overview](/how-to/rackspace-cloud-essentials-1-billing-services-overview)
-   [Navigating the Cloud Control
    Panel](/how-to/navigating-the-cloud-control-panel)
-   [Generating your API
    key](/how-to/rackspace-cloud-essentials-1-generating-your-api-key-0)

### [](){#serverMGMT}7. [Managing your server](/how-to/rackspace-cloud-essentials-managing-your-server)

-   [Start a Console
    session](/how-to/managing-your-server-start-a-console-session)
-   [Reboot your
    server](/how-to/managing-your-server-reboot-your-server)
-   [Recue
    mode](/how-to/managing-your-server-rescue-mode)
-   [Rebuild a Cloud
    Server](/how-to/managing-your-server-rebuild-a-cloud-server)
-   [Resize standard
    servers](/how-to/managing-your-server-resizing-standard-servers)
-   [Reset your server
    password](/how-to/managing-your-server-reset-your-server-password)
-   [Deleting your
    server](/how-to/managing-your-server-deleting-your-server)
