---
node_id: 3587
title: Migrating a .NET application from Amazon Web Services
type: article
created_date: '2013-07-02 17:59:15'
created_by: RackKCAdmin
last_modified_date: '2016-01-07 17:0330'
last_modified_by: rose.contreras
product: Cloud Servers
body_format: tinymce
---

This article describes the migration of a .NET web application from
Amazon Web Services (AWS) to Rackspace Cloud. It takes an estimated 30
minutes to complete, if you follow the instructions step by step.

### Previous section

[Provisioning cloud resources when migrating from Amazon Web
Services](http://www.rackspace.com/knowledge_center/article/provisioning-cloud-resources-when-migrating-from-amazon-web-services)

The topology of the application in this scenario is represented in the
following figure:

![](/knowledge_center/sites/default/files/field/image/4-2-1.png)

### Prerequisites

-   Microsoft Windows Server on AWS running a .NET web application on
    Internet Information Services (IIS) (Windows Server 2012 with IIS 8
    is used in this use case.)
-   Valid and enabled account on Rackspace Cloud

### Preparation

-   Identify the resources to migrate, including application and
    database resources.
-   If you have not already, [create a Cloud Server
    instance](/knowledge_center/article/provisioning-cloud-resources-to-migrate-from-amazon-web-services)
    and any supporting Rackspace Cloud services.

### Install software packages

1.  Install the Rackspace Cloud Files client as follows:
    1.  Connect to the AWS instance by using Remote Desktop Connection.\
         \
         ![](/knowledge_center/sites/default/files/field/image/4-2-6.png)\
          
    2.  After you are connected, install a client that you will use to
        back up data to Rackspace Cloud Files (for example,
        [Cyberduck](http://www.rackspace.com/knowledge_center/article/configuring-rackspace-cloud-files-with-cyberduck),
        available at [http://cyberduck.ch/](http://cyberduck.ch/)).\
         You can use any browser to download the client.
    3.  Create a connection to Rackspace Cloud Files by using your
        Rackspace account user name and API key.\
         You will use this connection to back up data during the
        migration steps.\
         \
         ![](/knowledge_center/sites/default/files/field/image/4-2-7.png)\
          

2.  Install IIS 8 by using the instructions located at
    [http://www.iis.net/learn/get-started/whats-new-in-iis-8/installing-iis-8-on-windows-server-2012](http://www.iis.net/learn/get-started/whats-new-in-iis-8/installing-iis-8-on-windows-server-2012)
    .

### Back up data from AWS to Rackspace Cloud Files

Using the client that you installed in the preceding section (for
example,
[Cyberduck](http://www.rackspace.com/knowledge_center/article/configuring-rackspace-cloud-files-with-cyberduck)),
upload the .NET project folder to the Rackspace Cloud Files container
that you created in the article [Provisioning cloud resources when
migrating from Amazon Web
Services](http://www.rackspace.com/knowledge_center/article/provisioning-cloud-resources-to-migrate-from-amazon-web-services).

### Restore data from Cloud Files to Cloud Servers

1.  Connect to your Rackspace Cloud Servers instance by using Remote
    Desktop Connection.
2.  Copy the .NET web application folder from the Cloud Files container
    to the cloud server at the following location:

        C:\inetpub\wwwroot

3.  Open IIS Manager, click **Add Website**, and enter details: site
    name, physical path, and host name.\
     \
     ![](/knowledge_center/sites/default/files/field/image/4-2-8.png)\
      
4.  After the website is created, stop the Default Web Site
    pre-installed application and start your web application.

### Test your application

Click on **Browse \*:80 (http)** to see the application in the browser.

### Next steps

[Post-migration considerations when migrating from Amazon Web
Services](http://www.rackspace.com/knowledge_center/article/post-migration-considerations-when-migrating-from-amazon-web-services)

For other migration scenarios, see the following articles:

-   [Migrating an application built on a LAMP stack from Amazon Web
    Services](https://www.rackspace.com/knowledge_center/article/migrating-an-application-built-on-a-lamp-stack-from-amazon-web-services)
-   [Migrating a Java web application from Amazon Web
    Services](https://www.rackspace.com/knowledge_center/article/migrating-a-java-web-application-from-amazon-web-services)
-   [Migrating an application based on Backbone.js, Node.js, and MongoDB
    from Amazon Web
    Services](https://www.rackspace.com/knowledge_center/article/migrating-an-application-based-on-backbonejs-nodejs-and-mongodb-from-amazon-web-services)


