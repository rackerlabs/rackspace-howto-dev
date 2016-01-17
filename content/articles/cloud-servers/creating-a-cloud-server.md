---
node_id: 1468
title: Getting Started with Cloud Servers
type: article
created_date: '2012-07-17'
created_by: Rackspace Support
last_modified_date: '2016-01-14'
last_modified_by: Stephanie Fillmon
product: Cloud Servers
body_format: tinymce
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
        key](/howto/connecting-to-a-server-using-ssh-on-linux-or-mac-os)
        and follow the instructions in that article.
                  For more information on how to generate a public and
        private key pairs, see
                  [Manage SSH Keypairs for Cloud Servers
        with-python-novaclient](/howto/manage-ssh-key-pairs-for-cloud-servers-with-python-novaclient).
    -   Once you have your entered your Key Name, Region, and the Public
        Key, click **Add Public Key**.


    ******![](https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/Screen%20Shot%202015-01-14%20at%209.30.59%20AM.png){width="655"
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

### <span>[](){#serverImages}1</span><span>.</span> Saving server images {#list-area-2}

<div class="six columns omega">

-   [Saving a Cloud Server
    Image](/howto/create-an-image-of-a-server-and-restore-a-server-from-a-saved-image)
-   [Restoring a Server From a
    Snapshot](/howto/create-an-image-of-a-server-and-restore-a-server-from-a-saved-image)
-   [Snapshot
    Limitations](/howto/rackspace-cloud-essentials-cloud-server-image-limitations)

</div>

<div class="getting-started-row-2">

<div class="six columns alpha">

### <span>[](){#remoteAccess}2.</span> Remote access {#list-area-3}

-   [Remote Connection from Windows to a Linux
    Server](/howto/connecting-to-linux-from-windows-by-using-putty)
-   [Remote Connection from Mac to a Linux
    Server](/howto/connecting-to-linux-from-mac-os-x-by-using-terminal)
-   [Remote Connection to a Windows Cloud Server Using
    RDP](/howto/log-in-to-your-server-via-rdp-windows)

</div>

<div class="six columns omega">

### <span>[](){#serverSecurity}3.</span> Cloud Server security {#list-area-4}

-   [Basic Linux Cloud Server
    security](/howto/basic-cloud-server-security)[](http://www.rackspace.com/knowledge_center/index.php/Creating_an_Inbound_Port_Allow_Rule_for_Windows_Firewall_%28Windows_2008%29)

</div>

</div>

<div class="getting-started-row-3">

<div class="six columns alpha">

### <span>[](){#uploadContent}4.</span> Uploading your content {#list-area-5}

-   [CentOS - Installing
    vsftpd](/howto/rackspace-cloud-essentials-centos-installing-vsftpd)
-   [CentOS - Configuring a user in
    vsftpd](/howto/rackspace-cloud-essentials-centos-configuring-a-user-in-vsftpd)

</div>

<div class="six columns omega">

### <span>[](){#dnsDomainMGMT}5.</span> DNS & domain management {#list-area-6}

-   [What Are Your
    Nameservers?](/howto/rackspace-cloud-essentials-what-are-your-name-servers)
-   [Transferring Your Domain to the Rackspace
    Cloud](/howto/rackspace-cloud-essentials-transferring-your-domain-to-be-served-from-rackspace-cloud)
-   [Managing
    DNS](/howto/create-dns-records-for-cloud-servers-with-the-control-panel)

### <span>[](){#accountMGMT}6.</span> Managing your account

-   [Billing services
    overview](/howto/billing-services-overview)
-   [Navigating the Cloud Control
    Panel](/howto/introducing-the-rackspace-cloud-control-panel)
-   [Generating your API
    key](/howto/view-and-reset-your-api-key)

</div>

</div>

### <span>[](){#serverMGMT}7.</span> [Managing your server](/howto/managing-your-server)

-   [Start a Console
    session](/howto/start-a-console-session)
-   [Reboot your
    server](/howto/reboot-your-server)
-   [Recue
    mode](/howto/rescue-mode)
-   [Rebuild a Cloud
    Server](/howto/rebuild-a-cloud-server)
-   [Resize standard
    servers](/howto/managing-your-server-resizing-standard-and-general-purpose-servers)
-   [Reset your server
    password](/howto/reset-your-server-password)
-   [Deleting your
    server](/howto/deleting-your-server)


