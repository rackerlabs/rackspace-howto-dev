---
node_id: 4414
title: Using dedicated load balancers with RackConnect v3.0
type: article
created_date: '2014-11-11 17:43:04'
created_by: juan.perez
last_modified_date: '2014-12-09 20:5150'
last_modified_by: kyle.laffoon
products: RackConnect
body_format: tinymce
---

undefined&rsquo;s management
    page, click **Select Pools**.
2.  Clear the check box for each load balancer pool from which you want
    to remove the cloud server.
3.  Click **Save Selected Load Balancer Pool(s)** to save your changes.

**Automation-compatible load balancer pools**

For load balancer pools to be recognized by RackConnect automation, the
following requirements must be met:

-   At least one pool member exists. A disabled pool member (existing,
    but not actively used) is used as a placeholder by default.
-   All pool members use the same forwarding port

If you do not see any available pools, when adding pool members from the
control panel (in the **Load Balancer pools** section under
 **RackConnect Details**), RackConnect automation was not able to detect
any automation-compatible load balancer pools on your dedicated load
balancer. If this is the case, contact Rackspace Network Security to
request the creation of one or more load balancer pools that are
RackConnect automation-ready.

### \
 **Use the RackConnect v3.0 API**

After you initially create a cloud server, you can use the following
RackConnect v3.0 API load balancer pool operations:

-   Retrieve a list of load balancer pools
-   Retrieve pool details for a given load balancer pool
-   Retrieve a list of all pool member nodes for a given load balancer
    pool
-   Retrieve details for a given pool member node (servers) within a
    given load balancer pool
-   Add a pool member node to a given load balancer pool
-   Remove a pool member node from a given load balancer pool
-   Bulk add multiple pool member nodes to one or more load balancer
    pools
-   Bulk remove multiple pool member nodes from one or more load
    balancer pools

The RackConnect v3.0 API is region-specific and returns results only for
the region specified in the URL of the API call itself.

For more information about using the RackConnect v3.0 API to manage load
balancer pool memberships, see [RackConnect v3.0
API](http://docs.rcv3.apiary.io/#loadbalancerpools).

If you have any questions, we are here to help. Our contact information
is available on the [Contact
Us](http://www.rackspace.com/knowledge_center/support) page.

