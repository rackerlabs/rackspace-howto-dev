---
node_id: 606
title: Create a domain or subdomain that points to a website not hosted on Cloud Sites
type: article
created_date: '2011-03-23 11:48:25'
created_by: RackKCAdmin
last_modified_date: '2015-06-23 16:3933'
last_modified_by: kelly.holcomb
product: Cloud Sites
body_format: tinymce
---

**Note:** This article refers to the [Cloud Sites Control
Panel](https://manage.rackspacecloud.com). You can access this interface
from the [Cloud Control Panel](https://mycloud.rackspace.com) by
clicking the **Cloud Control Panel** menu at the top of the window and
selecting **Cloud Sites**.

Follow these directions to point a domain or subdomain to a website that
is *not*hosted on Cloud Sites.

1.  Log in to the [Cloud Sites Control
    Panel](https://manage.rackspacecloud.com "https://manage.rackspacecloud.com").
2.  Create the new domain or subdomain under the correct account. If you
    have any questions about how to do this, see [Getting Started With
    Cloud Sites: How To Add A New Website](/knowledge_center/node/1132).
3.  After the domain or subdomain is set up in your account, add a PHP
    redirect to the **web/content** folder by using FTP. For information
    about how to do this, including using FTP, see [Getting Started With
    Cloud Sites, FTP/SSHFS/FTP Clients](/knowledge_center/node/580).
4.  Using a text editing program (like Notepad or Wordpad), create a
    file with the following PHP redirect on your computer. After
    `Location:`, enter the URL that you want to redirect the website to
    (for example, `http://www.yourdomain.com/`).

        <?
        header("Location: URL");
        exit;
        ?>

    Using the example link, the full script would look as follows:

        <?php
        header("Location: http://www.yourdomain.com/");
        ?>

5.  Save this file as **index.php**.
6.  Log in to your new subdomain's FTP server.
7.  Navigate to the **/www.yourdomain.com/web/content** directory.
8.  Upload the **index.php** into this folder.<br>
     The redirect should be fully functional.

