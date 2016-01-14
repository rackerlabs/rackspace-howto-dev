---
node_id: 3690
title: Cloud Queues FAQ
type: article
created_date: '2013-09-18 16:28:37'
created_by: megan.meza
last_modified_date: '2014-05-27 21:1357'
last_modified_by: rose.contreras
product: Cloud Queues
body_format: tinymce
---

**Q.  Will Cloud Queues work with Hybrid or RackConnect?**

A.  Yes. Cloud Queues will offer both public and snet IP's, so as long
as the dedicated network partition is set up to allow traffic to one of
these targets, Cloud Queues can be accessed.

**Q.  What does it cost to use Cloud Queues?**

A.  Please consult the [Cloud Queues product
page](http://www.rackspace.com/cloud/queues/) on our website for the
most current pricing.

**Q.  What happens if a message is stuck in a queue?  How can this be
fixed?**

A. Messages can't get stuck in a queue.  After posting a message, the
client will receive a resource URL which can be used to delete the
message. Alternatively, the client can simply wait for the message to
expire, at which point the service will automatically remove it.  All
messages have a "Time to Live" or TTL, which is configurable by the
user.

**Q.  Can a queue be migrated from one server to another server?**

A. Each queue is associated with a single cloud account, and is not tied
to any server in particular under that account. Queues cannot be
migrated between cloud accounts.

**Q.  Are there any limitations that Cloud Queues customers should be
aware of?**

A.  Yes, messages cannot be larger than 256K (excluding white space),
and a single request cannot contain more than 10 messages. If a single
request has multiple messages, the sum of those messages (excluding
white space) cannot exceed 256K. 

**Q.  What is the underlying message queuing system?**

A. Cloud Queues is based on the OpenStack "Marconi" project and uses its
own persistent, highly-available, document-based data store.  Cloud
Queues is not a wrapper around AMQP or other protocols.

**Q.  How can I be assured my messages will not be lost?**

A. Each message is replicated across three storage nodes, in memory, and
also persisted to disk. Messages are not replicated across data centers
(regions) at this time.

**Q.  How is the product different from RabbitMQ?**

A. Cloud Queues offers a simpler, HTTP-based API making it ideal for
modern web application development. The service does not rely on, or
even support persistent connections other than standard HTTP keep-alive,
and so is more reliable when accessed through firewalls and across
multiple network partitions (i.e., the Internet). The service is HA and
durable, and requires absolutely no setup or maintenance on the part of
the developer or system administrator. 

**Q.  Will we be able to enable some form of transaction logging that we
can store to Cloud Files or other accessible storage?**

A. This is on our roadmap.

**Q.  What stats does the API return?**

A.  We currently only offer a few very basic per-que stats but intend to
develop additional stats for GA.  The stats currently offered include
oldest message, newest message, number of claimed messages, number of
unclaimed messages.  However, it is easy to hook Graphite up to the
GetQueueStats call to plot graphs on the amount of free and unclaimed
messages.

**Q.  Can I run a local Marconi server with MongoDB?**

A.  Yes, you can find it documented on github:
 [https://github.com/stackforge/marconi/blob/master/README.rst](https://github.com/openstack/marconi/blob/9b9636c150252d65d9f225b3f49bfa76660a9741/README.rst)

**Q.  What is the maximum amount of time a message can be stored?**

A.  14 days.  The default message TTL will be set to 72 hours. 

**Q.  Is there be a max queue length to prevent queues from growing out
of control?**

A.  There are no limits on the number of queues or the number of
messages that a queue can contain. 

**Q.  Is there a limit of max requests per second for these API
operations?**

A.  Yes, customers will be limited to 300 request per second per
account.  Please contact support if you need to exceed this limit.  

**Q.  What do I need to enter for the "X-Project-ID" field?**

A.  Project ID is the Tenant ID, and is the customer's account number.

