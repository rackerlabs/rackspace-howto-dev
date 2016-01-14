---
node_id: 3848
title: Manually configure Outlook 2013 for email hosted on Exchange 2013
type: article
created_date: '2014-01-10 21:55:49'
created_by: mawutor.amesawu
last_modified_date: '2015-01-19 19:1819'
last_modified_by: jered.heeschen
product: Exchange
body_format: tinymce
---

Use the following steps to set up your Microsoft Exchange 2013 mailbox
with your Outlook 2013 email client.<br>
 <br>
 1. Click the Windows**Start**button, select **Control Panel**, and then
click **Mail** (32-bit).<br>
 <br>
 ![](/knowledge_center/sites/default/files/field/image/Step1_0.png)<br>
 <br>
 *Note: Depending on the version of Windows you're running, you might
need to switch to***Classic view to find the **Mail** entry or it might
be labeled **32-Bit***.*<br>
 <br>
 2. Click **Show Profiles**, click **Add**, enter a name for this
profile, and then select **OK**.<br>
 <br>
 3. On the Auto Account Setup page of the Add New Account wizard, select
**Manually configure server settings or additional server types**, and
then click **Next**.<br>
 <br>
 ![](/knowledge_center/sites/default/files/field/image/Step2_0.png)<br>
 <br>
 4. On the Choose Service page, select **Microsoft Exchange or
compatible service**, and then click **Nex****t**.<br>
 <br>
 ![](/knowledge_center/sites/default/files/field/image/Step3_0.png)<br>
 <br>
 5. On the Server Settings page, perform the following actions:<br>
      A. In the **Server** text box, type **outlook**.<br>
      B. Select the  the **Use Cached Exchange Mode** check box.<br>
      C. In the **User Name** text box, enter your entire email
address.<br>
      D. Click **More Settings**.<br>
 <br>
 *Note: Outlook 2013 offers the option to limit the amount of data that
is downloaded to your local machine.  This can be adjusted, using the
"Mail to keep offline slider."***You can select caching for 1 month, 3
months, 6 months, 1 year, 2 years, and &ldquo;all.&rdquo;*By default, Outlook 2013
only synchronizes twelve (12) months of email to your Offline Outlook
Data (.ost) file from the Exchange server. In this example, if you have
email items older than 12 months in your Exchange mailbox, they reside
only in your mailbox on the server.*<br>
 <br>
 ![](/knowledge_center/sites/default/files/field/image/Step4_0.png)<br>
 <br>
 6. In the Microsoft Exchange dialog box, click the **Connection** tab
and select the **Connect to Microsoft Exchange using HTTP**check box.
Then, click **Exchange Proxy Settings**.<br>
 <br>
 ![](/knowledge_center/sites/default/files/field/image/Step5_0.png)<br>
 <br>
 7. In the Microsoft Exchange Proxy Settings dialog box, perform the
following actions**:<br>
     **A. In the **Use this URL to connect to my proxy server for
Exchange** text box, enter **mex06.emailsrvr.com**.<br>
      B. Select both the **On fast networks** and **On slow networks**
check boxes.<br>
      C. Under **Proxy authentication settings**, select **Basic
Authentication**.<br>
      D. Click **OK**.<br>
 <br>
 ![](/knowledge_center/sites/default/files/field/image/Step6_0.png)<br>
 <br>
 8. In the Microsoft Exchange dialog box, click **Apply** and then click
**OK**.

9. On the Server Settings page, click **Check Name**, type your
password, and then click **OK**.

 

*Note: If you receive a pop-up message asking you to select your mailbox
from a list, select your mailbox and click OK.*

 

Your name will then be highlighted and a line will appear under the
**User Name**  field which indicates your profile has been configured.

 

*Note: The server name resolves to a unique string that is different
with every mailbox. Do not attempt to replicate this information with
other accounts.*

10. Click **Next**, and on the next page, click **Finish**.<br>
 <br>
 ![](/knowledge_center/sites/default/files/field/image/Step7_0.png)

![](/knowledge_center/sites/default/files/field/image/Step8_0.png)

11. Open Outlook to select your new Exchange profile.

