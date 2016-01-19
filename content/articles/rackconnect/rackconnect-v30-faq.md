---
node_id: 4271
title: RackConnect v3.0 - FAQ
type: article
created_date: '2014-09-26'
created_by: Juan Perez
last_modified_date: '2016-01-19'
last_modified_by: Stephanie Fillmon
product: RackConnect
body_format: markdown_w_tinymce
---

<p><strong>Applies to:</strong> RackConnect v3.0. For questions on RackConnect v2.0, see <a href="/how-to/rackconnect-20-faq">RackConnect 2.0 - FAQ</a>.</p>

<h3>Can I allocate multiple cloud networks to a single RackConnect v3.0 cloud server?</h3>

<p>No. We currently support only one cloud network per cloud server.</p>

<h3>Can I assign more than one cloud network IP address to my RackConnect v3.0 cloud servers?</h3>

<p>No. For each cloud server, we currently only support:</p>

<ul>
	<li>One cloud network</li>
	<li>One IP address per cloud network</li>
	<li>One public IP address network address translation (NAT) per cloud server</li>
</ul>

<h3>Can I upgrade my RackConnect v2.0 environment to RackConnect v3.0?</h3>

<p>Not yet, but we are working on a migration path. Initially, we plan to offer you the ability to associate a <em>new</em> cloud account with your existing RackConnect v2.0 configuration, which will enable you to experience RackConnect v3.0 without deactivating your existing RackConnect v2.0 environment. Note that only <em>next generation cloud servers</em> will be compatible with the migration process to RackConnect v3.0. We will provide more details about this process as they become available.</p>

<h3>Can I use a Brocade ADX 1000 as my RackConnect v3.0 edge device?</h3>

<p>No. Because of access list limitations, we currently support the Brocade ADX 1000 devices only in the connected device role. For a full list of network devices that are compatible with RackConnect v3.0, see <a href="/how-to/rackconnect-network-device-comparison">RackConnect Network Device Comparison</a>.</p>

<h3>Does RackConnect v3.0 support IPv6?</h3>

<p>Not yet — but support for IPv6 is anticipated for early 2016.</p>

<h3>Does RackConnect v3.0 support Managed Colocation environments?</h3>

<p>Network devices in a Managed Colocation environment are supported only if the network devices are managed by the Rackspace Network Security team. Customer-managed network devices are not supported. For more details about RackConnect v3.0 compatibility with other Rackspace offerings, see <a href="/how-to/rackconnect-v30-compatibility">RackConnect v3.0 Compatibility Matrix</a>.</p>

<h3>How do I get RackConnect v3.0?</h3>

<p>The answer varies based on whether you are an existing Rackspace customer:</p>

<ul>
	<li>If you are new to Rackspace, contact a member of our Sales team for help. For details about how to contact our Sales teams, go to <a href="http://www.rackspace.com/information/contactus/">Contact Rackspace</a>.</li>
	<li>If you are an existing Rackspace cloud-only customer, contact a member of our Sales team for help. For details about how to contact our Sales team, go to <a href="http://www.rackspace.com/information/contactus/">Contact Rackspace</a>.</li>
	<li>If you are an existing Rackspace dedicated-only customer, contact your account manager&nbsp;for help in getting RackConnect v3.0 set up in your environment.</li>
</ul>

<h3>Is it possible to attach a RackConnect v3.0 cloud network to pre-existing cloud servers?</h3>

<p>Yes, but with the following caveats:</p>

<p>Note that <em>pre-existing cloud servers</em> refers to cloud servers that were built before RackConnect v3.0 was associated with the cloud account.</p>

<ul>
	<li>For the best possible experience, we recommend using&nbsp;a clean cloud account (meaning a cloud account with no pre-existing cloud servers) with RackConnect v3.0.</li>
	<li>If the pre-existing cloud servers are using PublicNet, you must remove PublicNet before attempting to add a RackConnect v3.0 cloud network to the cloud server.</li>
	<li>If you are a Managed Operations customer and need help detaching PublicNet, contact your Rackspace support team for assistance.</li>
	<li>If the pre-existing cloud servers are using ServiceNet, the ServiceNet IP address will change because ServiceNet will be&nbsp;detached and then re-attached&nbsp;to apply the appropriate security policies. Note that ServiceNet in RackConnect v3.0 is highly restricted and cannot be used for communication between cloud servers.</li>
</ul>

<h3>What network subnet (CIDR) should I assign to my RackConnect v3.0 cloud network?</h3>

<p>See the <a href="/how-to/rackconnect-v30-limitations">Cloud Networks</a> section of <a href="/how-to/rackconnect-v30-limitations">RackConnect v3.0 limitations</a>.</p>

<h3>What requirements must be met to implement RackConnect v3.0 in my environment?</h3>

<p>For the full list of requirements, see <a href="/how-to/rackconnect-v30-requirements">RackConnect v3.0 requirements</a>.</p>

<h3>Whom do I contact for help with RackConnect v3.0?</h3>

<p>Because RackConnect spans both your cloud and dedicated environments, you can contact your cloud or dedicated hosting support teams for help with RackConnect. If you are certain that the issue you are experiencing is directly related to your cloud servers, we recommend contacting your cloud hosting team first. However, if you are certain that the issue is related to your network device, we recommend contacting your dedicated hosting team first. For details about how to contact your support teams, visit the <a href="/how-to/support">Contact Us</a> page.</p>

<h3>Why do I receive 403 Forbidden HTTP status code responses when I try to build RackConnect v3.0 cloud servers by using the Cloud Servers API or the nova client?</h3>

<p>By default, when you use the Cloud Servers API or nova client to build cloud servers, the servers are built with a PublicNet network. However, RackConnect v3.0 does not support PublicNet and restricts you from building cloud servers with PublicNet attached on RackConnect v3.0 linked cloud accounts. This restriction is likely the reason that you are receiving <code>403 Forbidden</code> responses. Following are details for resolving this error:</p>

<ul>
	<li>When building a cloud server using the nova client <code>boot</code> command, include the <code>--no-public</code> option to prevent the PublicNet network from being attached to the server. Note that you can also&nbsp;use the <code>--no-service-net</code> option with the nova client <code>boot</code> command to keep the ServiceNet network from being attached to a cloud server. However, consider that ServiceNet is required for cloud servers created in cloud accounts with a <a href="http://www.rackspace.com/managed-cloud/">Managed Operations</a> service level.</li>
	<li>With the Cloud Servers API, specify the cloud network that you want to attach to the cloud server. If you specify one or more networks, your server is attached to only those networks. See the <a href="https://developer.rackspace.com/docs/cloud-servers/v2/developer-guide/#document-getting-started/create-server-intro">Create your first Server </a> section of the Cloud Servers v2 Developer Guide for more information.</li>
</ul>
