---
node_id: 673
title: Install and use mojoPortal
permalink: article/install-and-use-mojoportal
type: article
created_date: '2011-03-16 21:57:40'
created_by: RackKCAdmin
last_modified_date: '2015-12-30 16:5118'
last_modified_by: stephanie.fillmon
products: Cloud Sites
body_format: tinymce
---

**NOTE:** This article refers to the [Cloud Sites Control
Panel](https://manage.rackspacecloud.com/). You can access this
interface from the [Cloud Control Panel](https://mycloud.rackspace.com/)
by clicking your username in the upper-right corner of the control panel
and selecting Cloud Sites Control Panel.

**Prerequisites**

-   Administrative access to the Rackspace Cloud to create domains and
    add databases
-   Latest mojoPortal release version uncompressed in a local repository
-   Ftp access to website, and a ftp client like ExpanDrive

**Procedure**

-   Review the mojoPortal Installation reference
    [http://www.mojoportal.com/installation-quick-start.aspx](http://www.mojoportal.com/installation-quick-start.aspx "http://www.mojoportal.com/installation-quick-start.aspx")
-   Login to the [Cloud Sites Control
    Panel](http://manage.rackspacecloud.com/pages/Login.jsp| "http://manage.rackspacecloud.com/pages/Login.jsp|")
-   If you are new to Rackspace Cloud, please refer to [Adding a new
    website](http://www.rackspace.com/knowledge_center/article/getting-started-with-cloud-sites-how-to-add-a-new-website "Adding a new website")
-   Navigate the Hosting-\>Cloud Sites menu to the website hyperlink on
    which mojoPortal is to be installed.

NOTE: The domain must have .Net and Asp technology Feature enabled, and
database Feature selected. The database feature can be added by using
the CHANGE PLAN hyperlink on the domain **General Settings** tab.

-   Upload the uncompressed files from the local repository to the
    desired location on the website using FTP - Refer to [Upload content
    to a website using
    FTP](http://www.rackspace.com/knowledge_center/article/getting-started-with-cloud-sites-uploading-your-content "/knowledge_center/index.php/Uploading_content_to_a_website_using_FTP").
    (We will assume you are using the primary ftp user name for the
    account.)

-   Next create a new MSSQL database (Refer to \* [Add a MSSQL database
    to a website or
    domain](http://www.rackspace.com/knowledge_center/article/rackspace-cloud-sites-essentials-mysql-databases "/knowledge_center/index.php/Adding_a_MySQL_database_to_a_website_or_domain")).
-   Note the database information a) database name b) user name c)
    password d) hostname (not localhost) for use during the mojoPortal
    installation
-   With this, Cloud Sites specific steps are complete. We can get
    started with the installation of mojoPortal.

**NOTE**: Only applications that run under **Medium Trust** can function
on the Rackspace Cloud. This is for security reasons in a hosting
environment.

-   Copy the file Web.mediumtrust.config to file Web.config in the
    /web/content/ directory
-   Modify the Web.config file to add the Impersonate directive. Refer
    to [Add impersonation to your ASP.NET
    site](http://www.rackspace.com/knowledge_center/article/add-impersonation-to-your-aspnet-cloud-site "/knowledge_center/index.php/How_do_I_add_impersonation_to_my_ASP.NET_site%3F").
-   Copy the file user.config.sample to user.config in the /web/content/
    directory. Modify the connection string with MSSQL database
    information noted during the preparation phase. Example below.

<!-- -->

     <add key="MSSQLConnectionString" value="server=mssql0804.wc1\inst2;UID=3xxxx_mojo;PWD=XXXX;database=3xxxx_mojo" />

-   Verify that logging is turned on if needed. Refer to [Enable logging
    for a
    website](http://www.rackspace.com/knowledge_center/article/enabling-raw-logging-for-a-cloud-sites-website "/knowledge_center/index.php/Enabling_logging_for_a_website")
-   mojoPortal is fully functional and can be accessed with the domain
    URL. e.g. visit: http://asp.example.com
    -   If DNS is not setup for the domain, visit the Testing
        URL provided in the Classic Cloud Control Panel under the
        **General Settings** tab,
        e.g. http://asp.example.com.asp1-7.dfw1-1.websitetestlink.com

---**RKN** - 12/10/2009

