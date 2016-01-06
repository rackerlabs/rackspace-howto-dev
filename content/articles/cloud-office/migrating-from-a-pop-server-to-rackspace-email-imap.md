---
node_id: 3789
title: Migrating from a POP server to Rackspace Email IMAP using Outlook 2010 - Drag and Drop Method
permalink: article/migrating-from-a-pop-server-to-rackspace-email-imap
type: article
created_date: '2013-11-19 14:33:05'
created_by: milton.prado
last_modified_date: '2013-11-29 19:0157'
last_modified_by: jered.heeschen
products: Cloud Office
body_format: tinymce
---

POP email is typically stored locally on a computer and removed from the
mail server after being downloaded by the client.  In many cases, this
data cannot be migrated with our migration tool when it does not exist
on your source mail server.  The steps in this article will walk you
through performing a manual migration of POP data via Outlook to a
Rackspace Email account via IMAP.

We'll accomplish this task by adding your new Rackspace Email IMAP
account to the same profile that your POP account is on. This change
will allow you to easily move all of the locally stored email to your
new Rackspace Email account.

If you would like to learn more about the differences between POP and
IMAP, please see the help topic, [IMAP vs.
POP](http://www.rackspace.com/knowledge_center/article/rackspace-email-imap-vs-pop).

### Prerequisites

Before performing the steps below, make sure that mailboxes have already
been created on the Rackspace environment and that the MX records have
been updated so that email is routing correctly to Rackspace.

-   [How to create
    mailboxes](http://www.rackspace.com/knowledge_center/article/adding-rackspace-email-mailboxes)
-   [How to change MX
    records](http://www.rackspace.com/knowledge_center/article/updating-your-mx-records-microsoft-exchange)

### Changing Settings

For increased security, we recommend that you use our secure (SSL)
servers, as detailed below. If your internal system configurations
require non-SSL ports, those settings are available in the article
referenced previously,  [IMAP vs.
POP](http://www.rackspace.com/knowledge_center/article/rackspace-email-imap-vs-pop).

1.  In Outlook 2010 select **File** \> **Account Settings**.

2.  To add your IMAP account, click the **New** button.

3.  Enter your name and email address, IMAP for the Account Type,
    "secure.emailsrvr.com" for the Incoming and Outgoing mail servers,
    and your User Name and Password.

    ![](/knowledge_center/sites/default/files/field/image/settings_screenIMAP%20copy_0.jpg)

4.  Check th  **Remember Password** box if you don't want to type your
    password each time you launch Outlook.

5.  Click the **More Settings** button.

6.  Click on the **Outgoing Server** tab.

7.  Check the **My Outgoing Server (SMTP) Requires Authentication** box.

8.  Leave the default setting - **Use Same Settings as My Incoming Mail
    Server**.

9.  Select the **Advanced** tab.

10. Set the Incoming port to 993 and the Outgoing port to
    465, and **Enable SSL Encryption**.

    ![](/knowledge_center/sites/default/files/field/image/portsimap%20copy.jpg)

11. Once the settings have been updated, navigate to your Inbox and note
    that your new IMAP account is listed in the left-hand folder pane.
     Click on the account to expand the folders.  You should see mail
    items for that account start to appear.

    ![](/knowledge_center/sites/default/files/field/image/IMAPaccount.png)

12. Now that you have added your Rackspace account via IMAP, you can
    drag and drop emails from your POP Inbox to your IMAP Inbox.  As
    items start moving over, those emails will automatically upload to
    our server and will be visible across all of your devices that
    connect via IMAP to that account.

    **NOTE:** Depending on the number of emails in your POP account,
    this process can take a while.  You may also consider moving emails
    over in batches by selecting groups of email messages.  Once you've
    confirmed that all emails have moved to the new account, you may
    remove the configuration for the POP account as it will no longer be
    needed.

After the change, your email will look similar to the screenshot below.

![](/knowledge_center/sites/default/files/field/image/2013-11-27_1204.png)

