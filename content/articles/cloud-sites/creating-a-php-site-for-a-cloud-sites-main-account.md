---
node_id: 532
title: Creating a PHP Site for a Cloud Sites main account
type: article
created_date: '2011-03-16'
created_by: Rackspace Support
last_modified_date: '2015-12-29'
last_modified_by: Stephanie Fillmon
product: Cloud Sites
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

-   Login to the
    <a href="http://manage.rackspacecloud.com/pages/Login.jsp%7C" class="external text" title="http://manage.rackspacecloud.com/pages/Login.jsp|">Cloud Sites Control Panel</a>
-   If you are new to The Rackspace Cloud, please refer to
    <a href="/how-to/getting-started-with-cloud-sites-how-to-add-a-new-website" class="external text" title="/knowledge_center/index.php/Adding_a_new_website">Adding a new website</a>
    and add the website.
-   Navigate to Hosting -&gt; Cloud Sites -&gt; This will list all the
    domains/websites owned by the account, now click on the php website
    hyperlink

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/Screenshot_5_20_13_12_11_PM.png" width="509" height="285" />

-   Verify that logging is turned on if needed. Refer to
    <a href="/how-to/enabling-raw-logging-for-a-cloud-sites-website" class="external text" title="/knowledge_center/index.php/Enabling_logging_for_a_website">Enable logging for a website</a>
-   Upload a sample index.php file (like the one shown below) to the
    main directory for the website using FTP - Refer to
    <a href="/how-to/getting-started-with-cloud-sites-uploading-your-content" class="external text" title="/knowledge_center/index.php/Uploading_content_to_a_website_using_FTP">Upload content to a website using FTP</a>

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
    <a href="/how-to/using-a-staging-url" class="external text" title="/knowledge_center/index.php/Using_a_staging_URL">Using a Staging URL</a>.
    Ensure that is served by Cloud Sites.



