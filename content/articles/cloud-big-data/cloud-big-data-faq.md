---
node_id: 5029
title: Cloud Big Data - FAQ
type: article
created_date: '2015-12-10'
created_by: Rackspace Support
last_modified_date: '2016-01-19'
last_modified_by: Stephanie Fillmon
product: Cloud Big Data
body_format: markdown_w_tinymce
---

<h2>Account Services</h2>

<h3>Can I manage the Cloud Big Data service through my Cloud Control Panel?</h3>

<p>Yes, you can manage your Cloud Big Data service through the Rackspace Cloud Control Panel, as well as by using a RESTful API.</p>

<h3>What is Rackspace Cloud Big Data?</h3>

<p>Rackspace Cloud Big Data is an on-demand Apache Hadoop service for the Rackspace Open Cloud. The service supports a RESTful API and alleviates the pain associated with deploying, managing, and scaling Hadoop clusters.</p>

<p>Cloud Big Data is just as flexible and feature-rich as Hadoop. With Cloud Big Data, you benefit from on-demand servers, utility-based pricing, and access to the full set of Hadoop features and APIs. However, you do not have to worry about provisioning, growing, or maintaining your Hadoop infrastructure. The Cloud Big Data service uses an environment that is specifically optimized for Hadoop, which ensures that your jobs run efficiently and reliably. Note that you are still responsible for developing, troubleshooting, and deploying your applications.</p>

<p>Cloud Big Data creates on-demand infrastructure for applications in production where physical servers would be too costly and time-consuming to configure and maintain.</p>

<p>You can use Big Data to perform the following tasks:</p>

<ul>
	<li>Develop, test, and pilot data analysis applications</li>
	<li>Create or resize Hadoop clusters in minutes and pay only for what you use</li>
	<li>Access the Hortonworks Data Platform (HDP), an enterprise-ready distribution that is 100 percent Apache open source</li>
	<li>Provision and manage Hadoop through an easy-to-use Control Panel and a RESTful API</li>
	<li>Seamlessly access data in Cloud Files containers</li>
	<li>Gain interoperability with any third-party software tool that supports HDP</li>
	<li>Access Fanatical Support® on a 24x7x365 basis via chat, ticket, or phone at 1-800-961-4454 (US toll free) and 1-210-312-4000 (international)</li>
</ul>

---------
<h2>Billing</h2>

<h3>What is the pricing for Cloud Big Data and how is it billed?</h3>

<p>Cloud Big Data is part of the Rackspace Cloud, and your use of it through the API is billed according to the pricing schedule listed on the<a href="http://www.rackspace.com/cloud/big-data">Cloud Big Data product page</a>. Cloud Servers is also part of the Rackspace Cloud, and your use of it through the Cloud Control Panel is billed according to <a href="http://www.rackspace.com/cloud/servers#pricinganchor">Cloud Servers pricing</a></p>

---------
<h2>General</h2>

<h3>How do I manage and customize Cloud Big Data?</h3>

<p>You can provision and manage the Cloud Big Data service through your Cloud Control Panel and a RESTful API.</p>

<h3>Where can I find the Cloud Big Data SLA?</h3>

<p>The service level agreements (SLAs) for Cloud Big Data and Cloud Servers are available at <a href="http://www.rackspace.com/cloud/legal/sla">http://www.rackspace.com/cloud/legal/sla</a>.</p>

<h3>Where can I access the Cloud Big Data API?</h3>

<p>You can access the Big Data API documentation at&nbsp;<a href="https://developer.rackspace.com/docs/">https://developer.rackspace.com/docs/</a>.</p>

<h3>Who do I contact if I need help or have problems with my Cloud Big Data service?</h3>

<p>You can access Rackspace Fanatical Support® on a 24x7x365 basis by using the following methods:</p>

<ul>
	<li>Live Chat: Click LiveChat in the Cloud Control Panel</li>
	<li>Phone: US toll free 1-800-961-4454, international 1-210-312-4000</li>
	<li>Ticket: Create a ticket in the Cloud Control Panel from the Support menu</li>
</ul>

<p>Learn more about the Rackspace cloud service levels on the cloud service levels comparison page.</p>

<h3>What are the service access endpoints for Cloud Big Data?</h3>

<p>The Cloud Big Data service is a regionalized service. The user of the service is therefore responsible for appropriate replication, caching, and overall maintenance of Cloud Big Data data across regional boundaries to other Cloud Servers. The endpoints to use for your Cloud Big Data API calls are summarized in the following table:</p>

<table>
  <tr>
    <th>Region</th>
    <th>Endpoint</th>
  </tr>
  <tr>
    <td>Chicago (ORD)</td>
    <td><code>https://ord.bigdata.api.rackspacecloud.com/v1.0/yourAccountID/</code></td>
  </tr>
  <tr>
    <td>Dallas/Ft. Worth (DFW)</td>
    <td><code>https://dfw.bigdata.api.rackspacecloud.com/v1.0/yourAccountID/</code></td>
  </tr>
  <tr>
    <td>London (LON)</td>
    <td><code>https://lon.bigdata.api.rackspacecloud.com/v1.0/yourAccountID/</code></td>
  </tr>
  <tr>
    <td>Northern Virginia (IAD)</td>
    <td><code>https://iad.bigdata.api.rackspacecloud.com/v1.0/yourAccountID/</code></td>
  </tr>
</table>

<p>Replace the yourAccountID placeholder with your actual account number, which is returned as part of the authentication service response, after the final slash (/) in the <code>publicURL</code> field.</p>

<p>For Cloud Big Data v2, replace v1.0 with v2 in the service access URLs.</p>
