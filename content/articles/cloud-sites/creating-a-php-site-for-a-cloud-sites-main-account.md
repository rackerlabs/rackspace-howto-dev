---
node_id: 532
title: Creating a PHP Site for a Cloud Sites main account
type: article
created_date: '2011-03-16 21:57:40'
created_by: RackKCAdmin
last_modified_date: '2015-12-29 18:2536'
last_modified_by: stephanie.fillmon
products: Cloud Sites
body_format: tinymce
---

**NOTE:** This article refers to the [Cloud Sites Control
Panel](https://manage.rackspacecloud.com/). You can access this
interface from the [Cloud Control Panel](https://mycloud.rackspace.com/)
by clicking your username in the upper-right corner of the control panel
and selecting Cloud Sites Control Panel.

**Pre-reqs**

-   User has administration access to the website

**Procedure**

-   Login to the [Cloud Sites Control
    Panel](http://manage.rackspacecloud.com/pages/Login.jsp| "http://manage.rackspacecloud.com/pages/Login.jsp|")
-   If you are new to The Rackspace Cloud, please refer to [Adding a new
    website](http://www.rackspace.com/knowledge_center/article/getting-started-with-cloud-sites-how-to-add-a-new-website "/knowledge_center/index.php/Adding_a_new_website")
    and add the website.
-   Navigate to Hosting -\> Cloud Sites -\> This will list all the
    domains/websites owned by the account, now click on the php website
    hyperlink

![](/knowledge_center/sites/default/files/field/image/Screenshot_5_20_13_12_11_PM.png)

-   Verify that logging is turned on if needed. Refer to [Enable logging
    for a
    website](http://www.rackspace.com/knowledge_center/article/enabling-raw-logging-for-a-cloud-sites-website "/knowledge_center/index.php/Enabling_logging_for_a_website")
-   Upload a sample index.php file (like the one shown below) to the
    main directory for the website using FTP - Refer to [Upload content
    to a website using
    FTP](http://www.rackspace.com/knowledge_center/article/getting-started-with-cloud-sites-uploading-your-content "/knowledge_center/index.php/Uploading_content_to_a_website_using_FTP")

<!-- -->

     <html>

      <head>
       <title>Sample Page</title>
      </head>
      <body>
       <?php echo '<p>Hello World</p>'; ?> 
      </body>

     </html
     

-   Navigate to index.php using the Test URL if necessary. Refer to
    [Using a Staging
    URL](http://www.rackspace.com/knowledge_center/article/using-a-staging-url "/knowledge_center/index.php/Using_a_staging_URL").
    Ensure that is served by Cloud Sites.

 

