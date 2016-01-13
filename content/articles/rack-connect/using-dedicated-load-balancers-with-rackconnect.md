---
node_id: 2028
title: Using Dedicated Load Balancers with RackConnect v2.0
type: article
created_date: '2012-08-21 19:41:31'
created_by: juan.perez
last_modified_date: '2015-07-15 20:1948'
last_modified_by: kelly.holcomb
products: RackConnect
body_format: tinymce
---

undefined&mdash; Name Match:**Before you create your cloud servers, provide
Rackspace with the preferred names and the pool(s) to associate with
your cloud servers. Currently, you must configure this through a ticket
request to your Support team.\
 \
 Regardless of which option you select, consider the following
requirements:

-   Verify that an appropriate health check has been configured for
    members of the load balancer pool or pools being used. The health
    check should confirm that the website or application is fully ready
    to accept end-user traffic, because the cloud server might be added
    almost immediately after creation, but before your application is
    ready to accept traffic, depending on the timing of the automation.
    For example, it would be advisable to use a URL content check
    instead of a TCP port check to confirm that a web application is
    ready to accept end-user requests.

-   The service port for each member of the load balancer pool must
    match or the automation will not be able to determine which service
    port to use. (For this same reason, there should always be at least
    one member in the pool.)  If a common service port cannot be
    determined, a notification will be routed to your Support team for
    manual intervention.

To get the name of one or more load balancer pools, contact your Support
team.

**NOTE:**  Any cloud servers that were originally added to a load
balancer pool as a result of a name match rule will be automatically
removed if the respective name match rule is deleted.

#### Inbound RackConnect Traffic Flow with a F5 Load Balancer

The following diagram shows the path that inbound (and return) load
balancer pool traffic follows to your cloud servers when you use an F5
BIG-IP load balancer with RackConnect:\

![](http://www.rackspace.com/knowledge_center/sites/default/files/styles/full_width/public/field/image/RackConnect.F5.TrafficFlow.png)

\
 Brocade Load Balancers
-----------------------

The Brocade ADX can also be used as a load balancer that balances
traffic between dedicated and cloud servers. In this case, the
RackConnect Connected Device will be a Cisco ASA firewall and any
traffic that needs to be load balanced to cloud servers will flow from
the ADX to the firewall to the cloud servers.

**The benefits of using  a Brocade load balancer with RackConnect are as
follows:**

-   The ability to load balance traffic between dedicated servers and
    cloud servers

-   The ability to use cloud servers as sorry servers for a load
    balancer pool. A sorry server normally contains a static maintenance
    page that users are directed to when health checks fail for all the
    members of a load balancer pool.

-   The ability to maintain Client Identity (source IP persistence) to
    RackConnect Cloud Servers through the use of X-Forwarded headers.
    Your Support team can provide more details about the caveats of
    client identity maintenance.

**The limitations of using  a Brocade load balancer with RackConnect are
as follows:**

-   Because the Brocade load balancer cannot function as a RackConnect
    Connected Device, the RackConnect Automation feature that
    automatically adds and removes cloud servers from your load balancer
    pools is not available

-   The Brocade load balancer must function as a full proxy for all
    external requests to your cloud servers.

#### Inbound RackConnect Traffic Flow with a Brocade Load Balancer

The following diagram shows the path that inbound and return load
balancer pool traffic follows to your cloud servers when you use a
Brocade ADX load balancer with RackConnect:\

![](http://www.rackspace.com/knowledge_center/sites/default/files/styles/full_width/public/field/image/RackConnect.Brocade.TrafficFlow.png)

If you have any questions about using Dedicated load balancers with
RackConnect, contact your Support team.

[Accessing RackConnected Cloud
Servers](http://www.rackspace.com/knowledge_center/article/accessing-rackconnected-cloud-servers)
\<---Previous | Next ---\> [Using Cloud Load Balancers with
RackConnect](http://www.rackspace.com/knowledge_center/article/using-cloud-load-balancers-with-rackconnect)

