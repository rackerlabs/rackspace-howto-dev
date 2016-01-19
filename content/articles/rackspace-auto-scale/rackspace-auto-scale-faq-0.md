---
node_id: 5005
title: Rackspace Auto Scale - FAQ
type: article
created_date: '2015-12-09'
created_by: Stephanie Fillmon
last_modified_date: '2016-01-19'
last_modified_by: Stephanie Fillmon
product: Rackspace Auto Scale
body_format: markdown_w_tinymce
---

<h2>Getting Started</h2>

<h3>Is there an easy path to migrate from other autoscaling products such as Rightscale?</h3>

<p>No. Your configurations cannot be migrated from other providers.</p>

<h3>Is authentication required for Auto Scale?</h3>

<p>Authentication is required to create a scaling group; you must send an&nbsp;<strong>X-Auth-Token</strong>&nbsp;header with most API requests. Authentication is not required to execute policies via anonymous webhooks.</p>

<h3>What do I need to do to get started using Auto Scale?</h3>

<p>Auto Scale works by horizontally scaling a particular tier of an application; for example, the web tier. You need to know which servers you want to scale. To get started, you need a server image that you have configured with all needed applications and settings, and that is configured to be ready when the server is started. You can ensure your servers deploy fully ready for service by using various programs such as Chef, Puppet, and Salt.</p>

---------
<h2>Account Services</h2>

<h3>Does Auto Scale record the history of a scale action?</h3>

<p>Not currently. The <strong>history</strong> resource on the Auto Scale API endpoint will show scaling history, triggers, and user changes. It will be available in a future release.</p>

<h3>How do I know what actions are taken by Auto Scale on my behalf?</h3>

<p>Some of the actions Auto Scale takes on your behalf are deferred; for example, when you set a schedule to create additional servers. Auto Scale will soon have an advanced audit log to track when Rackspace takes actions on your behalf. You will be able to access this through the&nbsp;<strong>history</strong>&nbsp;resource on the Auto Scale API endpoint.</p>

<h3>How much does the Rackspace Auto Scale service cost?</h3>

<p>Auto Scale is available at no cost to Rackspace Cloud customers, although you do pay for the servers created by a scale-up until they are removed.</p>

---------
<h2>Server Management</h2>

<h3>Can I add an existing server to an Auto Scale group?</h3>

<p>No. Even if you add the <strong>autoscale-group-id </strong>metadata to the server, the Auto Scale back end service will not know the server belongs in the group. Auto Scale manages only servers created by Auto Scale.</p>

<h3>What happens if I delete an Auto Scale server through the API or the Cloud Control Panel?</h3>

<p>Auto Scale currently does not track what happens to servers outside of the Auto Scale system. If a server is deleted outside of the system, Auto Scale will continue to treat the server as if it still exists. If you then try to delete the server through Auto Scale (for example, by scaling down), no problems should occur.</p>

<p>A new API endpoint has been added to Auto Scale, <strong>DELETE server</strong>, that allows you to remove a specific server from a scaling group. You can use this endpoint to bring Auto Scale back in sync with the correct number of servers in a group when a server has been deleted through the API or the Cloud Control Panel. For more information, see the Rackspace Auto Scale Developer's Guide <a href="https://developer.rackspace.com/docs/autoscale/v1/developer-guide/#delete-server-from-scaling-group">Delete server from scaling group</a> section.</p>

<h3>Can I suspend servers and restore them quickly to the same IP address?</h3>

<p>You can remove a server from an Auto Scale group and keep it on your Cloud account for observation. Auto Scale will automatically replace it with a new server.&nbsp;</p>

<p>Newly created servers have different IP addresses unless they are created in a scaling group with a load balancer.</p>

---------
<h2>Scaling and High Availability</h2>

<h3>Why might I see a server get created and then immediately destroyed?</h3>

<p>A server may be created for a scale-up operation and then be immediately deleted if there is a problem with the load balancer associated with the scaling group. The load balancer problems that can cause this are:</p>

<ul>
	<li>The load balancer is mis-configured</li>
	<li>The load balancer is at its limit</li>
	<li>The load balancer has been deleted</li>
</ul>

<p>If any of these problems are present, Auto Scale immediate deletes the newly-created server so the customer doesn't get billed for servers not in the load balancers.</p>

<h3>I got a 403 "Cannot execute policy - no change in servers" error when I tried to execute the policy. What does this mean?</h3>

<p>One possibility is that you tried to scale up or down beyond the configured minimum or maximum value. As a result, no servers could be created or destroyed. The error message could also mean that you are trying to set the needed capacity equal to what Auto Scale thinks is already there.</p>

<h3>Does Auto Scale drain connections on a node behind a load balancer as a server (LBaaS) before removing it from a pool?</h3>

<p>No. The server is removed from the load balancer before the delete command is sent. At present, connections are not drained.</p>

<h3>What is the maximum amount of time you can set for a cooldown timer?</h3>

<p>The maximum is 86400 seconds, equal to 24 hours.</p>

<h3>What is the minimum amount of time you can set for a cooldown time?</h3>

<p>Zero seconds. We recommend having the group cooldown being around 5 minutes (300 seconds) by default.</p>

<h3>How does Auto Scale moderate conflicting events?</h3>

<p>Cooldown timers are built in to the scaling group and the individual scaling policies, so that you can prevent too many servers from being created or deleted too quickly.</p>

<h3>Multiple scaling policies can be associated with the same scaling group. How is the "correct" policy selected when servers are generated?</h3>

<p>Scheduled policies are triggered at the time they are scheduled. Other policies are triggered by a webhook and the name or "handle" for each policy is defined by a construct called a webhook, which is a unique URL endpoing you call to invoke the policy execution.</p>

<h3>What are the different configuration parameters for scaling groups?</h3>

<p>For information on the parameters used with the Auto Scale API, see the <a href="https://developer.rackspace.com/docs/autoscale/v1/developer-guide/#document-api-operations/autoscale-groups">Scaling group configurations</a> and <a href="https://developer.rackspace.com/docs/autoscale/v1/developer-guide/#document-api-operations/configurations">Launch configuration</a> sections in the Auto Scale API Developer's Guide.</p>

<p>For information on the parameters used with the Auto Scale Control Panel, see the <a href="/how-to/rackspace-auto-scale-control-panel-user-guide-create-a-scaling-group">Create a scaling group</a> section in the Rackspace Auto Scale Control Panel User Guide.</p>

<h3>Are monitoring rules for the entire scaling group or can I monitor specific servers in the scaling group?</h3>

<p>No. There are no specific rules within Auto Scale for monitoring specific servers. However, you can do this through Monitoring configurations, which are documented in the <a href="https://developer.rackspace.com/docs/cloud-monitoring/v1/developer-guide/">Cloud Monitoring API Developer's Guide</a>.</p>

<h3>Can I have multiple load balancers in a scaling group?</h3>

<p>Yes. However, if you need to scale beyond 25 servers with a Cloud Load Balancer, we recommend creating multiple Auto Scale groups and creating a tree of load balancers.</p>

<h3>Is there a limit to the number of servers I can have in a scaling group?</h3>

<p>There is no maximum number of servers in a scaling group. However, a scaling group used with a Cloud Load Balancer instance is limited to 50 servers per load balancer group and you may have overall Cloud Servers limits on the number of servers you are allowed to create without having your quota bumped up. If you reach Cloud Load Balancer limits, Auto Scale will fail to add additional servers. If you are running up against limits with Cloud Load Balancer instances, you should consider creating multiple scaling groups and a tree of load balancers to service requests or using RackConnect to use a higher capacity hardware load balancer solution. For more information on RackConnect, see <a href="https://www.rackspace.com/knowledge_center/article/how-do-i-get-started-with-rackconnect-v20">How do I get started with RackConnect?</a></p>

<h3>Do the servers that I'm going to automatically scale up have to be associated with a group? If so, why?</h3>

<p>Yes. A scaling policy is associated with a specific group. All of the scaled-up servers are managed for health and monitoring in aggregate so they need to be part of a group.</p>

<h3>Can I create a scaling group with no servers in it?</h3>

<p>Yes. You can add servers later.</p>

<h3>What is a scaling group?</h3>

<p>A scaling group is a construct that contains the configuration for creating individual servers, has zero or more servers associated with it, and has one or more associated scaling policies that describe what actions to take when the policy is activated.</p>

<h3>Can I scale up servers in a particular order? For example, can I create a database server before creating a web server?</h3>

<p>No. Auto Scale does not scale up servers or load balancers in a particular order.</p>

<h3>Is it possible for Auto Scale to create servers that are not attached to a load balancer?</h3>

<p>Yes. A load balancer is not required as part of the launch configuration. however, you do need to configure how your servers get requests.</p>

<h3>Can Auto Scale add a server in ORD to a load balancer in the DFW data center, or use an image in DFW?</h3>

<p>No, all resources must be in the same data center. There is a different Auto Scale endpoint for each data center, and each endpoint orchestrates only within that data center. In the Auto Scale control panel, data centers are called&nbsp;<strong>Regions</strong>.</p>

<h3>Can I use Auto Scale across data centers?</h3>

<p>No, you must create separate scaling groups for different data centers.</p>

<h3>How does Auto Scale integrate with image services or other automation services, such as Chef or Puppet?</h3>

<p>Auto Scale is service agnostic and API based, so it works well with these services but does not explicitly integrate with them.</p>
