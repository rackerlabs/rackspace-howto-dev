---
node_id: 148
title: Uploading Content to a Cloud Files Container Using Fire Uploader
permalink: article/uploading-content-to-a-cloud-files-container-using-fire-uploader
type: article
created_date: '2011-03-15 23:23:46'
created_by: RackKCAdmin
last_modified_date: '2015-09-04 19:3041'
last_modified_by: kyle.laffoon
products: Cloud Files
body_format: tinymce
---

**NOTE:** This article is written for our [Cloud Sites Control
Panel](https://manage.rackspacecloud.com "https://manage.rackspacecloud.com/pages/Login.jsp").
Access this interface from the [Cloud Control
Panel](https://mycloud.rackspace.com) by clicking your Rackspace Cloud
account username in the upper-right corner of the control panel and
selecting Cloud Sites Control Panel.

The File Manager interface to Cloud Files is available through the Cloud
Sites Control Panel, but you can choose to use one of several
third-party interfaces that work just as well for managing your Cloud
Files content. FireUploader, a free add-on for Mozilla Firefox browsers,
is one such application.

The steps in this article describe the procedure for using FireUploader
to manage your Cloud Files content.

Prerequisites
-------------

-   Latest version of Firefox browser
-   Administrative access to the [Cloud Sites Control
    Panel](https://manage.rackspacecloud.com/pages/Login.jsp)

To upload content by using FireUploader
---------------------------------------

1.  Open the [Fire
    Uploader](http://www.fireuploader.com/DownloadPage.aspx "http://www.fireuploader.com/DownloadPage.aspx")
    website in FireFox.

2.  Click **Download** and follow the prompts to install Fire Uploader.

3.  Log in to the [Cloud Sites Control
    Panel](https://manage.rackspacecloud.com/pages/Login.jsp "https://manage.rackspacecloud.com/pages/Login.jsp")
    and select **Account Setting** and **Show** to view your API key.

4.  Make note of your username and API key. You will need them to set up
    FireUpLoader

5.  In your FireFox browser window, click **Tools**, then
    **FireUploader**.

6.  Select **Mosso a.k.a. The Rackspace Cloud**.

7.  Click **Manage Accounts** and enter the username and the API Key in
    the appropriate fields.

    **NOTE:**Do not use your `manage.rackspace.com` password. It will
    not work with Fire Uploader.****

8.  Toggle **Save password** the setting of your choice, then click
    **Add** and then **OK**.

9.  Create a container or folder by selecting **create directory** and
    name the container and click **OK**.
10. Double-click the newly created container

    .

11. You can now drag and drop video and image files into the new
    container.

12. Wait for the content to upload.

13. Navigate to **Hosting -\> Cloud Files** in the Classic Cloud Control
    Panel.

14. Select the new container and, in the bottom pane, select **Publish
    to CDN**.

15. Copy the CDN URL for later use.



