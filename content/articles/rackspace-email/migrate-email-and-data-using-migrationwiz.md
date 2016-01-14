---
node_id: 3349
title: Migrate your email by using the Self-Service tool
type: article
created_date: '2013-03-18 13:16:33'
created_by: mawutor.amesawu
last_modified_date: '2016-01-07 05:0441'
last_modified_by: constanze.kratel
product: Rackspace Email
body_format: tinymce
---

This article demonstrates how to use the Self-Service Migration Tool
provided in the Cloud Office Control Panel to copy email data from your
previous provider to Rackspace Email or Microsoft Exchange. The
Self-Service MIgration Tool uses our private-label version of
MigrationWiz, which you can run at any time at no additional cost.

**Note**: Some of the features that are present in the full version of
MigrationWiz (at migrationwiz.com) are not readily available within the
Self-Service Migration Tool. If you want to use the full version, see
[Accessing the Full Version of
MigrationWiz](http://www.rackspace.com/knowledge_center/article/accessing-the-full-version-of-migrationwiz).

Premigration steps
------------------

Before you begin your migration, you need to create your mailboxes on
the Rackspace environment. The migration tool does not create your
mailboxes for you.

Use the following resources to help you create your mailboxes:

-   Rackspace Email: [How to add Rackspace Email
    mailboxes](http://www.rackspace.com/knowledge_center/article/adding-rackspace-email-mailboxes)
-   Microsoft Exchange: [How to add Microsoft Exchange
    mailboxes](http://www.rackspace.com/knowledge_center/article/adding-microsoft-exchange-mailboxes-0)

You need the usernames and passwords for both your previous service and
the Rackspace environment. The migration tool requires that you enter
this information.<br>
  <br>
 To ensure that mail is routed properly to your new mailboxes, you must
update the MX records for your domain.  The following article provides
you with the appropriate DNS records:

[Set up DNS records for Cloud Office email and Skype for
Business](https://www.rackspace.com/knowledge_center/article/set-up-dns-records-for-cloud-office-email-and-skype-for-business)

To configure your email clients and mobile devices, you can use our
Email Setup Assistant: 

[http://emailhelp.rackspace.com](http://emailhelp.rackspace.com)

To migrate your email
---------------------

1.  Log in to your control panel.
2.  To create your self-service migration portal, click **Get Started
    with MigrationWiz Now.**

    ![](/knowledge_center/sites/default/files/field/image/self-service1.png)

    You are redirected to the MigrationWiz portal.

3.  Enter a contact email address in the **Email Address** box, agree to
    the Terms of Service (BitTitan is MigrationWiz), and then click
    **Login**.

    ![](/knowledge_center/sites/default/files/field/image/4-2_0.png)

    A notification informs you that an email with a secure link has been
    sent to your email address. Follow the instructions in the email to
    log in to the MigrationWiz portal.

4.  Locate your existing email service server information and determine
    what kind of service you have (POP, IMAP, or Exchange).
    -   IMAP: If you use Outlook, the incoming server address can be
        found under your account settings. It typically looks like
        **mail.domain.com** or **imap.domain.com**.
    -   Webmail: Your server address is a portion of the webmail URL.
        For example, if your webmail address is
        **https://webmail.domain.com**, then your server address is
        **webmail.domain.com**.
    -   Exchange: Your Outlook Web Access (OWA) address is the best way
        to connect. Check your mail via an Internet browser. It
        typically looks like **https://mail.domain.com/owa** or
        **https://mail.domain.com/exchange**.

5.  Click **Next**.
6.  Enter your source and destination server configuration settings. 

    1.  Select the source server system type and enter the server
        address. For IMAP, you must also enter a port number. IMAP ports
        are 993 (secure) and 143 (non-secure).
    2.  For the destination server, select the service that you are
        migrating to, Rackspace Email or Microsoft Exchange 2013, and
        then click **Next**.

    ![](/knowledge_center/sites/default/files/field/image/8-2_0.png)

7.  Enter the email address, username and password for the source and
    destination mailboxes. You can migrate multiple mailboxes by
    clicking the + symbol or by inputting your mailbox information into
    the spreadsheet provided. Then, click **Next**.

    ![](/knowledge_center/sites/default/files/field/image/9-2_0.png)

    The next step is a trial migration to ensure that connectivity is
    successful to both the source and destination mailboxes based on the
    information that you entered.

8.  Click **Next** to begin the trial migration.

    ![](/knowledge_center/sites/default/files/field/image/10-2_0.png)

9.  When the status changes to **Ready for migration**, click **Next**
    to proceed to the next screen.

    ![](/knowledge_center/sites/default/files/field/image/11-2_0.png)

10. Click **Next** to begin the migration of your email data. 

    ![](/knowledge_center/sites/default/files/field/image/13-2_0.png)

    Several factors influence how long your email will take to migrate.
    For a list of possible factors, see [Factors that affect the
    duration of email
    migrations](https://www.rackspace.com/knowledge_center/article/factors-that-affect-the-duration-of-email-migrations).

11. After your migration has completed, you can run the migration tool
    again by selecting **Migrate new items.**For more information about
    running additional migrations, see [Running additional passes with
    MigrationWiz](https://www.rackspace.com/knowledge_center/article/running-additional-passes-with-migrationwiz).
    Otherwise, clidk **Finish**.

    ![](/knowledge_center/sites/default/files/field/image/14-2_0.png)

12. You can find a list of all your projects under **My Migrations**,
    located in the top-right corner of your migration portal. To begin a
    new project, click **Start a new migration**.

    ![](/knowledge_center/sites/default/files/field/image/15-2_0.png)

 

