---
node_id: 3572
title: Provisioning cloud resources when migrating from Amazon Web Services
type: article
created_date: '2013-07-02'
created_by: Rackspace Support
last_modified_date: '2016-01-19'
last_modified_by: Rose Contreras
product: Cloud Servers
product_url: cloud-servers
---

This article describes how to provision your Rackspace Cloud services when migrating from Amazon Web Services (AWS).

### Previous section
[High-level steps for migrating from Amazon Web Services](/how-to/high-level-steps-for-migrating-from-amazon-web-services)

Perform the following procedures to provision and configure your cloud instances:

### Provision a new cloud server

1. Log in to the [Rackspace Cloud Control Panel](https://mycloud.rackspace.com).

2. On the Cloud Servers page, click **Create Server**.

3. Name the server and select a region for it.

4. Select an OS that matches your OS from AWS.

    **Note:** If your Amazon Elastic Compute Cloud (EC2) instance is Amazon Linux, select CentOS 5.0 or later. Amazon Linux is based on Red Hat Enterprise Linux 5.

5. Select the size (flavor) that matches your EC2 instance (RAM and disk space), and click **Create Server**.

   For information about instance size mapping, see [Mapping of Amazon Web Services resources to Rackspace resources](/how-to/mapping-of-amazon-web-services-resources-to-rackspace-resources).

	**Note**: You can add more storage to your cloud server after it is created by adding a Cloud Block Storage volume. For instructions, see the Add Cloud Block Storage section later in this article.

6. When your root admin password is displayed, copy the password to a secure location, and then click **Dismiss Password**.

  **Note**: It is important that you copy and save your root admin password for future reference. You need this password to log in to your server. After you click **Dismiss Password**, the password will not be displayed again.

### Create a custom password (optional)

You can create a custom password for you server.

1. On the Cloud Servers page in the Cloud Control Panel, click the gear icon next to the server in the server list and select **Change Password**.

2. Enter a new password and click **Change Password**.

### Add a Cloud Block Storage (optional)

If you had additional Amazon Elastic Book Store (EBS) volumes attached to your server, or if you prefer to have more storage space for your server, add additional Cloud Block Storage volumes as follows:

1. In the Cloud Control Panel, open the server's detail page.

2. In the **Storage Volumes** section, click **Create Volume**.

3. Name the volume, select its type (SATA or SSD), and select the size.

4. Click **Create Volume**.

    <img alt="" height="349" src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/Step%201-3.png" width="543" />

### Create a Cloud Files container (optional)

If you plan to use a Cloud Files container for the application, to back up files, or to assist with your application migration, create your container now.

1. At the top of the Cloud Control Panel window, click **Storage**.

2. In the pop-up menu, under **Object Storage and CDN**, select **Files**.

3. On the **Cloud Files/Containers** page, click **Create Container**.

4. Name the container, assign it to the same region as the server that you created, and select the container type.

5. Click **Create Container**.

### Create a Cloud Databases instance (optional)

If you will not be setting up your own database server, create a Cloud Databases instance.

1. At the top of the Cloud Control Panel window, click **Databases**.

2. In the pop-up menu, select **Database Instances**.

3. On the Cloud Databases page, click **Create Instance**.

4. Name the instance and assign it to the same region as your server.

5. Select the type of database instance (datastore), and specify its size (in RAM and disk space).

6. *(Optional)* Add your first database by assigning it a name, user name, and password.

   **Note:** You cannot name your user as root.

7. Click **Create Instance**.

### Connect to the cloud server

1. On the Cloud Servers page in the control panel, click the name of your server.

2. Under **Networks**, note the <strong>PublicNet (Internet) IPv4</strong> address.

3. Using SSH, connect to your cloud server by using the following command and the PublicNet address:

        ssh root@<ipAddress>

    If you're connecting from a Windows computer, [use PuTTY](/how-to/connecting-to-linux-from-windows-by-using-putty) or a similar SSH command to connect to your server's IP address.

4. Enter your root password to log on.

### Next steps

After your Rackspace Cloud services are provisioned, you can build your applications and transfer your data from AWS. The following articles provide detailed descriptions of migration scenarios:

- Applications built on a LAMP stack - [Migrating an Application Built on a LAMP Stack from Amazon Web Services](/how-to/migrating-an-application-built-on-a-lamp-stack-from-amazon-web-services)

- .NET applications - [Migrating a .NET application from Amazon Web Services](/how-to/migrating-a-net-application-from-amazon-web-services)

- Java web applications [Migrating a Java Web Application from Amazon Web Services](/how-to/migrating-a-java-web-application-from-amazon-web-services)
