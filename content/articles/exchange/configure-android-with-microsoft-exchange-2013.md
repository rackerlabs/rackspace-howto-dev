---
node_id: 3883
title: Manually configure Android devices for email hosted on Exchange 2013
type: article
created_date: '2014-01-31 16:58:52'
created_by: mawutor.amesawu
last_modified_date: '2015-01-09 18:2550'
last_modified_by: jered.heeschen
products: Exchange
body_format: tinymce
---

The following steps are required to configure Microsoft Exchange 2013 on
most Android phones/tablets:

*Note: The administrator of your account will need to add ActiveSync to
your email throught their Administrative Control Panel*

1.  Tap on the system **Settings**.

    ![](/knowledge_center/sites/default/files/field/image/1.%20Settings_2.png)\
      

2.  Tap **Accounts and Sync** (**Accounts**on some devices).

    ![](/knowledge_center/sites/default/files/field/image/2.%20Accounts%20and%20Sync_2.png)

     

3.  Tap on **Add**.

    ![](/knowledge_center/sites/default/files/field/image/3.%20Add_2.png)\
      

4.  Select **Exchange ActiveSync **(**Microsoft Exchange ActiveSync** on
    some devices).

    ![](/knowledge_center/sites/default/files/field/image/4.%20Exchange%20ActiveSync_2.png)

5.  Fill in your email address and password and tap **Manual Setup**.

    ![](/knowledge_center/sites/default/files/field/image/5.%20Manual%20Setup_2.png)\
      

6.  On the next page, add in the rest of the necessary information:

    -   Email address: your email address ("**test@emailcompany.org**")
    -   Server Address: **mex06.emailsrvr.com**
    -   Domain: (**Leave this blank**)
    -   Username: your email address again.
    -   Some devices may have the settings as domain\\username. On those
        Devices the field should have a "**\\**" before your email
        address. (e.g "**\\test@emailcompany.org**")
    -   Select **This server requires an encrypted SSL connection**.

    With the information filled in, click **Next**. You may be prompted
    to Enable Remote Security Administration. Press **Ok** or **Allow**.
    This allows you to remotely perform a factory reset (Delete all
    data) on the device from OWA (Outlook Web App) in the event that the
    phone is lost or stolen and there is sensitive company information
    within the device.

    ![](/knowledge_center/sites/default/files/field/image/4_40.png)

7.  Next select the services you wish to sync with the Exchange server
    and when to sync. Tap **Next**.

    ![](/knowledge_center/sites/default/files/field/image/7.%20Sync%20Options_2.png)

8.  Give your account a descriptive name and tap **Finish Setup**.

    ![](/knowledge_center/sites/default/files/field/image/8.%20Finalize_1.png)

 

