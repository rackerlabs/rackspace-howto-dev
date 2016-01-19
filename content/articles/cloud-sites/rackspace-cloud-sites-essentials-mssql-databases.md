---
node_id: 520
title: Rackspace Cloud Sites Essentials - MSSQL Databases
type: article
created_date: '2011-03-16'
created_by: Rackspace Support
last_modified_date: '2015-12-28'
last_modified_by: Kyle Laffoon
product: Cloud Sites
body_format: tinymce
---

**Note**: This article is written for our [Cloud Sites Control
Panel](https://manage.rackspacecloud.com/). You can get to it from the
Cloud Control Panel by clicking your name in the upper-right corner and
selecting [Cloud Sites Control
Panel](https://manage.rackspacecloud.com/).

### Previous section

[Getting Started with Cloud
Sites](/how-to/cloud-sites)



**In this article we are going to learn how to add a MSSQL database to
your website in Cloud Sites.** The process is fairly simple so let's
jump in and add our first database.

-   First, login to the [Rackspace Cloud Control
    Panel](http://manage.rackspacecloud.com)
-   Navigate to **Hosting-&gt;Cloud Sites**

    <img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/capture_1.png" width="179" height="287" />

<!-- -->

-   From the list of domains click on the **website for which a new
    MSSQL database needs to be added**.

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/capture_2.png" width="613" height="133" />

-   Click on the **Features** tab

    ![](http://c806394.r94.cf2.rackcdn.com/featurestab.png)

<!-- -->

-   In the **Databases** section click **Add** button

<!-- -->

-   Enter a **database name**
-   Choose a database type as SQL\_Server\_2008 and
    click **Continue**<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/capture_3.png" width="387" height="232" />



**NOTE:** *The prefix of the database name is generated for the user by
Cloud Sites. The database name is a combination of the prefix and the
identifier.*

-   Provide a database **user name**, a **password** and then
    click **Finish**

    <img src="http://c806394.r94.cf2.rackcdn.com/databaseuser.png" width="521" />

**NOTE:** *The prefix of the database user name is generated by Cloud
Sites. The database user name will be a combination of the prefix and
the identifier.*

-   A clock icon is displayed while the database completes setup, click
    on the **Features tab** to refresh status

    <img src="http://c806394.r94.cf2.rackcdn.com/pendingdatabase.png" width="285" />

<!-- -->

-   Confirm that the new database is active verifying that the status
    column has a **green check mark** icon next to the database
    name<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/capture_5.png" width="628" height="181" />



**NOTE:** T*his process can take a few moments to complete. If your
database does not have a green check mark next to it in excess of 10
minutes and you are still experiencing a problem, please do not hesitate
to contact our technical support 24x7 via phone, chat or by submitting a
ticket through your control panel.*



**Congratulations!** You have added a Microsoft SQL database to your
website! In the next article we will learn how to start working with the
new MSSQL database.



### Next section

[Cloud Sites
Technologies](/how-to/rackspace-cloud-sites-essentials-cloud-sites-technologies)
