---
node_id: 4166
title: Cloud Feeds FAQ
permalink: article/cloud-feeds-faq
type: article
created_date: '2014-07-31 18:08:17'
created_by: David Hendler
last_modified_date: '2015-09-02 22:1339'
last_modified_by: constanze.kratel
products: Cloud Servers
body_format: tinymce
---

Get quick answers to common questions about the Rackspace Cloud Feeds
service.

-   [Who can use Cloud Feeds?](#who)
-   [How much does Cloud Feeds cost?](#cost)
-   [How do I grant access to Cloud Feeds?](#access)
-   [What can I use Cloud Feeds for?](#usage)
-   [Where is Cloud Feeds available?](#where)
-   [What are the Terms of Service?](#terms)

* * * * *

### Who can use Cloud Feeds?

All Rackspace customers with a Cloud services account can use Cloud
Feeds.

^[back\\ to\\ top](#top)^

### How much does Cloud Feeds cost?

Cloud Feeds is available at no charge.

^[back\\ to\\ top](#top)^

### How do I grant access to Cloud Feeds?

For information about how to add Cloud Feeds to individual users on your
Cloud account, see [Cloud Feeds overview](/knowledge_center/node/4164).

^[back\\ to\\ top](#top)^

### What can I use Cloud Feeds for?

The following table shows the kind of information, in the form of
events, that you can receive for various Rackspace Cloud services.

Service

Feed name

Events

Autoscale

/autoscale/events

Actions Autoscale takes on behalf of the user

Cloud Backup

/backup/events

Bandwidth Usage\
 License Usage\
 Storage Usage

Cloud Big Data

/bigdata/events

Hadoop Cluster Usage

Cloud Block Storage

/cbs/events

Volume Usage

Cloud Databases

/dbaas/events

Database Memory and Disk Usage

Cloud DNS

/dns/events

Domain Create and Delete Events

Cloud Files

/files/events

Bandwidth Usage\
 Storage Usage

Cloud Identity

/identity/events

User Status Events

Cloud Load Balancers

/lbaas/events

Load Balancer Usage\
 System Status Events

Cloud Monitoring

/monitoring/events

Monitoring Usage

Cloud Queues

/queues/events

Bandwidth Usage\
 System Usage

First Generation Cloud Servers

/servers/events

Bandwidth Usage\
 Server Usage\
 System Status Events

Next Generation Cloud Servers

/nova/events

Bandwidth Usage\
 Server Usage\
 System Status Events

Rackspace CDN

/rackspacecdn/events

Bandwidth Usage\
 Request Count

Event notifications are stored for up to three days so they can be
retrieved when convenient. Events are published in JSON and XML format.
At this time most events are related to usage, with few system and
security events.

Cloud Feeds also supports the following:

-   NAST tenant IDs to access feeds that have been archived in Cloud
    Files containers.
-   Enterprise Security, which allows you to authenticate by using basic
    authentication via username and API key.
-   User access events that are encoded in the CADF standard.\
     **Note:** User access events for Identity and Next Generation
    Servers will be available in the near future.

^[back\\ to\\ top](#top)^

### Where is Cloud Feeds available?

Cloud Feeds is available in the following regions:

-   Chicago (ORD)
-   Dallas-Fort Worth (DFW)
-   Hong Kong (HKG)
-   London (LON)
-   Northern Virginia (IAD)
-   Sydney (SYD)

**Note:** Events that occur in a particular region are published in
Cloud Feeds in that region only. For example, if a Next Generation Cloud
Server in ORD transmits a bandwidth event, that event is only available
in the ORD region.

^[back\\ to\\ top](#top)^

### What are the Terms of Service?

During the Early Access period, the Cloud Feeds Terms of Service are
available at
[http://www.rackspace.com/information/legal/testterms](http://www.rackspace.com/information/legal/testterms).
When the Early Access Program is over, the Terms of Service will revert
to the standard Cloud Terms of Service.

^[back\\ to\\ top](#top)^

w.rackspace.com/information/legal/testterms).
When the Early Access Program is over, the Terms of Service will revert
to the standard Cloud Terms of Service.

^[back\\ to\\ top](#top)^

