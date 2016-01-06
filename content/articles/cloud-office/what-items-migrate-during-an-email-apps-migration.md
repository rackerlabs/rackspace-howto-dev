---
node_id: 3776
title: Items migrated during an Cloud Office migration
permalink: article/what-items-migrate-during-an-email-apps-migration
type: article
created_date: '2013-11-13 22:56:13'
created_by: milton.prado
last_modified_date: '2014-10-23 15:4242'
last_modified_by: David Hendler
products: Cloud Office
body_format: tinymce
---

When migrating email to Rackspace Cloud Office, we utilize a tool called
MigrationWiz.  Depending on which email platform you choose to migrate
to, the items that are migrated by MigrationWiz may differ.  The
following table shows which items are automatically migrated by the
tool.  

Items that are migrated
-----------------------

![](/knowledge_center/sites/default/files/field/image/WhatWeMigrate%20copy.png)

 

Items that are not migrated
---------------------------

Due to system limitations, the following items will not be automatically
migrated in the migration process.  In order to migrate this data, they
will need to be manually created or brought over via an email client.  

-   Items that do not match folder types (i.e. calendar responses within
    a mail folder)
-   Custom items that do not inherit from the core system types
    (Examples: items which are not true emails, calendars, contacts,
    journals, mail, notes, or tasks)
-   Personal Distribution Lists
-   Bounce notifications such as Non-Delivery Report/Receipt (NDR) or 
-   Delivery Status Notification (DSN)
-   Calendar notifications such as invites, cancellations, etc.
-   Public folders
-   RSS feeds
-   Mailbox settings, permission settings, sharing settings, client
    settings (ex: default font)
-   Mailbox rules
-   From Exchange 2003: BCC recipients (also resource attendees for
    appointments)
-   Acceptance status for meeting participants (ex: accepted, declined,
    tentative)

MigrationWiz is a content migration solution and is unable to perform
any of the following:

-   Creation of Outlook profiles
-   Migration of client side settings
-   Provisioning of accounts
-   Active Directory related object creations or synchronization
-   NK2 files migration


