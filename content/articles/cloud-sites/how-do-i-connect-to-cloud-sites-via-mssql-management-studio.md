---
node_id: 602
title: Connect to Cloud Sites via SQL Server Management Studio Express
type: article
created_date: '2011-03-23 11:43:22'
created_by: RackKCAdmin
last_modified_date: '2015-12-29 19:1803'
last_modified_by: stephanie.fillmon
product: Cloud Sites
body_format: tinymce
---

**Note:** This article refers to the [Cloud Sites Control
Panel](https://manage.rackspacecloud.com/). You can access this
interface from the [Cloud Control Panel](https://mycloud.rackspace.com/)
by clicking the **Cloud Control Panel** menu at the top of the window
and selecting **Cloud Sites**.

Microsoft SQL Server Management Studio Express provides a graphical
management tool for SQL Server. You can use SQL Server Management Studio
Express to remotely connect to your Cloud Sites database.

**Note:** Only the primary database owner can make remote connections to
the database. This means that the original user added to the database is
the only one who is allowed to connect via SQL Server Management Studio
Express. Any secondary users who have been added who need to make
changes must use
[myLittleAdmin](http://www.rackspace.com/knowledge_center/article/rackspace-cloud-sites-essentials-mylittleadmin-database-management-interface "Working with a MSSQL database")
to connect.

-   [Prerequisite](#prereq)
-   [Get started](#get_started)
-   [Connect by using the external IP address](#connect)

Prerequisite {#prereq}
------------

Ensure that you have installed the latest version of SQL Server
Management Studio Express and any available service packs. As of the
last update of this article, SQL Server 2008 Management Studio Express
was available at
[http://www.microsoft.com/downloads/details.aspx?familyid=08e52ac2-1d62-45f6-9a4a-4b76a8564a2b](http://www.microsoft.com/downloads/details.aspx?familyid=08e52ac2-1d62-45f6-9a4a-4b76a8564a2b "http://www.microsoft.com/downloads/details.aspx?familyid=08e52ac2-1d62-45f6-9a4a-4b76a8564a2b").

Get started {#get_started}
-----------

To make an external connection, you need the external IP address for
your database. You can get the IP address by following these steps:

1.  Log in to [the Cloud Sites Control
    Panel](https://manage.rackspacecloud.com "https://manage.rackspacecloud.com").
2.  In the left navigation pane, click **Hosting** **\> Cloud Sites**.
3.  Click the domain name under which the database exists.
4.  Click the **Features** tab.
5.  Click the database name that you want to connect to.

The IP address is listed as the **Database Management IP Address**. You
need this address in the next section.

Connect by using the external IP address {#connect}
----------------------------------------

1.  Open Microsoft SQL Server Management Studio Express.<br>
     If the connection dialog box does not open, click the **File** menu
    and then select **Connect Object Explorer**.
2.  From the **Server type** menu, select **Database Engine**.
3.  In the **Server Name** box, enter the external IP address for your
    database.
4.  From the **Authentication** menu, select **SQL Server
    Authentication**.
5.  In the **Login**box, enter the primary user name for the database.<br>
     The user name must be prefixed by an account ID, so you must use
    the full user name; for example, **123456\_user** and not just
    **user***.*
6.  Enter that user's corresponding password.
7.  Enter the port number. To successfully connect, you must use port
    **4120**.
8.  To ensure that your queries run properly, click the **Connection
    Properties** tab at the top of the dialog box.<br>
     If you cannot see the **Connection Properties** tab, click the
    **Options** button at the bottom right of the dialog box.
9.  On the **Connection Properties** tab, enter your database name in
    the **Connect to database** box.
10. Click the **Connect** button.

