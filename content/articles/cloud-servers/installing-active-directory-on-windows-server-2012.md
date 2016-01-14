---
node_id: 3380
title: Installing Active Directory on Windows Server 2012
type: article
created_date: '2013-04-03 18:30:47'
created_by: Rackspace Support
last_modified_date: '2016-01-14 20:4833'
last_modified_by: stephanie.fillmon
product: Cloud Servers
body_format: tinymce
---

Description
-----------

This article will walk you through setting up the Active Directory Role
on a Windows Server 2012. This article is intended to be used for those
without an existing Active Directory Forest, it will not cover
configuring a server to act as a Domain Controller for an existing
Active Directory Forest. 

Content
-------

-   [Installing Active Directory](#install)
-   [Configuring Active Directory](#configure)

Installing Active Directory
---------------------------
1. Open the **Server Manager** from the task bar. 
2. From **Server Manager **Dashboard select **Add roles and features**.
This will launch the Roles and Features Wizard allowing for
modifications to be performed on the Windows Server 2012 instance.

![](/knowledge_center/sites/default/files/field/image/server_manage.png)
3. Select **Role-based or features-based** installation from the
Installation Type screen and click **Next**. 

*Note: Roles are the major feature sets of the server, such as IIS, and
features provide additional functionality for a given role.*

*![](/knowledge_center/sites/default/files/field/image/roles_based.png)*
4. The current server is selected by default. Click **Next** to proceed
to the Server Roles tab.

![](/knowledge_center/sites/default/files/field/image/server_selection_1.png)
5. From the Server Roles page place a check mark in the box next to
**Active Directory Domain Services.** A notice will appear explaining
additional roles services or features are also required to install
domain services, click **Add Features**.

*Note: There are other options including, Certificate services,
federation services, lightweight directory services and rights
management. Domain Services is the glue that holds this all together and
needs to be installed prior to these other services.*

*![](/knowledge_center/sites/default/files/field/image/add_features.png)*
6. Review and **select optional features** to install during the AD DS
installation by placing a check in the box next to any desired features;
Once done click **Next**.

![](/knowledge_center/sites/default/files/field/image/features_0.png)
7. Review the information on the **AD DS tab** and click **Next**.

![](/knowledge_center/sites/default/files/field/image/ad_ds.png)

8. Review the installation and click **Install**.

*Note: The installation progress will be displayed on the screen. Once
installed the AD DS role will be displayed on the 'Server Manager'
landing page.*

![](/knowledge_center/sites/default/files/field/image/ad_install.png)

 

Configuring Active Directory
----------------------------

Once the AD DS role is installed the server will need to be configured
for your domain.
1. If you have not done so already, **Open the Server Manager** from
the task bar. 
2. Open the Notifications Pane by selecting the **Notifications icon**
from the top of the Server Manager. From the notification regarding
configuring AD DS click **Promote this server to a domain controller**.

![](/knowledge_center/sites/default/files/field/image/promote.png)
3. From the Deployment Configuration tab select **Add a new forest**
from the radial options menu. Insert your root domain name into the
**Root domain name** field.

![](/knowledge_center/sites/default/files/field/image/new_forrest.png) 
4. Review and **select a Domain and Forest functional level**. Once
selected **fill in a DSRM password** in the provided password fields.
The DSRM password is used when booting the Domain Controller into
recovery mode.

*Note: The selection made here will have lasting effects to features and
server domain controller eligibility. For further information on
Domain/Forest functional levels see official Microsoft documentation.*

*![](/knowledge_center/sites/default/files/field/image/domain_forest.png)*
5. Review the warning on the DNS Options tab and select **Next**.

![](/knowledge_center/sites/default/files/field/image/dns_options.png)
6. Confirm or enter a NetBIOS name and click **Next**.

![](/knowledge_center/sites/default/files/field/image/netbios.png)
7. Configure the location of the SYSVOL, Log files, and Database
folders and click **Next**.

![](/knowledge_center/sites/default/files/field/image/paths.png)
8. Review the configuration options and click **Next**.

![](/knowledge_center/sites/default/files/field/image/review.png)
9. The system will check to ensure all necessary prerequistes are
installed on the system prior to moving forward. If the system passes
these checks you will proceed by clicking **Install**.

*Note: The server will automatically be rebooted once the installation
completes.*

![](/knowledge_center/sites/default/files/field/image/promote_ad.png)

After the server is done rebooting, reconnect via RDP. Congratulations
on successfully installing and configuring a Active Directory Domain
Services on Windows Server 2012.

