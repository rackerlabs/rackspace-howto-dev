---
node_id: 5026
title: Cloud Databases - FAQ
type: article
created_date: '2015-12-10'
created_by: Rackspace Support
last_modified_date: '2016-01-19'
last_modified_by: Stephanie Fillmon
product: Cloud Databases
body_format: markdown_w_tinymce
---

<h2>- Getting Started -</h2>

<h3>Can I provision Cloud Databases if I don't have Cloud Servers, Cloud Load Balancers, or Cloud Sites on my account?</h3>

<p>Yes, but instances are provisioned only with network interfaces on their data center's internal service network (ServiceNet). Connecting to a Cloud Database instance remotely requires either a Cloud Server or Cloud Load Balancer to <a href="https://www.rackspace.com/knowledge_center/article/connecting-to-your-cloud-database" target="_blank">proxy the connection</a>.</p>

<h3>What kind of storage solution does Cloud Databases offer?</h3>

<p>Each Cloud Database instance comes with an attached storage volume. Storage volumes are automatically provisioned on a shared Internet Small Computer System Interface (iSCSI) storage area network (SAN) that provides for increased performance, scalability, availability, and manageability. Applications with high I/O demands are performance-optimized and data is protected through both local and network RAID-10. Additionally, network RAID provides synchronous replication of volumes with automatic failover and load balancing across available storage clusters.</p>

<h3>How is performance better than running a MySQL database on a Cloud Server?</h3>

<p>Every Cloud Databases instance is optimized for performance. Cloud Databases uses container-based virtualization, which eliminates the performance bottlenecks of the traditional hardware virtualization and enables your database to run at near bare metal speeds. It also uses dedicated SAN storage and high speed networking to give you faster access to your data.</p>

<h3>What is Cloud Databases?</h3>

<p>Cloud Databases is a stand-alone, API-based, relational database service built on OpenStack® cloud that allows Rackspace customers to easily provision and manage multiple MySQL database instances. Instances are provisioned in a single-tenant, container-based environment per account and are accessible via the Rackspace internal ServiceNet network. Each database instance is optimized for performance. You can run a database instance with MySQL, Percona, or MariaDB as the database technology.</p>

<h3>What are the benefits of using Cloud Databases?</h3>

<p>Cloud Databases provides a complete solution for customers demanding a high-performance, purpose-built infrastructure designed for relational databases backed and supported by engineers who specialize in MySQL workloads. Cloud Databases is a fully managed service for customers who want to focus on developing their applications and not worry about the underlying infrastructure. The service offers on demand backups and restores, integrated monitoring, redundant storage, scalability to grow based on your application needs, and full control of your database.</p>

<h3>What instance sizes do you currently support?</h3>

<p>For the most up-to-date information about available instance sizes, see the <a href="http://www.rackspace.com/cloud/databases/">Cloud Databases website</a> or the "<a href="https://developer.rackspace.com/docs/cloud-databases/v1/developer-guide/#listing-flavors">Listing flavors</a>" section of the Cloud Databases Developer Guide.</p>

<h3>What types of Rackspace products / accounts can use Cloud Databases?</h3>

<p>Any US or UK customer with a Cloud account will be able to provision multiple ServiceNet database instances, manage multiple databases and users (within resource limits). This service is also available to RackConnected Cloud Servers. Both First and Open Cloud Servers can connect to Cloud Databases, as well as any product with access to our internal ServiceNet network within the same regional datacenter.</p>

<h3>Can Cloud Databases be used with Dedicated servers?</h3>

<p>No, Cloud Databases are available only to customers with Cloud account credentials. Managed Operations Service Level or Dedicated customers with RackConnect (that is those customers who also have a Cloud account) have access, but can use the service only with their Rackspace Cloud product resources.</p>

<h3>Is Cloud Databases available in the Control Panel?</h3>

<p>Yes. Click <strong>Databases </strong>in the <a href="http://mycloud.rackspace.com/">Cloud Control Panel</a>. Connecting to a Cloud Database instance remotely requires either a Cloud Server or Cloud Load Balancer to <a href="https://www.rackspace.com/knowledge_center/article/connecting-to-your-cloud-database">proxy the connection</a>.</p>

---------
<h2>Account Services</h2>

<h3>Does Cloud Databases support SSL for communication between my application and my database instance?</h3>

<p>Yes, Cloud Databases supports connecting to your instance using SSL. An SSL certificate is installed for each Cloud Databases instance that enables a secure connection between your application and the instance. When an SSL connection is established, any data transfer between the instance and application is encrypted.</p>

---------
<h2>Backups</h2>

<h3>Can I write to my database instance during a backup?</h3>

<p>The behavior of your instance during a backup depends on the storage engine that you are using for tables. If you use only InnoDB, write access to your database instance is not suspended. Conversely, if you have MyISAM tables, those databases are write-locked during the backup process.</p>

<h3>What storage engines do you support for database backups?</h3>

<p>MySQL supports several types of table engines, also known as <em>table types</em>. The tables on a Cloud Databases instance can use a mix of different table engine types or they can all use the same type. Currently we support backups of databases that use InnoDB and MyISAM.</p>

<h3>How much do you charge for database backups?</h3>

<p>Backups are stored in your Cloud Files account, and you are charged for storage used. Standard rates for Cloud Files storage apply. For current costs, see the <a href="http://www.rackspace.com/cloud/files/pricing/">Cloud Files pricing page</a>.</p>

<h3>How do you perform database backups?</h3>

<p>Backups are created by using Percona XtraBackup to perform a hot copy of all databases on an instance. The resulting database files are streamed directly to your Cloud Files account for storage.</p>

<h3>Do you provide database backup and restore features?</h3>

<p>Manual backup and restore operations are currently supported from within the Control Panel. For more information, please read the article <a href="https://www.rackspace.com/knowledge_center/article/managing-backups-for-cloud-databases"> Managing Backups for Cloud Databases</a>. Alternately you can manage backup operations<a href="https://developer.rackspace.com/docs/cloud-databases/v1/developer-guide/#document-api-operations/backups">via the Cloud Databases API</a>, or by using the <a href="https://developer.rackspace.com/docs/cloud-databases/v1/developer-guide/#install-the-trove-client">Trove command line tool (CLI)</a>.</p>

<p>Although Cloud Databases provides built-in data replication, as a best practice, we encourage our Cloud customers to back up their data using MySQL tools like mysqldump. Managed Operations Service Level customers can request assistance with backups from their support team.</p>

<h3>How long does a database backup take?</h3>

<p>The duration of the backup will depend on the size of your databases and any network saturation during the backup.</p>

<h3>How do I restore a database backup?</h3>

<p>To restore a database backup, you must create a new database instance, specifying the backup that you want to restore during the create request. Your backup is loaded to the new instance, and you will receive a DNS endpoint for the new instance. After the restore operation is complete, you can update your application to use the new endpoint.</p>

<p>The original instance is not altered during a restore operation and may remain in use or be deleted through the API, CLI, or Control Panel.</p>

<h3>How many database backups can I request?</h3>

<p>There are no limits on how many database backups you can create. Note that you can run only one backup at a time; duplicate requests result in a 422 error.</p>

<h3>When a Cloud Database is deleted how is the data removed?</h3>

<p>Cloud databases run off of SAN storage using a mount point. Once an instance is deleted, the mount point is destroyed.</p>

<h3>Are database backups deleted when a database is deleted?</h3>

<p>Backups are not deleted when an instance is deleted. You must manually remove any stored backups.</p>

---------
<h2>Monitoring and Troubleshooting</h2>

<h3>What Cloud Databases operations are supported at different service levels?</h3>

<p>Support coverage information for Managed Infrastructure and Managed Operations Service Level is available on <a href="http://www.rackspace.com/cloud/databases/support/">the Cloud Databases support matrix page</a>.</p>

<h3>Where can I find the Cloud SLA?</h3>

<p>The <a href="http://www.rackspace.com/information/legal/cloud/sla">Cloud service level agreement (SLA)</a> on the Rackspace website.</p>

<h3>How can I monitor my resource use on Cloud Databases?</h3>

<p>Monitoring is available for all Cloud Databases instances through pre-configured Cloud Monitoring checks, including load average, CPU, memory, disk storage, network, and a number of MySQL metrics. You can monitor your Cloud Databases instances using the<a href="https://www.rackspace.com/knowledge_center/article/monitoring-cloud-databases-with-the-cloud-control-panel">Cloud Control Panel</a>, the<a href="https://developer.rackspace.com/docs/cloud-monitoring/v1/developer-guide/">Cloud Monitoring API</a>, or the <a href="https://www.rackspace.com/knowledge_center/article/getting-started-with-rackspace-monitoring-cli">Cloud Monitoring command-line tool</a>.</p>

<p>You can also set up alarms to send you email alerts based on thresholds you define. An alert for disk space is set up by default for every instance. You can also use our <a href="https://intelligence.rackspace.com/">Cloud Intelligence beta site</a> to observe usage patterns or any unexpected changes in your environment.</p>

<h3>Can I create a Cloud Databases support ticket?</h3>

<p>Yes. A Cloud Databases support ticket category is available in the <a href="https://mycloud.rackspace.com/">Cloud Control Panel</a>.</p>

---------
<h2>Databases</h2>

<h3>What are the differences between InnoDB and MyISAM?</h3>

<p>InnoDB is the default storage engine for Cloud Databases. InnoDB enforces ACID transactions allowing for commit, rollback, and crash recovery capabilities to protect user data.</p>

<p>During a backup, a hot copy process is used on all tables. InnoDB tables record all transactions during the copy in order to replay them during a restore operation.</p>

<p>MyISAM tables are write-locked during the copy process in order to create a consistent backup. While the instance is being backed up you cannot add or delete databases, add or delete users, or delete, stop, or reboot the instance.</p>

<p>For more information about these engine types, see the MySQL documentation:</p>

<ul>
	<li><a href="http://dev.mysql.com/doc/refman/5.1/en/innodb-storage-engine.html" target="_blank">InnoDB Storage Engine documentation</a></li>
	<li><a href="http://dev.mysql.com/doc/refman/5.1/en/myisam-storage-engine.html" target="_blank">MyISAM Storage Engine documentation</a></li>
</ul>

<h3>How many connections does each database instance size support?</h3>

<p>Details about maximum connections and access to my.cnf file settings per database size are listed in the following table:</p>

<table>
  <tr>
    <th>Size</th>
    <th>Max connections</th>
    <th>Max user connections</th>
  </tr>
  <tr>
    <td>512 MB</td>
    <td>50</td>
    <td>40</td>
  </tr>
  <tr>
    <td>1 GB</td>
    <td>110</td>
    <td>100</td>
  </tr>
  <tr>
    <td>2 GB</td>
    <td>210</td>
    <td>200</td>
  </tr>
  <tr>
    <td>4 GB</td>
    <td>410</td>
    <td>400</td>
  </tr>
  <tr>
    <td>8 GB</td>
    <td>810</td>
    <td>800</td>
  </tr>
  <tr>
    <td>16 GB</td>
    <td>1610</td>
    <td>1600</td>
  </tr>
  <tr>
    <td>32 GB</td>
    <td>3210</td>
    <td>3200</td>
  </tr>
  <tr>
    <td>64 GB</td>
    <td>6410</td>
    <td>6400</td>
  </tr>
</table>

<h3>What is the maximum scalable capacity of a Cloud Database instance?</h3>

<p>Instances can be provisioned with up to 64GB of memory and up to 500GB of disk storage. You can increase storage up to the maximum using the <a href="https://mycloud.rackspace.com/">Cloud Control Panel</a>. Note that disk storage cannot be decreased on a running instance.</p>

<h3>Can I set up a read-only MySQL user in Cloud Databases?</h3>

<p>Yes, but by default all users created through the Control Panel, API, and command line interface (CLI) have full permissions.</p>

<p>To create read-only users, you first must enable the root user and use that user to generate and manage additional users with read-only privileges.</p>

<h3>Can I enable a root (super) user?</h3>

<p>Yes. Currently, the root user can only be enabled via the public API or command line interface (CLI). We do plan to integrate this feature into the Cloud Control Panel at a later date.</p>

<p>Once root is enabled, it cannot be disabled.</p>

<h3>What versions of MySQL do you offer?</h3>

<p>Cloud Databases supports MySQL 5.6, Percona 5.6 and MariaDB 10. For all newly created Cloud Database instances, MySQL 5.6 is the default. We will continue to support MySQL 5.1 for legacy instances, but we recommend our customers use the latest version of MySQL, Percona, or MariaDB because they offer significant performance improvements and newer features. For more information to help you choose the right database version for your application, see <a href="https://www.rackspace.com/knowledge_center/article/choosing-the-right-data-store">Choosing the right data store</a>.</p>

<h3>What bandwidth limitations are enforced on the ServiceNet network?</h3>

<p>The following table shows bandwidth, in megabits per second (Mbps), based on instance size.</p>

<table>
  <tr>
    <th>Instance Size</th>
    <th>Bandwidth</th>
  </tr>
  <tr>
    <td>512 MB</td>
    <td>20 Mbps</td>
  </tr>
  <tr>
    <td>1 GB</td>
    <td>100 Mbps</td>
  </tr>
  <tr>
    <td>2 GB</td>
    <td>200 Mbps</td>
  </tr>
  <tr>
    <td>4 GB</td>
    <td>300 Mbps</td>
  </tr>
  <tr>
    <td>8 GB</td>
    <td>400 Mbps</td>
  </tr>
  <tr>
    <td>16 GB</td>
    <td>500 Mbps</td>
  </tr>
  <tr>
    <td>32 GB</td>
    <td>1000 Mbps</td>
  </tr>
  <tr>
    <td>64 GB</td>
    <td>2000 Mbps</td>
  </tr>
</table>

<h3>Where can I find the Cloud Databases documentation?</h3>

<p>Release notes, API documentation, and a getting started guide for Cloud Databases are all available on the Rackspace <a href="http://docs.rackspace.com/api/">API Documentation site</a>.</p>

<h3>Are there API or account limits for my Cloud Database instances?</h3>

<p>Yes. All accounts, by default, have a preconfigured set of thresholds (or limits) to manage capacity and prevent abuse of the system. The system recognizes two kinds of limits: rate limits and absolute limits. Rate limits are thresholds that are reset after a certain amount of time passes. Absolute limits are fixed at the account level. For the most up-to-date information about rate and absolute limits (which include instance and volume limits), see the Limits section in the <a href="https://developer.rackspace.com/docs/cloud-databases/v1/developer-guide/#document-general-api-info/limits">Rackspace Cloud Databases Developer Guide</a>.</p>

<h3>If my database instance is unavailable, what happens to my data?</h3>

<p>If you cannot access your Cloud Databases instance, your data is still protected on a redundant SAN.</p>

<h3>How can I access my database instance?</h3>

<p>Cloud Databases provides several options for connecting to your database, giving you complete flexibility in how you access your database. For increased security, your database is available only on the Rackspace private network by default. However, you can connect to your database by using several methods described at the following links:</p>

<p><a href="https://www.rackspace.com/knowledge_center/article/public-and-private-access-for-cloud-databases">Public and private access for Cloud Databases</a></p>

<p><a href="https://www.rackspace.com/knowledge_center/article/connect-to-a-cloud-databases-instance">Connect to a Cloud Databases instance</a></p>

<p>Additionally, you can use the Cloud Control Panel, API, or command line interface (CLI) to manage your database instance. Some of the features are not available in the Control Panel but can be accessed through API or through the CLI. More information about the API and CLI is located in the <a href="https://developer.rackspace.com/docs/cloud-databases/v1/developer-guide/">Cloud Databases API documentation</a>, in both the API developers guide and the getting started guide.</p>

<h3>How do I set the default time zone for MySQL?</h3>

<p>You can set the default time zone for a Cloud Databases instance of MySQL by creating a configuration group that sets the default_time_zone parameter to the offset from UTC (for example, "-6:00" for CST).</p>

<p>For more information, see <a href="https://www.rackspace.com/knowledge_center/article/setting-the-time-zone-for-a-cloud-databases-instance"> Setting the time zone for a Cloud Databases instance</a>.</p>

<h3>Do you support importing and exporting data into the database?</h3>

<p>You can use standard MySQL client tools to import data into and export data from your instance. Knowledge Center articles that detail the processes of&nbsp;<a href="https://www.rackspace.com/knowledge_center/article/importing-data-to-cloud-databases">importing</a> or <a href="/how-to/exporting-data-from-mysql">exporting</a> data are available.</p>

<h3>Do you support MySQL configuration (my.cnf) file modifications?</h3>

<p>Yes. Configuration settings for Cloud Databases instances can be stored and applied using the<a href="https://mycloud.rackspace.com/">Cloud Control Panel</a> and the <a href="https://developer.rackspace.com/docs/cloud-databases/v1/developer-guide/">Cloud Databases API</a>. You can save your settings in configuration groups, and each configuration group can be applied to multiple instances. You can maintain multiple configuration groups to account for different workloads.</p>

<h3>What level of access do I have to my database instance?</h3>

<p>Access to MySQL is allowed only over port 3306; shell-level access is not available. Full MySQL access can be obtained by enabling the root user on the database instance.</p>

<h3>What is the default database storage engine?</h3>

<p>The default storage engine is InnoDB, but other storage engines included with MySQL 5.1, such as MyISAM, also work for certain use cases.</p>

---------
<h2>High Availability</h2>

<h3>What is High Availability for Cloud Databases?</h3>

<p>A Cloud Databases High Availability (HA) instance group includes a source database instance with one or two replicas. If the source database instance becomes unavailable, an automatic failover is initiated to one of the replicas. The automatic failover and promotion of the new instance is completed within a short downtime (approximately 10-30 seconds).</p>

<h3>What flavors are supported for HA instance groups?</h3>

<p>You can choose any flavor from 1 GB to 64 GB for provisioning an HA instance group.</p>

<h3>Can I create a backup of the High Availability instances?</h3>

<p>Currently backups, resizes, and custom configurations cannot be performed for instances that are part of the HA setup. Backups and incremental backups can be created for the HA group rather than an individual instance.</p>

<h3>Can I resize the RAM for my HA instances?</h3>

<p>Resizing is not currently supported for HA instances for Cloud Databases. Rackspace will start supporting resizing for HA instances in a future release.</p>

<h3>What is the underlying technology for creating HA Cloud Databases instances?</h3>

<p>Technical architecture details are provided in the <a href="https://www.rackspace.com/knowledge_center/article/high-availability-for-cloud-databases">High Availability for Cloud Databases</a> article.</p>

<h3>Do HA instances support automatic failover?</h3>

<p>Yes. Rackspace ensures that if the source database instance becomes unavailable, an automatic failover is initiated to the replicas within 10-30 seconds of downtime.</p>

<h3>What is the pricing for HA instances for Cloud Databases?</h3>

<p>For the product introduction, Rackspace is charging the same price for HA instances as for single instances for a limited time. In the future, there will be an increase in the price of HA instances.</p>

<h3>Which databases are supported for HA instances for Cloud Databases?</h3>

<p>Rackspace currently supports MySQL 5.6, Percona 5.6, and MariaDB 10 for HA database instances.</p>

<h3>How many replicas can I add to the HA group?</h3>

<p>You can add a maximum of two replicas to the primary source database instance. So you can have a maximum of three instances in the HA group, one primary and two replicas. In the future, we will increase the number of replicas that can be added to the HA group.</p>

<h3>Where can I find more technical details about High Availability (HA)?</h3>

<p>See the article <a href="https://www.rackspace.com/knowledge_center/article/high-availability-for-cloud-databases">High Availability for Cloud Databases</a>.</p>

---------
<h2>Replication</h2>

<h3>Can I monitor replication?</h3>

<p>Yes. You can monitor replication using the monitoring agent installed on the instance. For more information, see <a href="https://developer.rackspace.com/docs/cloud-databases/v1/developer-guide/#document-general-api-info/monitoring-read-replication">Monitoring Read Replication</a> in the API documentation.</p>

<h3>Is replication supported between different versions of the database?</h3>

<p>No. You can only add replica of the same database type and version as your source database instance.</p>

<h3>Is replication supported between different regions?</h3>

<p>No. You can only add a replica in the same region as your source database instance.</p>

<h3>Does setting up replication require downtime?</h3>

<p>When you add a replica to the source DB instance, the instance gets restarted. So your database will be unavailable until the instance restarts.</p>

<h3>Is there a charge for replication?</h3>

<p>Each read replica added is charged the same way as a new instance.</p>

<h3>Does replication support auto failover?</h3>

<p>Currently replication does not support auto failover. In case your database instance goes down and you would like to use replica instance for minimizing downtime, you will have to do a manual failover to the replica instances. For manual failover, you must detach the replica from the source instance and change the application endpoint to this new source database instance.</p>

<h3>Is replication supported for all database types?</h3>

<p>Replication is supported for MySQL 5.6, Percona 5.6, and MariaDB 10. We do not support replication for MySQL 5.1 as this is an older version of MySQL and there have been significant improvements for replication support in newer versions of MySQL. We highly recommend all users to <a href="https://www.rackspace.com/knowledge_center/article/upgrade-a-cloud-databases-instance-from-mysql-51-to-mysql-56"> upgrade from MySQL 5.1 to MySQL 5.6</a>.</p>

<h3>Do you support replication?</h3>

<p>Yes we do support Master Slave Replication. You can add and manage replicas using <a href="https://mycloud.rackspace.com/">Cloud Control Panel</a> and Cloud Databases API. For more information about managing replication with API, see <a href="https://developer.rackspace.com/docs/cloud-databases/v1/developer-guide/#document-general-api-info/replication">API docs for replication</a>.</p>

---------
<h2>Billing</h2>

<h3>How much does Cloud Databases cost?</h3>

<p>Pricing information is available at <a href="http://www.rackspace.com/cloud/databases/pricing/">the Cloud Databases pricing page</a>. Standard charges apply for any Cloud Servers, Cloud Load Balancers, or Cloud Sites that are used to access your Cloud Database instances.</p>
