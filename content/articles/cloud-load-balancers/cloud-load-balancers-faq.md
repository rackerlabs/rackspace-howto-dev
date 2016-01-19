---
node_id: 5004
title: 'Cloud Load Balancers: FAQs'
type: article
created_date: '2015-12-08'
created_by: Rackspace Support
last_modified_date: '2016-01-19'
last_modified_by: Stephanie Fillmon
product: Cloud Load Balancers
body_format: markdown_w_tinymce
---

<h2>Load Balancing</h2>

<h3>How do I see the original IP address of a connection to a load balancer?</h3>

<p>The connection's <code>X-Forwarded-For</code> HTTP header stores a visitor's originating IP address by default. For more information, see <a href="https://developer.rackspace.com/docs/cloud-load-balancers/v1/developer-guide/#creating-a-load-balancer"> the API documentation for creating a Cloud Load Balancer</a>.</p>

<h3>How do I configure SSL Termination using the Cloud Control Panel?</h3>

<p>You can quickly configure SSL termination for an existing Cloud Load Balancer by using the Cloud Control Panel.</p>

<ol>
	<li>Click on an existing load balancer to open its Details Page.</li>
	<li>Scroll to the Optional Features section.</li>
	<li>Click the Edit pencil to the right of the Secure Traffic (SSL) option.</li>
	<li>In the pop-up dialog box, enter and save your SSL configuration.</li>
</ol>

<p>How can I raise my API rate limits for Cloud Load Balancers?</p>

<p>To modify imposed API rate limits, contact Support.</p>

<h3>What is the maximum throughput of each load balancer?</h3>

<p>A single Cloud Load Balancer is connected through a 10Gb/second network to both the public network and Rackspace's internal network, which has been tested to achieve about 9Gb/second of actual throughput. Some limiting factors might influence the actual throughput at any given time.</p>

<h3>How long does it take to provision a load balancer?</h3>

<p>In most cases, it should take less than one minute to provision a load balancer after the <a href="http://www.rackspace.com/cloud/cloud_hosting_products/loadbalancers/api/">API</a> request is submitted. During periods of extreme system load, it should take no more than a few minutes for complete provisioning.</p>

<h3>Who should not use SSL termination on Cloud Load Balancers?</h3>

<p>You should not use SSL termination when transferring certain types of sensitive customer data classified as <a href="https://www.rackspace.com/knowledge_center/article/definition-of-personally-identifiable-information-pii" target="_self"> Personally Identifiable Information (PII) </a>. Examples of PII include information protected by the HIPAA and Gramm-Leach-Bliley acts, credit card information, or any personal data that can result in identity theft if disclosed.</p>

<h3>How do you manage and distribute IPs?</h3>

<p>Each load balancer comes with one public IPv4 address.</p>

<h3>How many concurrent connections can the service handle?</h3>

<p>A single load balancer is capable of consistently handling 20,000 concurrent connections with support for periodic spikes estimated at up to 100,000 concurrent connections. Because Cloud Load Balancers are implemented in a multi-tenant environment, estimates are not guaranteed and might vary depending on the number of concurrent connections that other customer load balancers are processing.</p>

<h3>Do Cloud Load Balancers work with dedicated servers?</h3>

<p>Yes, but we recommend using RackConnect to include <a href="http://www.rackspace.com/managed-hosting/dedicated-servers/">dedicated servers</a>, except in low-traffic scenarios, because of the potential for significant bandwidth charges. Without RackConnect, you are billed for bandwidth charges for requests outbound from the load balancer, and responses outbound from the dedicated firewall, inbound to the load balancer, <em>and</em> outbound again from the load balancer returning to the user.</p>

<h3>Can I use Cloud Load Balancers in conjunction with RackConnect®?</h3>

<p>You can use the <a href="http://www.rackspace.com/cloud/hybrid/rackconnect/">RackConnect</a> Cisco ASA solution to connect dedicated servers and cloud servers while leveraging Cloud Load Balancers to balance the workload between the cloud servers. Charges apply for outgoing bandwidth through the dedicated environment, as well as inbound and outbound traffic for the load balancers.</p>

<p>To include dedicated and cloud servers in the same resource pools (to balance the workload between both platforms), use the RackConnect F5 BIG-IP Local Traffic Manager solution.</p>

<h3>Can I manage my Cloud Load Balancer using the API?</h3>

<p>Yes, implementation and management of the Cloud Load Balancer solution is currently available through the Rackspace Cloud Control Panel and the API. To use the Cloud Load Balancer API, you should have a general understanding of the load balancing service and be familiar with the following technologies:</p>

<ul>
	<li>RESTful web services</li>
	<li>HTTP/1.1 conventions</li>
	<li>JSON and serialization formats</li>
	<li>Atom Syndication Format</li>
</ul>

<h3>How does Rackspace charge for bandwidth (public and private traffic)?</h3>

<ul>
	<li><strong>Public</strong> - Standard bandwidth rates apply for outbound transfers. There is no charge for inbound transfers.</li>
	<li><strong>Private</strong> - No charges apply for inbound or outbound bandwidth transfers over the Rackspace internal network.</li>
</ul>

<h3>How much does a Rackspace Cloud Load Balancer cost?</h3>

<p>See the <a href="http://www.rackspace.com/cloud/load-balancing/pricing/">pricing page</a> for details. If you enable log delivery to your Cloud Files account, standard charges for Cloud Files apply. Additionally, standard charges apply for additional (unique) virtual IP addresses per load balancer.</p>

<h3>What is a Cloud Load Balancer?</h3>

<p>Your business's website, applications, and web-based workloads depend on high availability. Rackspace <a href="http://www.rackspace.com/cloud/load-balancing/">Cloud Load Balancers</a> enable you to quickly balance the workload of multiple Cloud Servers for optimal traffic management and maximum failover protection. Load balancers distribute workloads across two or more servers, network links, and other resources to maximize throughput, minimize response time, and avoid network overload.</p>

<h3>What are the requirements for using SSL Termination?</h3>

<p>When using SSL Termination on your load balancers, the following requirements should be understood.</p>

<ul>
	<li>Additional fees apply when SSL Termination is enabled.</li>
	<li>SSL Termination is available to Rackspace Cloud Load Balancer customers in the US and UK with a valid SSL certificate/intermediate certificate and associated private key.</li>
	<li>SSL Termination cannot be enabled when a Cloud Load Balancer is provisioned; it must be configured on existing load balancers by issuing a command through the API. Read our Developer's Guide to learn <a href="https://developer.rackspace.com/docs/cloud-load-balancers/v1/developer-guide/#document-api-operations/ssl-termination">how to configure SSL Termination</a> on an existing load balancers through the API.</li>
</ul>

<p>For information about how to do this in the Control Panel, see <a href="https://community.rackspace.com/products/f/25/t/3302">SSL Termination - How to set it up</a>.</p>

<h3>What is ServiceNet?</h3>

<p>ServiceNet is an internal only, multi-tenant network connection within each Rackspace data center. ServiceNet IP addresses are not accessible from the public Internet and are local to each data center.</p>

<p><strong>Note</strong> : You can configure your account resources, such as Cloud Servers and Cloud Load Balancers, to utilize a ServiceNet IP address instead of the public IP address. Any traffic that occurs between your cloud resources on the Rackspace Network does not incur bandwidth charges.</p>

<p>If you filter traffic to your servers by using a firewall, the best practice is to allow the subnet range in which your Load Balancer resides. For more information how to filter traffic from a load balancer on your servers, see <a href="https://www.rackspace.com/knowledge_center/article/using-cloud-load-balancers-with-rackconnect">Using Cloud Load Balancers with RackConnect</a>.</p>

<h3>What are the security concerns with SSL termination?</h3>

<p>After SSL termination decrypts the data at the Cloud Load Balancer, it passes the unencrypted data to any nodes that are configured for that device. If you have nodes that are not in the same data center as the SSL-enabled load balancer, that unencrypted data is sent over the public Internet to those nodes. Therefore we recommend that you use an SSL-enabled load balancer <strong>only with nodes that reside in the same data center as the load balancer.</strong> The proximity allows the load balancer to use the nodes’ private IP addresses (the ServiceNet) to limit unencrypted traffic to within the data center’s network, as illustrated in the following diagram.</p>

<p>(sslterminationsFAQpic.png)</p>

<h3>Do Cloud Load Balancers support SSL Termination?</h3>

<p>SSL Termination on Cloud Load Balancers is supported<a href="https://developer.rackspace.com/docs/cloud-load-balancers/v1/developer-guide/#document-api-operations/ssl-termination">via the API</a> and <a href="https://www.rackspace.com/knowledge_center/article/ssl-termination-on-cloud-load-balancers">through the Cloud Control Panel</a>. SSL Termination allows users to have their secure traffic terminate at the load balancer with centralized certificate management. Features of this service are as follows:</p>

<ul>
	<li>SSL acceleration for improved throughput</li>
	<li>Reduced CPU load at the application level for better performance</li>
	<li>HTTP/HTTPS session persistence</li>
</ul>

<p><strong>Note</strong> : SSL Termination should not be used when transferring certain types of <a href="/how-to/definition-of-personally-identifiable-information-pii"> Personally Identifiable Information (PII) </a> .</p>

<h3>What are the benefits of using SSL Termination on the Cloud Load Balancer?</h3>

<p>With SSL Termination the traffic is decrypted at the Cloud Load Balancer, and unencrypted traffic can now be distributed to one or more Cloud Servers to be processed</p>

<p>Following are other benefits:</p>

<ul>
	<li>The ability to configure a load balancer that accepts both secure &amp; unsecured traffic, or secure traffic only</li>
	<li>Can be a less expensive than a dedicated F5 load balancer solution</li>
	<li>Another alternative to using HA Proxy with Cloud Servers</li>
</ul>

<h3>How is SSL traffic normally handled?</h3>

<p>Secure traffic comes in to your site over an encrypted SSL connection, and it must be decrypted by the webserver which holds the SSL certificate. The Cloud Load Balancer passes all traffic directly to the Cloud Server with the corresponding SSL certificate, placing the burden of the decryption on that server alone. This is because each device (Cloud Server or Cloud Load Balancer) handling traffic through an SSL connection requires either its own SSL certificate or a Licensed Certificate Option.</p>
