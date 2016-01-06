---
node_id: 4064
title: Deploying Rackspace Cloud Big Data
permalink: article/deploying-rackspace-cloud-big-data
type: article
created_date: '2014-05-07 15:08:31'
created_by: kyle.laffoon
last_modified_date: '2016-01-04 20:5856'
last_modified_by: kyle.laffoon
products: Cloud Big Data
body_format: tinymce
---

The Rackspace Cloud Big Data Platform provides a scalable, robust, and
complete Hadoop cluster within a few clicks. All Cloud Big Data
deployments are backed by [Hortonworks Data
Platform](http://hortonworks.com/) (HDP). Using HDP enables Cloud Big
Data to take advantage of Hadoop packages and patches provided by
Hortonworks, as well as an escalation path to some of the top
contributors of the core Hadoop projects.

Two deployments are available: HDP 1.3 and HDP 2.1. Both include the
core Hadoop components (for example, MapReduce and HDFS) as well as Pig
and Hive. The 2.1 deployment also includes Tez. Pig and Hive will take
advantage Tez for data processing, by default.

Build a cluster
---------------

There are multiple methods for deploying and scaling your Hadoop
cluster: the API, Cloud Control Panel, and Lava command line. API and
Lava client walkthroughs are provided under [Using the Python Lava
Client](http://docs.rackspace.com/cbd/api/v1.0/cbd-getting-started/content/Using_Python_lavaclient.html)
in the [Getting Started
Guide](http://docs.rackspace.com/cbd/api/v1.0/cbd-getting-started/content/CBD_Overview.html).

You can create a cluster through the Cloud Control Panel as follows:

1.  Log in to the [Cloud Control Panel](https://mycloud.rackspace.com).

2.  In the menu bar at the top of the window, click **Databases \> Big
    Data**.

3.  Click **Create Cluster**.

4.  Provide values for the following fields, and then click **Create
    Cluster**:

    -   **Cluster Name:**Specify a name to identify and distinguish the
        cluster.
    -   **Region: **Specify the region in which to create the cluster.
    -   **Cluster Type: **Select the type of HDP deployment.
    -   **Node Size:**Specify the flavor of data nodes to use within the
        cluster.
    -   **Number of Nodes:**The number of data nodes within your
        cluster.
    -   **Username: **Specify a user that will be created on all nodes
        for access to and administration of the cluster.
    -   **Password: **Specify a password for the user.
    -   *(Optional)* **SSH Key Name:**If you want to access the cluster
        by using an SSH key, provide a name for the key.
    -   *(Optional)* **SSH Key:**If you chose to use an SSH key, specify
        the SSH public key.
    -   *(Optional)***Post-Install Script:**Specify the URL of a custom
        script to download and run on each node after deployment of the
        node has completed.
    -   *(Optional)***Alternate Storage:**If you want the option of
        accessing and storing data in Cloud Files from your cluster,
        select this check box.
    -   **Username: **If you are using alternate storage, specify the
        username of your Rackspace cloud account.
    -   **API Key:**If you are using alternate storage, specify the API
        key associated with your Rackspace cloud account. To find your
        API key, see [View and reset your API
        key](http://www.rackspace.com/knowledge_center/article/view-and-reset-your-api-key).

5.  After the status changes to Active, use SSH to log in to your
    Gateway node&rsquo;s PublicNet IP address, using the username and password
    that you provided in the user profile.

    ![](/knowledge_center/sites/default/files/field/image/HowtoBuildaCluster4.png)

Choosing a cluster
------------------

We recommend that you use the HDP 2.1 deployment, but if your workflow
requires the older versions of Hadoop, you can use the HDP 1.3
deployment. One difference you will notice is that the HDP 2.1
deployment includes a secondary Namenode where the HDP 1.3 deployment
has a stand alone Namenode.

Choosing a data node size
-------------------------

Cloud Big Data offers four flavors: Small (1.25 TB), Medium (2.5T),
Large (5T), and XLarge (10 TB). For complete specifications and pricing,
see
[http://www.rackspace.com/cloud/big-data/pricing/](http://www.rackspace.com/cloud/big-data/pricing/).

![](/knowledge_center/sites/default/files/field/image/cbd_example_builds.png)

 

For maximum performance, choose extra-large data nodes, which take up an
entire physical server to provide consistent cluster performance. If you
prefer to scale your environment more granularly or have lower storage
and processing needs, you can choose small data nodes.

More information
----------------

Following are some great links for further reading about data processing
as well as a data ingest method supported by Rackspace:

**Apache Pig**:

[http://hortonworks.com/hadoop-tutorial/how-to-process-data-with-apache-pig/](http://hortonworks.com/hadoop-tutorial/how-to-process-data-with-apache-pig/)

**Apache Hive**:

[http://hive.apache.org](http://hive.apache.org)

**Rackspace Swiftfs**:

[http://www.rackspace.com/knowledge\_center/article/swift-filesystem-for-hadoop](http://www.rackspace.com/knowledge_center/article/swift-filesystem-for-hadoop)

**Getting Data Into Your Cluster**:

[http://www.rackspace.com/knowledge\_center/article/getting-data-into-your-big-data-cluster](http://www.rackspace.com/knowledge_center/article/getting-data-into-your-big-data-cluster)

**Apache Tez**:

[http://hortonworks.com/hadoop/tez/](http://hortonworks.com/hadoop/tez/)

