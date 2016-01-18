---
node_id: 3390
title: Permissions Matrix for Cloud Load Balancers
type: article
created_date: '2013-04-10'
created_by: Renee Rendon
last_modified_date: '2015-05-26'
last_modified_by: Kyle Laffoon
product: Cloud Load Balancers
body_format: tinymce
---

The following permissions matrix displays specific permissions for the
roles in Cloud Load Balancers. The matrix displays the method names,
their corresponding RESTful API commands, and the roles that are
supported.

**[API Documentation](http://docs.rackspace.com/)<span> </span>**

**[Related Knowledge Center
Articles](/how-to/)**

**[Cloud Load Balancer
Terminology](#Cloud%20Load%20Balancer%20Terminology)**

**As of May 24, 2015**

CAPABILITY

ROLE

DESCRIPTION

Method Name

API Action

Observer

Creator

Admin



### LOAD BALANCER

<span>List Load Balancers</span>

<span>GET /loadbalancers</span>

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Provide a list of all load balancers configured and associated
with your account.</span>

<span>List Load Balancer Details</span>

<span>GET /loadbalancers/</span><span>{loadBalancerId}</span>

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Provide a list of all load balancers configured and associated
with your account. \*</span>

<span>Create Load Balancer</span>

<span>POST /loadbalancers</span>



<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Create a new load balancer with the configuration defined by the
request.</span>

<span>Update Load Balancer Attributes</span>

<span>PUT /loadbalancers/{loadBalancerId}</span>



 <img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Asynchronously update the attributes of the specified load
balancer.</span>

<span>Remove Load Balancer</span>

<span>DELETE /loadbalancers/</span><span>{loadBalancerId}</span>





<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Remove the specified load balancer and its associated
configuration from the account.</span>

<span>Remove Load Balancer Batch Delete</span>

<span>DELETE /loadbalancers{?id}</span>





<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Bulk-delete load balancers.</span>

### ERROR PAGES

<span>List Error Page</span>

<span>GET
/loadbalancers/</span><span>{loadBalancerId}</span><span>/errorpage</span>

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>List error page configured for the specified load balancer.</span>

<span>Update Error Page</span>

<span>PUT
/loadbalancers/</span><span>{loadBalancerId}</span><span>/errorpage</span>



 <img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Set custom error page for the specified load balancer.</span>

<span>Delete Error Page</span>

<span>DELETE
/loadbalancers/</span><span>{loadBalancerId}</span><span>/errorpage</span>





<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Delete custom error page for the specified load balancer.</span>

### LOAD BALANCER STATISTICS

<span>List Load Balancer Stats</span>

<span>GET
/loadbalancers/</span><span>{loadBalancerId}</span><span>/stats</span>

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Provide detailed stats output for a specific load balancer.</span>

### NODES

<span>List Nodes</span>

<span>GET
/loadbalancers/</span><span>{loadBalancerId}/</span><span>nodes</span>

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>List node(s) configured for the load balancer.</span>

<span>List Details of Specific Node</span>

<span>GET
/loadbalancers/</span><span>{loadBalancerId}</span><span>/nodes/{nodeId}</span>

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>List details of a specific node.</span>

<span>Add Nodes</span>

<span>POST
/loadbalancers/</span><span>{loadBalancerId}</span><span>/nodes</span>



<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

Add a new node to the load balancer.

<span>Modify Nodes</span>

<span>PUT
/loadbalancers/</span><span>{loadBalancerId}</span><span>/nodes/{nodeId}</span>



 <img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Modify the configuration of a node on the load balancer.</span>

<span>Delete Nodes</span>

<span>DELETE
/loadbalancers/</span><span>{loadBalancerId}</span><span>/nodes/{?nodeId}</span>





<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Delete a node from a specified load balancer.</span>

<span>Delete Nodes Batch</span>

<span>DELETE
/loadbalancers/</span><span>{loadBalancerId}</span><span>/nodes/{nodeId}</span>





<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Bulk-delete the specified nodes from a specified load
balancer.</span>

<span>List Nodes</span>

<span>GET
/loadbalancers/</span><span>{loadBalancerId}/</span><span>nodes</span>

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>List node(s) configured for the load balancer.</span>

### VIRTUAL IPs

<span>List Virtual IPs</span>

<span>GET /loadbalancers/loadBalancerId/virtualips</span>

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>List virtual IPs that are associated with a specified load
balancer.</span>

<span>Add Virtual IPs</span>

<span>POST /loadbalancers/{loadBalancerId}/virtualips</span>



<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Add virtual IP version 6.</span>

<span>Bulk-delete Virtual IPs</span>

<span>DELETE
/loadbalancers/{loadBalancerId}/virtualips/{?virtualIpId}</span>





<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Bulk-delete specified virtual IPs.</span>

<span>Delete Virtual IPs</span>

<span>GET
/loadbalancers/{loadBalancerId}/virtualips/{virtualIpId}</span>





<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Delete a specified virtual IP.</span>

### ALLOWED DOMAINS

<span>List Allowed Domains</span>

<span>GET /loadbalancers/alloweddomains</span>

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>View a list of allowed domains. \*\*</span>

### USAGE REPORTS

<span>List Billable Load Balancers</span>

<span>GET
/loadbalancers/billable</span><span>{?startTime,endTime,offset,
limit}</span>

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>List billable load balancers for the given date range. The
response is paginated with a default limit of 500 and a maximum limit of
1000.</span>

<span>Show Account-level Usage</span>

<span>GET /loadbalancers/usage</span><span>{?startTime,endTime}</span>

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Show account-level usage.</span>

<span>Show Historical Usage</span>

<span>GET
/loadbalancers/{loadBalancerId}/usage{?startTime,endTime}</span>

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Show historical usage. \*\*\*</span>

<span>Show Current Usage</span>

<span>GET
/loadbalancers/{loadBalancerId}/usage/current/</span><span>{?startTime,endTime}</span>

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Show current usage.</span>

### ACCESS LISTS

<span>Show Access List</span>

<span>GET /loadbalancers/{loadBalancerId}/accesslist</span>

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Show the access list.</span>

<span>Create or Update Access List</span>

<span>POST /loadbalancers/{loadBalancerId}/accesslist</span>



<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Create or append to an existing access list.</span>

<span>Delete Access List</span>

<span>DELETE /loadbalancers/{loadBalancerId}/accesslist</span>





<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Delete the entire access list.</span>

<span>Bulk-delete Specified Networks</span>

<span>DELETE
/loadbalancers/{loadBalancerId}/accesslist/{?networkItemId}</span>





<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Bulk-delete the specified networks from an access list.</span>

<span>Delete Network Item from Access List</span>

<span>DELETE /loadbalancers/{loadBalancerId}/accesslist/
{networkItemId}</span>





<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Delete a network item from a specified access list.</span>

### MONITOR HEALTH

<span>Show Health Monitor Configuration</span>

<span>GET /loadbalancers/{loadBalancerId}/healthmonitor</span>

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Show the health monitor configuration, if one exists.</span>

<span>Update Health Monitor</span>

<span>PUT /loadbalancers/loadBalancerId/healthmonitor</span>



<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Update the settings for a health monitor.</span>

<span>Delete Health Monitor</span>

<span>DELETE /loadbalancers/loadBalancerId/healthmonitor</span>





<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Delete a health monitor.</span>

### SESSION PERSISTENCE

<span>Show Session Persistence Configuration</span>

<span>GET /loadbalancers/{loadBalancerId}/sessionpersistence</span>

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>List session persistence configuration.</span>

<span>Enable Session Persistence</span>

<span>PUT /loadbalancers/{loadBalancerId}/sessionpersistence</span>



<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Enable session persistence.</span>

<span>Disable Session Persistence</span>

<span>DELETE /loadbalancers/{loadBalancerId}/sessionpersistence</span>





<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Disable session persistence.</span>

### LOG CONNECTIONS

<span>Show Connection Logging Configuration</span>

<span>GET /loadbalancers/{loadBalancerId}/connectionlogging</span>

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Show connection logging configuration.</span>

<span>Enable or Disable Connection Logging</span>

<span>PUT /loadbalancers/{loadBalancerId}/connectionlogging</span>



<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Enable or disable connection logging.</span>

Note: Enable connection logging requires that the user have access to
Cloud Files, which is used for storing the logs.

### THROTTLE CONNECTIONS

<span>Show Connection Throttling Configuration</span>

<span>GET /loadbalancers/{loadBalancerId}/connectionthrottling</span>

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Show connection throttling configuration.</span>

<span>Create or Update Connection Throttling Configuration</span>

<span>PUT /loadbalancers/{loadBalancerId}/connectionthrottling</span>



<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Create or update throttling configuration.</span>

<span>Delete Connection Throttling Configuration</span>

<span>DELETE /loadbalancers/{loadBalancerId}/connectionthrottling</span>





<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Delete connection throttling configurations.</span>

### CONTENT CACHING

<span>Show Content Caching Configuration</span>

<span>GET /loadbalancers/{loadBalancerId}/contentcaching</span>

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Show current configuration of content caching.</span>

<span>Enable or Disable Content Caching</span>

<span>PUT /loadbalancers/{loadBalancerId}/contentcaching</span>



<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Enable or disable content caching.</span>

### PROTOCOLS

<span>List Load Balancer Protocols</span>

<span>GET /loadbalancers/protocol</span>

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>List supported load balancing protocols.</span>

### ALGORITHMS

<span>List Load Balancer Algorithms</span>

<span>GET /loadbalancers/algorithms</span>

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>List all supported load balancing algorithms.</span>

### SSL TERMINATION / CERTIFICATE MAPPINGS

<span>Show SSL Termination Configuration</span>

<span>GET /loadbalancers/{loadBalancerId}/ssltermination</span>

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Show the load balancer's SSL termination configuration.</span>

<span>Update SSL Termination</span>

<span>PUT /loadbalancers/{loadBalancerId}/ssltermination</span>



<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Update the SSL termination. \*\*\*\*\*</span>

<span>Delete SSL Termination</span>

<span>DELETE /loadbalancers/{loadBalancerId}/ssltermination</span>





<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Delete SSL termination.</span>

<span>List Certificate Mappings</span>

<span>GET
/</span><span>loadbalancers/{loadBalancerId}/ssltermination/certificatemappings</span>

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>List certificate mappings that are configured for a specified load
balancer.</span>

<span>Add </span><span>Certificate Mapping</span>

<span>POST
/</span><span>loadbalancers/{loadBalancerId}/</span><span>ssltermination/certificatemappings</span>



<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Add a certificate mapping to a specified load balancer.</span>

<span>Show </span><span>Certificate Mappings Details</span>

<span>GET
/</span><span>loadbalancers/{loadBalancerId}/</span><span>ssltermination/certificatemappings/{certificateMappingId}</span>

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Show details for a specified certificate mapping.</span>

<span>Update </span><span>Certificate Mapping</span>

<span>PUT
/</span><span>loadbalancers/{loadBalancerId}/</span><span>ssltermination/certificatemappings/{certificateMappingId}</span>



<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Update the configuration for a specified certificate mapping on a
specified load balancer.</span>

<span>Delete </span><span>Certificate Mapping</span>

<span>DELETE
/</span><span>loadbalancers/{loadBalancerId}/</span><span>ssltermination/certificatemappings/{certificateMappingId}</span>





<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Delete a certificate mapping from a specified
load </span>balancer.

### METADATA

<span>Add Load Balancer Metadata </span>

<span>POST /loadbalancers/{loadBalancerId}/metadata</span>

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Add a new metadata item to the load balancer.</span>

Show Load Balancer Metadata

GET /loadbalancers/{loadBalancerId}/metadata

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

Show all metadata associated with the specified load balancer.

Bulk-delete Load Balancer Metadata Items

DELETE /loadbalancers/{loadBalancerId}/metadata{?metaId}





<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

Bulk-delete the metadata items given specified id list.

Show Load Balancer Metadata Item

<span>GET /loadbalancers/{loadBalancerId}/metadata/{metaId}</span>

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Show details for a specified metadata item for a specified load
balancer.</span>

Update <span>Load Balancer Metadata Item</span>

<span>PUT /loadbalancers/{loadBalancerId}/metadata/{metaId}</span>



<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Update the configuration of a metadata item on the load
balancer.</span>

<span>Delete Load Balancer Metadata Item</span>

<span>DELETE /loadbalancers/{loadBalancerId}/metadata/{metaId}</span>



<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Delete a metadata item from the load balancer.</span>

<span>Show Load Balancer Node Metadata</span>

GET <span>loadbalancers/{loadBalancerId}/nodes/{nodeId}/metadata</span>



 <img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Show all metadata associated with a specified node and load
balancer.</span>

<span>Add Load Balancer Node Metadata</span>

<span>POST </span><span>loadbalancers/{loadBalancerId}/nodes/{nodeId}/metadata</span>



 <img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Adds a metadata item to a specified node and load balancer.</span>

<span>Bulk-delete Load Balancer Node Metadata Items</span>

DELETE <span>loadbalancers/{loadBalancerId}/nodes/{nodeId}/metadata{?metaId}</span>





<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Bulk-deletes the metadata items given specified id list.</span>

Show Load Balancer Node Metadata Item

<span>GET
loadbalancers/{loadBalancerId}/nodes/{nodeId}/metadata/{metaId}</span>

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Show details for a specified metadata item for a specified node
and load balancer.</span>

<span>Update Load Balancer Node Metadata Item</span>

PUT <span>loadbalancers/{loadBalancerId}/nodes/{nodeId}/metadata/{metaId}</span>



<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Update the configuration of a metadata item on the node.</span>

<span>Delete Load Balancer Node Metadata Item </span>

<span>loadbalancers/{loadBalancerId}/nodes/{nodeId}/metadata/{metaId}</span>





<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

<span>Delete a metadata item from the node.</span>

### LIMITS

List Absolute Limits

 <span>GET /loadbalancers/absolutelimits/</span>

 <img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

 <img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

 <img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

 <span>Return the current absolute limits for the account.</span>

List Limits

 <span>GET /loadbalancers/limits</span>

 <img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

 <img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

 <img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/green%20checkmark_2.png" alt="check" width="41" height="39" />

 <span>Return the current limits for the account.</span>

\* This operation is not capable of returning details for a load
balancer which has been deleted.

\*\* <span>Currently only Rackspace-based domain names are
supported.</span>

<span>\*\*\* </span><span>Historical usage data is available for up to
90 days of service activity.</span>

<span>\*\*\*\*\* </span>**<span>Warning</span>**<span>:</span>
If<span> SSL is enabled on a load balancer that is configured with nodes
that are NOT in the same datacenter, then decrypted traffic will be sent
in clear text over the public internet to the external node(s) and will
no longer be secure.</span>

<span> </span>

[]()Cloud Load Balancer Terminology
-----------------------------------

### Algorithm

A Process <span>that defines how traffic should be directed between
back-end nodes.</span>

### **Connection Logging**

A feature that allows logs to be delivered to a Cloud Files account
every hour. For HTTP-based protocol traffic, these are Apache-style
access logs. For all other traffic, this is connection and transfer
logging.

### [**Content Caching**](/how-to/content-caching-for-cloud-load-balancers)

<span>An operation that stores </span><span>recently-accessed files on
the load balancer for easy retrieval by web clients. </span>

### **<span>Error Page</span>**

<span>The HTML file that is shown to an end user who is attempting to
access a load balancer.</span>

### **<span>Health Monitor</span>**

<span>A configurable feature of each load balancer. It is used to
determine whether or not a back-end node is usable for processing a
request. The load balancing service currently supports active health
monitoring.</span>

### [**Load Balancer**](/how-to/configure-a-load-balancer)

<span>A logical device which belongs to a cloud account. It is used to
distribute workloads between multiple back-end systems or services,
based on the criteria defined as part of its configuration.</span>

### <span>Metadata</span>

<span>Metadata can be associated with each load balancer and each node
for the client's personal use. It is defined using key-value pairs where
the key and value consist of alphanumeric characters. A key is unique
per load balancer.</span>

### **<span>Node</span>**

<span>A back-end device providing a service on a specified IP and
port.</span>

### **Session Persistence**

A<span> feature of the load balancing service that forces multiple
requests from clients to be directed to the same node.</span>

### **<span>Usage Reports</span>**

<span>A report that provides a view of all transfer activity, average
number of connections, and number of virtual IPs associated with the
load balancing service. </span>

### **<span>Virtual IP</span>**

<span>An Internet Protocol (IP) configured on the load balancer for use
by clients connecting to a service that is load balanced. Incoming
connections are distributed to back-end nodes based on the configuration
of the load balancer.</span>

<span> </span>

[&lt; Permission Matrices for RBAC](/how-to/permissions-matrix-for-role-based-access-control-rbac)
--------------------------------------------------------------------------------------------------------------------------------------------



