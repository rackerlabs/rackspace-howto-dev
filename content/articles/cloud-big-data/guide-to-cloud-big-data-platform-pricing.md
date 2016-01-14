---
node_id: 4063
title: Cloud Big Data Platform provisioning and pricing
type: article
created_date: '2014-05-07 15:02:15'
created_by: david.grier
last_modified_date: '2016-01-04 20:5430'
last_modified_by: kyle.laffoon
product: Cloud Big Data
body_format: tinymce
---

Rackspace Cloud Big Data Platform is a new public cloud offering
leveraging the Hortonworks Data Platform (HDP) and OpenStack. Users can
quickly deploy a full HDP stack and scale the solution simply by adding
new nodes on the configuration. The provisioning of resources in Cloud
Big Data Platform can be done easily via the Rackspace Cloud Control
Panel or API. For more information about how to get started using Cloud
Big Data Platform, see the [Getting
Started](http://docs.rackspace.com/cbd/api/v1.0/cbd-getting-started/content/DB_Doc_Change_History.html)
Guide.

Although Cloud Big Data Platform uses a standard and common Apache
Hadoop^TM^ distribution, it differs from running Hadoop on dedicated
servers or plain cloud servers. The back-end infrastructure of Cloud Big
Data Platform has been optimized for running Hadoop at scale and
includes gigabit Ethernet, optimized local storage, and easy API access.

The following sections provide information that will help you understand
the pricing and provisioning of this service.

Data node instances
-------------------

Cloud Big Data Platform offers four datanode sizes:

+----------------+----------------+----------------+----------------+----------------+
| ### **Flavor I | ### **Name**   | ### **vCPU**   | ### **RAM**    | ### **Disk**   |
| D**            |                |                |                |                |
+----------------+----------------+----------------+----------------+----------------+
| hadoop1-7      | Small Hadoop   | 2              | 7.5G           | 1.25T          |
|                | Instance       |                |                |                |
+----------------+----------------+----------------+----------------+----------------+
| hadoop1-15     | Medium Hadoop  | 4              | 15G            | 2.5T           |
|                | Instance       |                |                |                |
+----------------+----------------+----------------+----------------+----------------+
| hadoop1-30     | Large Hadoop   | 8              | 30G            | 5T             |
|                | Instance       |                |                |                |
+----------------+----------------+----------------+----------------+----------------+
| hadoop1-60     | XLarge Hadoop  | 16             | 60G            | 10T            |
|                | Instance       |                |                |                |
+----------------+----------------+----------------+----------------+----------------+
| onmetal-io1    | OnMetal Hadoop | 40             | 128G           | 3.2T           |
|                | instance       |                |                |                |
+----------------+----------------+----------------+----------------+----------------+

When provisioning, you need to know how much data node (disk) space is
needed to process your query or job. HDFS has a configurable level of
replication which we set based on the size of the provisioned cluster.

-   Replication Factor 1: 1-2 Datanodes
-   Replication Factor 2: 3-4 Datanodes
-   Replication Factor 3: \>4 Datanodes

Considering a Cloud Big Data deployment with 3x replication, you must
first take your raw data set and multiply that volume by 3. This value
indicates how much Cloud Big Data Platform resources you need.<br>
 <br>
 One additional thing to note is that a 10 TB instance actually occupies
an entire physical machine, so users do not have to worry about sharing
resources.

Gateway node
------------

The Gateway node is provisioned automatically when you create a cluster.
It is designed to give you access directly into the data nodes residing
in the cluster.

Name node
---------

The Name node is provisioned at the time of cluster creation. The Name
node handles the master services of the Hadoop cluster including the map
operation and logical location of the data copies.

Bandwidth
---------

All incoming bandwidth is provided at no charge, which means that you
are not metered or billed for bandwidth usage during import. Only
outgoing bandwidth is metered, which means that anything exported from
or distributed from the Hadoop cluster is charged. Bandwidth between
data nodes and the Name node or Gateway node, or between sets of data
nodes, is not metered or billed.

Scaling
-------

Hadoop is a distributed technology that allows for seamless horizontal
scaling. This means that you can easily expand the capacity of your
Hadoop cluster by simply adding a node to the cluster via the Coud
Control Panel or API. You can also scale down the resources by removing
data node instances from the cluster.

Cloud Files integration
-----------------------

One of the main features of Cloud Big Data Platform is its ability to
process data that lives in Cloud Files. For detailed information about
how to do this, see [Getting data into your Big Data Cluster
guide](http://www.rackspace.com/knowledge_center/article/getting-data-into-your-big-data-cluster).
It is important to note that any usage of Cloud Files is billed at the
storage rate for Cloud Files as outlined on the [Cloud Files pricing
page](http://www.rackspace.com/cloud/files/pricing/). Bandwidth and
transfer of Cloud Files data to Cloud Big Data is at no charge; however,
customers might incur bandwidth when exporting results back into Cloud
Files if the Cloud Files container is not in the same region (data
center) as the Hadoop cluster.

We hope that these additional points help you successfully understand
and deploy your Cloud Big Data solution. If you need help, reach out to
our data specialist support team by creating a ticket in the Rackspace
Cloud Control Panel.

