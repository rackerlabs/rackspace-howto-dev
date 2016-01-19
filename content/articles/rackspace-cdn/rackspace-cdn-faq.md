---
node_id: 4705
title: Rackspace CDN FAQ
type: article
created_date: '2015-06-08'
created_by: Rackspace Support
last_modified_date: '2016-01-19'
last_modified_by: Stephanie Fillmon
product: Rackspace CDN
body_format: markdown_w_tinymce
---

<p>Get quick answers to common questions about the Rackspace CDN service. If you have any questions about the terms used in this FAQ, see the <a href="/how-to/rackspace-cdn-terminology">Rackspace CDN terminology</a> page.</p>

<h2>Getting Started</h2>

<h3>How does Rackspace CDN benefit my website or web application?</h3>

<p>Benefits include fast load times when serving your content, access control, and origin protection. For detailed information, see <a href="/how-to/features-of-rackspace-cdn">Features of Rackspace CDN</a>.</p>

<h3>How many edge servers does Rackspace CDN give me access to?</h3>

<p>When you use Rackspace CDN, you have access to over 230 edge nodes (servers) around the world.&nbsp; &nbsp;</p>

<h3>Can I specify certain files for caching or create specific inclusions and exclusions?</h3>

<p>Yes, you can set a time to live (TTL) of 0 on any content that you don't want served from an edge node. You might choose to do this for dynamic content that changes for every visitor. &nbsp;</p>

<h3>How can I check the performance of my site?</h3>

<p>Many web browser plugins and tools are available. For example:</p>

<ul>
	<li>In Firefox, click <strong>Tools</strong> &gt; <strong>Web Developer</strong> &gt; <strong>Network</strong>.<br />
	If you don't see the <strong>Tools</strong> menu, press the <strong>F10</strong> key on your keyboard.</li>
	<li>In Chrome, you can use the <a href="https://chrome.google.com/webstore/detail/page-load-time/fploionmjgeclbkemipmkogoaohcdbig?hl=en" target="_blank">Page load time plugin</a></li>
</ul>

<p>Additionally, some customers use YSlow or Pingdom.</p>

<h3>Can I push content to edge nodes before it's needed?</h3>

<p>No. Rackspace CDN does not prepopulate the edge nodes. Content is copied to the edge nodes only when it is requested.</p>

<h3>How does origin pull work?</h3>

<p>Rackspace CDN seamlessly and automatically fetches content from an origin server and caches it at the edge location if the edge location doesn’t already have it.</p>

<h3>Can content be pulled from anywhere, including sources external to Rackspace?</h3>

<p>Yes. Rackspace CDN can pull content from any origin with a public IP address or web address, including servers hosted in our public, private, or dedicated infrastructures, as well as servers hosted offsite.</p>

<h3>What are my options for serving traffic over HTTPS?</h3>

<p>Rackspace CDN works with shared domain SSL, SSL SAN certificates, and fully owned certificates. Our custom SSL options satisfy your security, budget, and marketing requirements. Pricing for each option is different.</p>

---------
<h2>General</h2>

<h3>Is there a service level agreement (SLA) for Rackspace CDN?</h3>

<p>Yes. It is located at <a href="http://www.rackspace.com/information/legal/service-level-guarantee-rackspace-cdn">Rackspace CDN SLA</a>.</p>

<h3><a id="Pricing information" name="Pricing information"></a>Can you provide pricing information for Rackspace CDN?</h3>

<p>See <a href="http://www.rackspace.com/cloud/cdn-content-delivery-network">Rackspace CDN pricing</a>.</p>

<p><sup><a href="#top">back to top</a></sup></p>

<h3><a id="certificate authorities" name="certificate authorities"></a>Is there a list of approved Certificate Authorities (CAs) for Rackspace CDN?</h3>

<p>Yes. See <a href="/how-to/rackspace-cdn-secure-delivery-options#Secure%2520origin">Rackspace CDN secure delivery options</a>.</p>

<h3>Will I be charged for edge node storage when I use Rackspace CDN?</h3>

<p>No. You are charged for storage on your origin server, but Rackspace CDN does not charge for edge node storage on top of that.</p>

<h3>Does Rackspace CDN honor the Expires header value set by the origin server (web server)?</h3>

<p>If the content is cacheable and you have <em>not</em> set a time to live (TTL) rule on the service, edge nodes honor the Expires or Cache Control headers sent by the origin server. When a request is made to the origin for content, the edge node looks for Expires or Cache Control headers in the response sent by the origin. If these headers are present, the TTL for that content matches the time referenced in the Expires or Cache Control headers. If both Expires and Cache Control headers are present, Cache Control takes precedence.</p>

<p>If the content is cacheable and you have set a TTL on the service, the caching TTL is honored. The Cache Control and Expires headers are ignored, and content is refreshed based on the TTL value that you set. This rule applies only to content that matches the path specified in the TTL rule. For example, if you have a TTL rule for the page <strong>/images/*</strong>, then all Expires and Cache Control headers for content that is <em>not</em> in the <strong>images</strong> directory is honored.</p>

<p>If the content is not cacheable, it is not cached on the edge nodes, regardless of the origin headers.</p>

<p><strong>Note</strong>: A default caching rule with a TTL of 1 day and a request_url of /* is set for all content. You need to remove your default caching in order to hone origin headers.</p>

<h3>What is cacheable content?</h3>

<p>Content with the following file extensions is cacheable:</p>

<p>aif, aiff, au, avi, bin, bmp, cab, carb, cct, cdf, class, css, doc, dcr, dtd, exe, flv, gcf, gff, gif, grv, hdml, hqx, ico, ini, jpeg, jpg, js, mov, mp3, nc, pct, pdf, png, ppc, pws, swa, swf, txt, vbs, w32, wav, wbmp, wml, wmlc, wmls, wmlsc, xsd, zip, webp, jxr, hdp, wdp</p>

<h3>Does Rackspace CDN support Service Name Indication (SNI)?</h3>

<p>SNI is not currently supported.</p>

<h3>Does Rackspace CDN have a free secure delivery option?</h3>

<p>Yes, customers who use the shared Rackspace domain will not be charged any certificate fees.</p>

<h3>What is the process for requesting a dedicated certificate?</h3>

<p>Customers need to submit a ticket from the Control Panel with their domain details and Rackspace Support will reach out to them.</p>

<h3>What should customers expect after they provision a certificate?</h3>

<p>The administrator for the domain will be contacted by GeoTrust to verify the domain. It is critical that customers respond to this verification request. Certificates will not be provisioned until it is complete.</p>
