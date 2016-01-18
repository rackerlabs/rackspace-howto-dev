---
node_id: 4970
title: Cloud Servers - FAQ
type: article
created_date: '2015-12-01'
created_by: Rackspace Support
last_modified_date: '2016-01-15'
last_modified_by: Stephanie Fillmon
product: Cloud Servers
body_format: markdown_w_tinymce
---

<h2>Contents</h2>

<ul>
	<li><a href="#gettingStarted">Getting started</a>

	<ul>
		<li><a href="#howDoIinstallversionxy">I want to install version x.y of software in Linux, but your system doesn't allow me to? How do I install it?</a></li>
		<li><a href="#willyouhelpmeinstallmysoftwarpackage">Will you help me install my software package?</a></li>
		<li><a href="#doyousupportRubyPythonetc">Do you support Ruby/Python/(insert language or application here)?</a></li>
		<li><a href="#whataretheDNSservers">What are the DNS servers for my Cloud Server?</a></li>
		<li><a href="#howManyDomainscanIhost">How many domains can I host?</a></li>
		<li><a href="#newDifficult">I’m kind of new to this, will it be difficult?</a></li>
		<li><a href="#whatLevelofSupport">What level of support comes with Cloud Servers?</a></li>
		<li><a href="#whatCanIdowithaCloudServer">What can I do with a Cloud Server?</a></li>
		<li><a href="#canIReninstallandStartOver">Can I reinstall a different distribution or start over?</a></li>
		<li><a href="#whatIfIMessUp">What if I mess up my Cloud Server?</a></li>
	</ul>
	</li>
	<li><a href="#accountServices">Account services</a>
	<ul>
		<li><a href="#whatAreSecurityGroups">What are security groups?</a></li>
		<li><a href="#whereAretheDocs">Where are the docs?</a></li>
		<li><a href="#benefits">What are the benefits?</a></li>
		<li><a href="#whatisbeingLaunched">What is being launched?</a></li>
		<li><a href="#featuresSupportedatLaunch">What features are supported at launch?</a></li>
		<li><a href="/how-to/cloud-servers-faq">Are security groups on Cloud Networks supported?</a></li>
		<li><a href="#supportedNeutronClient">Will security groups be supported via the neutron client?</a></li>
		<li><a href="#supportedinControlPanel">Will this be integrated and available from within the Control Panel and Reach?</a></li>
		<li><a href="#supportedforOnmetal">Are security groups supported for OnMetal users?</a></li>
		<li><a href="#defaultSecurityGroup">Is there a default security group that gets applied to my instances?</a></li>
		<li><a href="#applyatBootTime">Can I apply security groups to ports on an instance at boot time?</a></li>
		<li><a href="#securityRuleAdded">What happens when a security group rule is added to the security group?</a></li>
		<li><a href="#trafficBlockedDenied">Can traffic be blocked or denied based on a security group rule?</a></li>
		<li><a href="#trafficPermittedAllowed">Is there any traffic that is permitted / allowed by default by security groups?</a></li>
		<li><a href="#trafficMatchedbySecurityGroupRules">What kinds of traffic can be matched by the security group rules?</a></li>
		<li><a href="#noRules">Can I have a security group with no rules?</a></li>
		<li><a href="#appliedtoInstances">Are security groups applied to instances?</a></li>
		<li><a href="#whataretheLimits">What are the limits for security groups and rules?</a></li>
	</ul>
	</li>
	<li><a href="#serverManagement">Server management</a>
	<ul>
		<li><a href="#doYouHostDNS">Do you host DNS?</a></li>
		<li><a href="#reverseDNS">How do I get reverse DNS setup for my Cloud Server?</a></li>
		<li><a href="#throughputLimit">Is there a throughput limit on my server's network interface card?</a></li>
		<li><a href="#internalIPs">Do you offer internal IPs?</a></li>
		<li><a href="#publicIPs">Can I buy extra public IPs?</a></li>
		<li><a href="#multpileServersfromSameImage">I would like to set up multiple servers from the same image. Can I do this?</a></li>
		<li><a href="#ondemandImages">Do you offer on-demand images (snapshots) and scheduled images and what are the prices?</a></li>
		<li><a href="#guiforLinux">I would like to use the GUI interface for my Linux Cloud Server. Is this possible?</a></li>
		<li><a href="#doYouhaveaControlPanel">Do you have a control panel?</a></li>
		<li><a href="#consoleAccess">Do you provide Console access?</a></li>
		<li><a href="#rebootMyMachine">Can I reboot my machine?</a></li>
		<li><a href="#billedifServerOff">Will I be billed if my server is powered off?</a></li>
		<li><a href="#powerServerBackOn">How do I power my server back on after shutting it down?</a></li>
		<li><a href="#whichDistros">Which distributions do you offer?</a></li>
		<li><a href="#upgradeLater">Can I upgrade down the road?</a></li>
		<li><a href="#usersPerMachine">How many users go onto each machine?</a></li>
		<li><a href="#CPUscheduling">How does the CPU scheduling work on Standard Next Generation servers?</a></li>
		<li><a href="#howlongforResize">How long does a standard Cloud Server resize take?</a></li>
		<li><a href="#extraStorage">Can I buy extra storage?</a></li>
	</ul>
	</li>
	<li><a href="#performance">Performance</a>
	<ul>
		<li><a href="#differencebetweenStandardandGeneral">What is the difference between Standard and General Purpose Cloud Servers?</a></li>
	</ul>
	</li>
	<li><a href="#billingandAccount">Billing and account</a>
	<ul>
		<li><a href="#discounts">Do you offer discounts for Cloud Servers?</a></li>
	</ul>
	</li>
	<li><a href="#support">Support</a>
	<ul>
		<li><a href="#trafficBlocked">Can I have traffic blocked or denied based on a Security Group rule?</a></li>
	</ul>
	</li>
	<li><a href="#security">Security</a>
	<ul>
		<li><a href="#addingSecurityRule">What happens when a Security Group rule is added to the Security Group?</a></li>
		<li><a href="#securityGroupsatBoot">Can I apply Security Groups to ports on an instance at boot time?</a></li>
		<li><a href="#defaultSecurityGroup">Is there a default Security Group that gets applied to my instances?</a></li>
		<li><a href="#securityGroupsOnMetal">Are Security Groups supported for OnMetal users?</a></li>
		<li><a href="#intrgratedinControlPanel">Will this be integrated and available to use via the Control Panel / Reach?</a></li>
		<li><a href="#supportedinNeutron">Will Security Groups be supported via Neutron client?</a></li>
		<li><a href="#securityGroupsonCloudNetworks">Are Security Groups on Cloud Networks supported?</a></li>
		<li><a href="#outboundSecurityGroups">Are Outbound Security Groups supported?</a></li>
		<li><a href="#securityGroupsfeaturesSupportedatLaunch">What features are supported at launch for Security Groups?</a></li>
		<li><a href="#securityGroupforAllCloudCustomers">Is the security group feature supported for all Cloud customers?</a></li>
		<li><a href="#securityGroupsforallPublicCloudusers">Is Security Groups available to all Rackspace Public Cloud users?</a></li>
		<li><a href="#benefitsofusingSecurityGroups">What are the benefits of using Security Groups?</a></li>
		<li><a href="#locationofDocsforSecurityGroups">Where are the docs for Security Groups?</a></li>
		<li><a href="#whatAreSecurityGroups">What are Security Groups?</a></li>
		<li><a href="#PCIDSScompliant">Are cloud servers PCI-DSS compliant?</a></li>
		<li><a href="#firewallonServer">Can I run a firewall on my server?</a></li>
		<li><a href="#numberofRulesperUserLimit">Is there a limit of number of rules per user?</a></li>
		<li><a href="#numberofRulesperGroupLimit">Is there a limit of number of rules per Security Group?</a></li>
		<li><a href="#securityGroupsperPort">How many Security Groups can I apply per port?</a></li>
		<li><a href="#securityGroupsappliedtoInstances">Are Security Groups applied to instances?</a></li>
		<li><a href="#securityGroupwithNoRules">Can I have a Security Group with no rules?</a></li>
		<li><a href="#kindsofTraffic">What kinds of traffic can be matched by the Security Group rules?</a></li>
		<li><a href="#trafficTypesDefaultforSecurityGroups">Is there any traffic that is permitted or allowed by default by Security Groups?</a></li>
		<li><a href="#maximumLimits">What are the maximum limits for the Cloud Servers service?</a></li>
		<li><a href="#secureDataDestruction">When a Cloud Server is deleted how is the data removed from the host server?</a></li>
	</ul>
	</li>
	<li><a href="#API">API</a>
	<ul>
		<li><a href="#whereareyourAPIs">Where are your APIs?</a></li>
	</ul>
	</li>
</ul>

<h2>- Getting started -<a id="gettingStarted" name="gettingStarted"></a></h2>

<h3>I want to install version x.y of software in Linux, but your system doesn't allow me to? How do I install it? <a id="howDoIinstallversionxy" name="howDoIinstallversionxy"></a></h3>

<p>Chances are that the repository for your operating system's package manager has an older approved version. This is fairly common, and you will need to remove that installation and then compile the newer version yourself. Refer to the software vendor for instructions.</p>

<h3>Will you help me install my software package?<a id="willyouhelpmeinstallmysoftwarpackage" name="willyouhelpmeinstallmysoftwarpackage"></a></h3>

<p>It depends on your service level. For Managed Infrastructure Cloud accounts, you are responsible for installing and maintaining all software on your server. Rackspace does provide support for specific software and server configurations on Cloud Servers with Managed Operations. For more information on supported systems and third party packages, see <a href="/how-to/cloud-servers-with-managed-operations-support-for-linux">Cloud Servers wih Managed Operations - Spheres of Support</a>.</p>

<h3>Do you support Ruby/Python/(insert language or application here)?<a id="doyousupportRubyPythonetc" name="doyousupportRubyPythonetc"></a></h3>

<p>All of our Cloud Servers can be configured as development stacks, database servers and web servers. Apache, Lighttpd and Mongrel, Visual Studio are all options.</p>

<p>You can use the programming language of your choice to interact with Cloud Servers. For help getting started with that, use any of the Software Development Kits (SDKs) documented at <a href="https://developer.rackspace.com/sdks/">https://developer.rackspace.com/sdks/</a>.</p>

<h3><span>What are the DNS servers for my Cloud Server?<a id="whataretheDNSservers" name="whataretheDNSservers"></a></span></h3>

<p><em>dns1.stabletransit.com</em> and <em>dns2.stabletransit.com</em></p>

<h3>How many domains can I host?<a id="howManyDomainscanIhost" name="howManyDomainscanIhost"></a></h3>

<p>This is a question familiar to those who use shared hosting. There is no limit, since you are in control of everything on your Cloud Server.</p>

<h3>I’m kind of new to this, will it be difficult?<a id="newDifficult" name="newDifficult"></a></h3>

<p>Maybe. That mostly depends on your experience as a Systems Administrator for Linux and/or Windows Server. Our Linux Cloud Servers are full Linux distributions with root-level access. Our Windows Cloud Servers give you Administrator access, and are built with nothing but the default applications on install. Cloud Servers are geared towards customers who want to start from scratch and tune a system for their own purposes.</p>

<p>If, after wearing the Systems Administrator hat for a while, you feel that you are out of your league - don't despair! We also offer Cloud Servers with a Managed Operations. Read here for more information on <a href="http://www.rackspace.com/cloud/managed_cloud/">Cloud Servers with Managed Operations</a>.</p>

<h3>What level of support comes with Cloud Servers?<a id="whatLevelofSupport" name="whatLevelofSupport"></a></h3>

<p>We have two Service Levels: <strong>Managed Infrastructure</strong> and <strong>Managed Operations</strong>. At the Managed Infrastructure level, we support the Cloud Server hardware, datacenter environment, and Internet connectivity - but do not support the software installed on your server, including the operating system and its configuration. When you provision a Cloud Server, you will be given a server with unrestricted access. The Managed Infrastructure support team will not assist in the installation of software or troubleshooting any kind of issue related to the software installed. We have some articles in the Knowledge Center covering basic installation of common applications. We also have community forums where you can share tips and tricks with other customers.</p>

<p>If you would like to have a <a href="/how-to/cloud-servers-with-managed-operations-support-for-linux">Managed Operations</a> on your Cloud Servers, we offer that service. This operations level provides additional support on Cloud Servers, which includes monitoring, operating system and application infrastructure layer support, and technical guidance.</p>

<h3>What can I do with a Cloud Server?<a id="whatCanIdowithaCloudServer" name="whatCanIdowithaCloudServer"></a></h3>

<p>Anything you want to (within the law and our <a href="http://www.rackspace.com/cloud/legal/aup/">Acceptable Use Policy</a>, of course)! The Rackspace Cloud Server solution is a fully unrestricted, root/Administrator level access, Linux or Windows environment. Any application or service that you can run from a traditional, physical, dedicated-unmanaged operations can be run from your Cloud Server.</p>

<h3>Can I reinstall a different distribution or start over?<a id="canIReninstallandStartOver" name="canIReninstallandStartOver"></a></h3>

<p>Of course you can! Simply press the <strong>Rebuild</strong> button in the Control Panel and you will be able to select a new distribution. Be sure you have a backup of your data because this process will destroy any data that is on the server. The rebuild process does allow you to save you IP address.</p>

<h3>What if I mess up my Cloud Server?<a id="whatIfIMessUp" name="whatIfIMessUp"></a></h3>

<p>You can <a href="/how-to/reboot-your-server">reboot your server</a>. You can <a href="/how-to/create-an-image-of-a-server-and-restore-a-server-from-a-saved-image">restore from a backup</a>. You can <a href="/how-to/deleting-your-server">delete your server</a> and start over. You can <a href="/how-to/rescue-mode">boot into an emergency rescue mode</a> and attempt fix the problem. There are many options for recovering from mistakes, but the easiest is to keep regular backups and to <a href="/how-to/best-practices-for-backing-up-your-data-cloud-block-storage-versus-cloud-backup">make a fresh backup</a> before attempting any major configuration changes or before installing new software.</p>

<h3><a href="/how-to/cloud-servers-faq">Back to Top</a></h3>

<h3 align="center">&nbsp;</h3>

<hr align="center" size="2" width="100%" />
<h2>Account services<a id="accountServices" name="accountServices"></a></h2>

<p><strong>Cloud Networks security groups</strong></p>

<h3>What are security groups?<a id="whatAreSecurityGroups" name="whatAreSecurityGroups"></a></h3>

<p><em>Security groups</em> are named collections of network access rules that&nbsp;enable Rackspace Public Cloud users to specify the types of traffic that are allowed to pass through PublicNet and ServiceNet ports on a Cloud Servers instance.&nbsp;A security group is a container for <em>security group rules</em>. After you launch an instance, you can assign one or more security groups to ports on that instance. &nbsp;Security groups act as a stateful firewall for your Cloud Server instances.</p>

<h3>Where is the documentation?<a id="whereAretheDocs" name="whereAretheDocs"></a></h3>

<p>Developer guide: <a href="http://docs.rackspace.com/networks/api/v2/cn-devguide/content/conceptSecurityGroups.html">http://docs.rackspace.com/networks/api/v2/cn-devguide/content/conceptSecurityGroups.html</a>&nbsp;</p>

<p>Getting started guide: <a href="http://docs.rackspace.com/networks/api/v2/cn-gettingstarted/content/security_groups.html">http://docs.rackspace.com/networks/api/v2/cn-gettingstarted/content/security_groups.html</a></p>

<h3>What are the benefits of using security groups? <a id="benefits" name="benefits"></a></h3>

<p>Prior to the release of this feature, users had to manage traffic to and from their instances individually via iptables rules (as an example) on every instance, or perhaps use third-party tools such as CloudPassage. Managing firewall policies involves significant overhead. Security groups make it possible to use a self-service API to define a common set of rules and apply them to the servers without needing to manage iptables rules on each server. Security groups simplify security policy administration for customers across their deployments.</p>

<h3>What is being launched? <a id="whatisbeingLaunched" name="whatisbeingLaunched"></a></h3>

<p>We are launching security groups as limited availability in all data centers, so customers can request the security groups feature and receive provisioned endpoints in their service catalog. Security groups are supported for Managed Infrastructure (non RackConnect) customers at launch.</p>

<h3>What features are supported at launch? <a name="featuresSupportedatLaunch"></a></h3>

<p>With the limited availability launch in early 2015, we support only inbound security groups on both PublicNet and ServiceNet interfaces. This means that customers can filter incoming traffic to their PublicNet and ServiceNet ports. We will add outbound security group support later in 2015.</p>

<h3>Are security groups on Cloud Networks supported? <a name="securityGroupsonCloudNetworks"></a></h3>

<p>Not at this time. We will add support later in 2015.</p>

<h3>Will security groups be supported via the neutron client? <a name="supportedNeutronClient"></a></h3>

<p>Yes. Users can provision security groups via the neutron client.</p>

<h3>Is this functionality integrated with and available from the Cloud Control Panel? <a name="supportedinControlPanel"></a></h3>

<p>Not yet. The product will be available soon. In the interim, you can use either the neutron client or the API.</p>

<h3>Are security groups supported for OnMetal users? <a name="supportedforOnmetal"></a></h3>

<p>No. We currently support security groups only for virtual cloud servers.</p>

<h3>Is a default security group applied to my instances? <a name="defaultSecurityGroup"></a></h3>

<p>No default security groups are applied. Users must create a security group themselves and apply it to ports on an instance.</p>

<h3>Can I apply security groups to ports on an instance at boot time? <a name="applyatBootTime"></a></h3>

<p>No. Security groups can be applied only after the instance is active.</p>

<h3>What happens when a security group rule is added to the security group? <a name="securityRuleAdded"></a></h3>

<p>Traffic that matches the new security group rule is allowed to go through.</p>

<h3>Can traffic be blocked or denied based on a security group rule? <a name="trafficBlockedDenied"></a></h3>

<p>No. Traffic that matches a rule is permitted, and any traffic that is not part of the ruleset for that security group is denied or blocked. Because of OpenStack API design requirements, you cannot specify that traffic matching a rule should be denied. The security groups API is a whitelist. &nbsp;Thus, traffic that doesn't match any of the rules in the whitelist is automatically blacklisted.</p>

<h2>Is there any traffic that is permitted or allowed by default by security groups<span>?</span> <a name="trafficPermittedAllowed"></a></h2>

<p>DNS responses from Rackspace Provider DNS servers (UDP source port 53) are allowed by default even if a security group does not explicitly allow them. Also the TCP flags ACK and RST are permitted by default.</p>

<h3>What kinds of traffic can be matched by the security group rules? <a id="trafficMatchedbySecurityGroupRules" name="trafficMatchedbySecurityGroupRules"></a></h3>

<p>The following types of traffic can be matched (for both IPv4 and IPv6 addresses):</p>

<ul>
	<li>TCP traffic</li>
	<li>UDP traffic</li>
	<li>ICMP traffic</li>
	<li>Traffic from a Source IP address</li>
	<li>Traffic from a CIDR</li>
</ul>

<p>&nbsp;</p>

<h3>Can I have a security group with no rules? <a name="noRules"></a></h3>

<p>Yes. Such a security group will deny or block all traffic.</p>

<h3>Are security groups applied to instances? <a name="appliedtoInstances"></a></h3>

<p>No. Security groups are applied to a Neutron port on a network that is attached to an instance and not to an instance itself.</p>

<h3>What are the limits for security groups and rules? <a name="whataretheLimits"></a></h3>

<p>You can apply up to 5 security groups per port.</p>

<p>You can have up to 20 security group rules per security group</p>

<p>You can have up to 100 security group rules (aggregate) per user during the limited availability release.</p>

<h3>Are Rackspace Cloud Servers HIPAA compliant? <a id="HIPAA compliant" name="HIPAA compliant"></a></h3>

<p>Rackspace cannot determine if a given customer is meeting their obligations under the laws applicable to them, and it remains our customers’ obligation to understand the laws applicable to their use of the services and select appropriate services to meet those obligations. We do understand the needs of many of our customers in the healthcare space to implement appropriate security measures to protect the sensitive information they work with.&nbsp;</p>

<p>To help customers in the healthcare industry meet their compliance requirements with regards to HIPAA, Rackspace offers a <a href="http://www.rackspace.com/information/legal/hipaabaa">Business Associate Agreement</a> in all of our dedicated hosting services segments, and it is included by default in our agreements with customers for those services.</p>

<h3>How does Cloud Servers handle my data from potentially becoming visible when I delete a server? <a id="handleMyDatafrombecomingVisilble" name="handleMyDatafrombecomingVisilble"></a></h3>

<p>For your security, the Virtual Hard Drive (VHD) on the hypervisor is deleted when you delete a server. Once it is deleted, data cannot be retrieved and customers do not have logical or direct access to the physical drive.</p>

<p>&nbsp;</p>

<h3>What are PVHVM images? <a id="whatarePVHVMimages" name="whatarePVHVMimages"></a></h3>

<p>PVHVM refers to the virtualization mode used by the hypervisor to run the virtual machine. PVHVM images are virtual machine images that use the PVHVM virtualization mode. In general, PVHVM offers better performance than PV, especially for disk and network IO, but is not well supported in Linux operating systems with a kernel version earlier than 2.6.36. The availability of PV and PVHVM images in the Rackspace Cloud is determined by the effectiveness of each virtualization mode for that particular operating system.</p>

<p><strong>Note</strong>: Work-optimized servers (Compute, I/O, and Memory) require PVHVM images. If you try to create a work-optimized server by using a non-PVHVM image, the following error message is displayed: <code>Image cannot be built with provided flavor</code>.</p>

<p>For more information about PVHVM, see <a href="/how-to/choosing-a-virtualization-mode-pv-versus-pvhvm">Choosing a Virtualization Mode (PV versus PVHVM)</a>.</p>

<h3>What do I enter in the Server Name field? <a id="whatdoIEnterinServerNameField" name="whatdoIEnterinServerNameField"></a></h3>

<p>The information that you enter in the <strong>Server Name </strong>field helps you identify this server in the API and Cloud Control Panel. The name that you enter when you create a server is used as the server’s host name. If you rename the server later, the name that is displayed in the API and Cloud Control Panel is updated. However, the host name on the computer is not updated.</p>

<p><strong>Can I connect to a server by using the server name?</strong></p>

<p>To connect to the server from outside of the server’s local network, you need to configure an A record in Cloud DNS. To access Cloud DNS, in the top navigation bar of the Cloud Control Panel, select <strong>Networking &gt; Cloud DNS</strong>.</p>

<p>&nbsp;For example, if you name your server <strong><a href="http://mywebserver1.myexampledomain.com/">MyWebServer1.MyExampleDomain.com</a></strong>, you must add an A record for <strong><a href="http://mywebserver1.myexampledomain.com/">MyWebServer1.MyExampleDomain.com</a> </strong>to your DNS zone (<a href="http://myexampledomain.com/">MyExampleDomain.com</a>) that points to the public IP address of the server. The information that you enter in the <strong>Server Name</strong> field helps you identify this server in the API and <a href="https://mycloud.rackspace.com/">Cloud Control Panel</a>.</p>

<p>&nbsp;</p>

<h3>Can I read your SLA?&nbsp;<a id="readSLA" name="readSLA"></a><span> </span><span>&nbsp;</span><span>&nbsp;</span><span>&nbsp;</span><span>&nbsp;</span><span>&nbsp;</span><span>&nbsp;</span><span>&nbsp;</span><span> </span></h3>

<p>&nbsp;</p>

<p>Sure, it's <a href="https://www.rackspace.com/information/legal/cloud/sla" title="Rackspace Cloud SLA">right here</a>.</p>

<h3>How do I contact Support? <a id="contactSupport" name="contactSupport"></a></h3>

<p>At Rackspace, our goal is to make the Cloud easy for you to use. To meet that goal, we have created many different ways for you to get the support that you need to get the most out of the Cloud.</p>

<ul>
	<li>Your first stop should be our <a href="/how-to/">Knowledge Center</a>, which is the best source for articles and tutorials to help you get the precise answers that you need.<br />
	&nbsp;</li>
	<li>The Knowledge Center contains the <a href="/how-to/">Getting Started with Cloud Servers Guide</a>, which provides you with the most important information that you need to set up a server.<br />
	&nbsp;</li>
	<li>Our <a href="https://community.rackspace.com/products/f/25">Open Cloud Forum</a> in the Rackspace Community is always open. Use the forum to get your questions answered by a Racker.<br />
	&nbsp;</li>
	<li>Do you have a quick question that you can't find an answer for in the Knowledge Center? Open Chat and talk with our Fanatical Support® staff anytime, 24x7x365.<br />
	&nbsp;</li>
	<li>Do you have a specialized Service Request or are you experiencing a problem with our service? Open a ticket. From the Rackspace <a href="http://mycloud.rackspace.com/">Cloud Control Panel</a>, select <strong>Support Tickets</strong> from the Account menu. Click <strong>Create Ticket</strong> to open a ticket directly with our support teams to report a problem or make a service request.<br />
	&nbsp;</li>
	<li>Call us 24x7x365 at 800 961 4454&nbsp;(toll-free) or +1 210 312 4000&nbsp;(international).</li>
</ul>

<p>&nbsp;</p>

<h3 align="center">&nbsp;</h3>

<hr align="center" size="2" width="100%" />
<h2>Server Management <a id="serverManagement" name="serverManagement"></a></h2>

<h3>Do you host DNS? <a id="doYouHostDNS" name="doYouHostDNS"></a></h3>

<p>Yes. Our Control Panel has a DNS menu for maintaining domain records for your Cloud Servers. Read this article for <a href="/how-to/create-dns-records-for-cloud-servers-with-the-control-panel">detailed information on using the Rackspace Cloud DNS Control Panel</a>.</p>

<h3>How do I get reverse DNS setup for my Cloud Server? <a id="reverseDNS" name="reverseDNS"></a></h3>

<p>You can setup reverse DNS from your control panel. This article will show you how:<a href="/how-to/create-a-reverse-dns-record-0" title="/knowledge_center/index.php/DNS_-_Creating_a_Reverse_DNS_Record">DNS - Creating a Reverse DNS Record.</a></p>

<h3>Is there a throughput limit on my server's network interface card? <a id="throughputLimit" name="throughputLimit"></a></h3>

<p>The amount of network throughput varies based on the Cloud Server flavor. &nbsp;For more details, see&nbsp;<a href="http://www.rackspace.com/cloud/public-pricing/#cloud-servers" target="_blank">here</a>.</p>

<h3><span>Do you offer internal IPs? <a id="internalIPs" name="internalIPs"></a></span></h3>

<p>Yes. Each server comes with an internal IP address that is used to communicate between servers. The traffic that flows over this interface (eth1) on your server is unmetered and is not billed. This network is also referred to as ServiceNet. ServiceNet is an internal only, multi-tenant network connection within each Rackspace datacenter. ServiceNet IPs are not accessible from the public Internet and are local per datacenter.</p>

<h3><span>Can I buy extra public IPs? <a id="publicIPs" name="publicIPs"></a></span></h3>

<p>Yes.&nbsp; For more informaton on the IP request process, see <a href="/how-to/requesting-additional-ipv4-addresses-for-cloud-servers">Requesting Additional IPv4 Addresses for First and Next Generation Cloud Servers</a>.</p>

<h3><span>I would like to set up multiple servers from the same image. Can I do this? <a id="multpileServersfromSameImage" name="multpileServersfromSameImage"></a></span></h3>

<p>As a Cloud Servers customer, you have access to create both on-demand images and scheduled images of your cloud server. All Cloud Server images will be stored in your Cloud Files account. This enables you to keep these images even after the Cloud Server they were created on is deleted. It also allows the flexibility to create an unlimited number of on-demand images of your Cloud Server. All Cloud Server images can be used to create new Cloud Servers or restore an existing Cloud Server. For details, see <a href="/how-to/create-an-image-of-a-server-and-restore-a-server-from-a-saved-image">Creating an Image of Your Performance Flavor Server with the Control Panel</a>.</p>

<h3><span>Do you offer on-demand images (snapshots) and scheduled images and what are the prices? <a id="ondemandImages" name="ondemandImages"></a></span></h3>

<p>You can create an image of any General Purpose&nbsp;Cloud Server, and you can use this image to restore a server or clone a new one. You can create an unlimited number of images on-demand, or you can schedule an automatic daily or weekly image.</p>

<p>Images will be compressed and stored on Rackspace Cloud Files at the <a href="http://www.rackspace.com/cloud/cloud_hosting_products/files/pricing/">current storage rates</a>. Please also read this list of <a href="/how-to/rackspace-cloud-essentials-cloud-server-image-limitations">Snapshot Limitations</a>.</p>

<p>If using a virtual cloud server, see <a href="/how-to/create-an-image-of-a-server-and-restore-a-server-from-a-saved-image">Creating an image of your General Purpose Cloud Server with the control panel</a> for more information on the image options associated with virtual cloud servers.</p>

<h3><span>I would like to use the GUI interface for my Linux Cloud Server. Is this possible? <a id="guiforLinux" name="guiforLinux"></a></span></h3>

<p>Yes it is! An article on how to install VNC and X-Windows is located here: <a href="/how-to/vnc-install" title="VNC Install">VNC Install</a>. Keep in mind that this will use up a large amount of bandwidth on your server.</p>

<h3><span>Do you have a control panel? <a id="doYouhaveaControlPanel" name="doYouhaveaControlPanel"></a></span></h3>

<p>Yes, the Rackspace <a href="https://mycloud.rackspace.com/">Cloud Control Panel</a> is a web-based management interface for restarting your cloud server, starting support discussions, viewing stats, and scheduling snapshots. However, we do not offer a control panel like Plesk or cPanel. You’re free to install such packages for your own cloud server.</p>

<p>You may be interested in installing the free monitoring agent on your server and using the <a href="https://intelligence.rackspace.com/">Cloud Intelligence dashboard</a>, which offers many of the same functions as a control panel.</p>

<h3><span>Do you provide Console access? <a id="consoleAccess" name="consoleAccess"></a></span></h3>

<p>Yes, via a Java web terminal accessible through the Details section of each webserver, in the Actions menu under the section labeled Manage, you will see a link to Connect Via Terminal.&nbsp;</p>

<p><b>Note</b>: Console access is via a secure HTTP connection which is different connection from the traditional way to connect via SSH for Linux or RDP for Windows. Console can be a useful troubleshooting tool if your server is unresponsive or you have locked yourself out.</p>

<h3><span>Can I reboot my machine? <a id="rebootMyMachine" name="rebootMyMachine"></a></span></h3>

<p>Yes. All Cloud Servers can perform both soft (reset button) and hard (power cycle) reboots. These are performed instantly and handled via the Cloud Server Control Panel.</p>

<h3><span>Will I be billed if my server is powered off? <a id="billedifServerOff" name="billedifServerOff"></a></span></h3>

<p>Yes. You will be billed for the resources that are used on the host while your server is in the <strong>Active</strong> status. When your server is created, you are given a dedicated amount of RAM and hard drive space. As long as your server exists, no one else will be able to use those resources that have been allocated to you - this is why you are billed per hour even while powered off. If you would like to stop incurring charges for a given server, you must delete that server in the Control Panel.</p>

<p>If you want to stop paying for a server, but still need to retain the configurations from it, your best option is to <a href="/how-to/create-an-image-of-a-server-and-restore-a-server-from-a-saved-image">create an image</a> of the Cloud Server. Your system configurations on your system disk will be preserved in the image. The image will be saved in Cloud Files and accessible through the Saved Images tab in the Control Panel. There is a fee associated with Cloud Files storage but it is much less than the cost of an active server. You will also need to save the data from your data disk out to Cloud Block Storage or Rackspace Cloud Backup to have available on your next server. Then you will be free to delete the original server, safe in the knowledge that you can always provision a new server using the saved image of your old server and you saved data.&nbsp; After restoring your server from the saved image, the primary difference will be that your new server has a different IP address from the old one. Putting the new server into production may require you to update any associated DNS records to reflect the new IP address.</p>

<h3><span>How do I power my server back on after shutting it down? <a id="powerServerBackOn" name="powerServerBackOn"></a></span></h3>

<p>Please see the following article: <a href="/how-to/reboot-your-server" title="Shutting Down and Restarting a Cloud Server">Shutting Down and Restarting a Cloud Server</a></p>

<h3><span>Which distributions do you offer? <a id="whichDistros" name="whichDistros"></a></span></h3>

<p>The Features section of our <a href="http://www.rackspace.com/cloud/servers/">product page</a> has information regarding the Linux distributions and Windows operating systems that we have available.</p>

<h3><span>Can I upgrade down the road? <a id="upgradeLater" name="upgradeLater"></a></span></h3>

<p>Yes.&nbsp; With General Purpose&nbsp;Cloud Servers, you can change the size of your data storage space in one of two ways:</p>

<ul type="disc">
	<li class="MsoNormal"><span>Increase Available Storage with Cloud Block Storage. For more information on Cloud Block Storage, see <a href="/how-to/create-and-attach-a-cloud-block-storage-volume">Create and Attach a Cloud Block Storage Volume</a>.</span></li>
	<li class="MsoNormal"><span>Migrate to a larger size server with more RAM, disk space, and vCPUs. For&nbsp; more information on resizing, see <a href="/how-to/upgrading-resources-for-general-purpose-or-io-optimized-cloud-servers">Changing the Size of Your First Generation Cloud Server</a>.</span></li>
</ul>

<h3><span>How many users go onto each machine? <a id="usersPerMachine" name="usersPerMachine"></a></span></h3>

<p>The number of customers on a Cloud Server host machine depends on the size of the customers’ Cloud Servers, and the type of operating system.</p>

<h3><span>How does the CPU scheduling work on Standard Next Generation servers? <a id="CPUscheduling" name="CPUscheduling"></a></span></h3>

<p><strong>Note</strong>: <a href="/how-to/new-features-in-general-purpose-and-work-optimized-cloud-servers" target="_blank">General Purpose Cloud Servers</a> have specific virtual CPU allocations, as detailed on the <a href="http://www.rackspace.com/cloud/servers/pricing/">Cloud Servers pricing page</a>. &nbsp;The following information on CPU scheduling applies only to next-generation standard (for example, not General Purpose) Cloud Servers.</p>

<p>For Windows images, each Cloud Server is assigned a number of virtual cores based on the size of the Cloud Server. The Standard 1 GB Cloud Server receives 1 virtual core, the standard 2 GB and 4 GB Cloud Servers receive 2 virtual cores, the standard 8 GB and 15.5 GB Cloud Servers receive 4 virtual cores, and the standard 30GB servers receive 8 virtual cores. Each of these cores is given equal weight when allocating CPU cycles.</p>

<p>For Linux distributions, each Standard Cloud Server is assigned the number of virtual cores and the CPU cycles allocated to these cores, as selected when creating the server in the Control Panel.</p>

<p>All standard Cloud Servers receive a guaranteed minimum amount of CPU cycles with the ability to burst when excess cycles are available.</p>

<h3><span>How long does a standard Cloud Server resize take? <a id="howlongforResize" name="howlongforResize"></a></span></h3>

<p>The amount of time a resize takes varies by the size of the server and the time of day you are performing the resize. If you have a brand-new server with no additional data or software installed, then you might be looking at 10 minutes. However, if you have data installed on your server and have been installing software then it can take up to 30 minutes or more. Peak times for resize activity tend to be at the start and end of the business day. Expect a short period of downtime while your server is being resized.</p>

<p>Note also that resizing a server down can take longer than resizing up because the system needs to consolidate and copy data to a smaller disk container rather than expand the existing container. &nbsp;Cleaning up unneeded files (like old logs and session files) can improve the speed of a resize operation.</p>

<p>There are different processes of resizes, as follows:</p>

<ul type="disc">
	<li class="MsoNormal"><strong><span>Online Resizes</span></strong><span>:&nbsp; Allow for the original sized Cloud Server to be powered on during the "Prep-Resize" step, and only powers down during the second step of the resize process.<br />
	This includes: &nbsp;First Generation Server&nbsp;resize up and resize down, and Standard resize up.</span></li>
	<li class="MsoNormal"><strong><span>Offline Resizes</span></strong><span>: Power down as the first "Prep-Resize" step.<br />
	This includes:&nbsp; Standard resize down.</span></li>
</ul>

<p><strong>NOTE: Resizing is not available for workload-optimized Cloud Servers. For information on your available options, see <a href="/how-to/upgrading-resources-for-general-purpose-or-io-optimized-cloud-servers">Changing the size of your workload-optimized Cloud Server</a>.</strong></p>

<h3><span>Can I buy extra storage? <a id="extraStorage" name="extraStorage"></a></span></h3>

<p>While the native storage allocation for a Cloud Server is based on the Cloud Server flavor that you select, you can also add extra storage at any time with our <a href="http://www.rackspace.com/cloud/blockstorage/">Cloud Block Storage</a> service.</p>

<h3 align="center">&nbsp;</h3>

<hr align="center" size="2" width="100%" />
<h2><span>Performance <a id="performance" name="performance"></a></span></h2>

<h3><span>What is the difference between Standard and General Purpose Cloud Servers? <a id="differencebetweenStandardandGeneral" name="differencebetweenStandardandGeneral"></a></span></h3>

<p>There are several noteworthy differences between Standard and General Purpose Cloud Servers:</p>

<ul type="disc">
	<li class="MsoNormal"><span>General Purpose Cloud Servers use faster solid state drives (SSD) compared to the standard spinning disk allocation for Standard Cloud Servers.</span></li>
	<li class="MsoNormal"><span>Up to 120 GB of RAM is available on General Purpose servers, whereas Standard Servers provide up to 30 GB of RAM.</span></li>
	<li class="MsoNormal"><span>You can have up to 32 vCPUs running on General Purpose Cloud Servers, comapred to the maximum of 8 on the Standard Cloud Servers.</span></li>
	<li class="MsoNormal"><span>Maximum network bandwidth on Standard Cloud Servers is 300 Mbps public network and 600 Mbps private network. Maximum network bandwidth on General Purpose Cloud Servers is 10,000 Mbps to divide between public and private networks as you choose..</span></li>
</ul>

<p>For more information about General Purpose Cloud Servers, see <a href="/how-to/new-features-in-general-purpose-and-work-optimized-cloud-servers">What is new with&nbsp;General Purpose Cloud Servers</a>.</p>

<h3 align="center">&nbsp;</h3>

<hr align="center" size="2" width="100%" />
<h2><span>Billing and Account <a id="billingandAccount" name="billingandAccount"></a></span></h2>

<h3><span>Do you offer discounts for Cloud Servers? <a id="discounts" name="discounts"></a></span></h3>

<p>Yes. We offer different types of discounts based on usage. Please see the <a href="http://www.rackspace.com/cloud/servers/discounts/">Cloud Servers discounts page</a> for details.</p>

<h3 align="center">&nbsp;</h3>

<hr align="center" size="2" width="100%" />
<h2><span>Support <a id="support" name="support"></a></span></h2>

<h3><span>Can I have traffic blocked or denied based on a Security Group rule? <a id="trafficBlocked" name="trafficBlocked"></a></span></h3>

<p class="MsoNormal"><span class="field-content"><span>&nbsp;</span></span></p>

<p class="MsoNormal"><span>Traffic that matches a rule is permitted. Any traffic that is not part of the ruleset for that Security Group is denied / blocked. There is no way to specify that traffic matching a rule should be denied. This is how the OpenStack Security Groups API was designed. Hence the Security Groups API is a white-list. &nbsp;Traffic that doesn't match any of the rules in the white-list is automatically black-listed.</span></p>

<h3 align="center">&nbsp;</h3>

<hr align="center" size="2" width="100%" />
<h2><span>Security <a id="security" name="security"></a></span></h2>

<h3><span>What happens when a Security Group rule is added to the Security Group? <a id="addingSecurityRule" name="addingSecurityRule"></a></span></h3>

<p>Traffic matching a Security Group rule is allowed to go through.</p>

<h3><span>Can I apply Security Groups to ports on an instance at boot time? <a id="securityGroupsatBoot" name="securityGroupsatBoot"></a></span></h3>

<p>No. Security Groups can only be applied after the instance is active.</p>

<h3><span>Is there a default Security Group that gets applied to my instances? <a id="defaultSecurityGroup" name="defaultSecurityGroup"></a></span></h3>

<p>No, there is no default security Group that gets applied. Users have to create a Security Group themselves and apply them to ports on an instance.</p>

<h3><span>Are Security Groups supported for OnMetal users? <a id="securityGroupsOnMetal" name="securityGroupsOnMetal"></a></span></h3>

<p>No, Security Groups are currently only supported for Virtual Cloud servers.</p>

<h3><span>Will this be integrated and available to use via the Control Panel / Reach? <a id="intrgratedinControlPanel" name="intrgratedinControlPanel"></a></span></h3>

<p>The product will be available via Control panel very soon. In the interim, customers can use either the Neutron client or the API.</p>

<h3><span>Will Security Groups be supported via Neutron client? <a id="supportedinNeutron" name="supportedinNeutron"></a></span></h3>

<p>Yes. Users can provision security groups via Neutron client.</p>

<h3><span>Are Security Groups on Cloud Networks supported? <a id="securityGroupsonCloudNetworks" name="securityGroupsonCloudNetworks"></a></span></h3>

<p>No.&nbsp;Rackspace will add Security Group support for Cloud Networks&nbsp;in the near future.</p>

<h3><span>Are Outbound Security Groups supported? <a id="outboundSecurityGroups" name="outboundSecurityGroups"></a></span></h3>

<p>No.&nbsp;Rackspace will add Outbound security Group support in the near future.</p>

<h3><span>What features are supported at launch for Security Groups? <a id="securityGroupsfeaturesSupportedatLaunch" name="securityGroupsfeaturesSupportedatLaunch"></a></span></h3>

<p>Inbound Security Groups on PublicNet and ServiceNet interfaces are supported. This means customers can filter incoming traffic to their PublicNet and ServiceNet ports.</p>

<h3><span>Is the security group feature supported for all Cloud customers? <a id="securityGroupforAllCloudCustomers" name="securityGroupforAllCloudCustomers"></a></span></h3>

<p>Security Groups will only be supported for Managed Infrastructure, non-RackConnect customers at launch.</p>

<h3><span>Is Security Groups available to all Rackspace Public Cloud users? <a id="securityGroupsforallPublicCloudusers" name="securityGroupsforallPublicCloudusers"></a></span></h3>

<p>Security Grouos is in&nbsp;Limited Availability in all Data Centers. Please contact Rackspace support to enable this feature.</p>

<h3><span>What are the benefits of using Security Groups? <a id="benefitsofusingSecurityGroups" name="benefitsofusingSecurityGroups"></a></span></h3>

<p>Prior to this feature being available, customers had to manage traffic to/from their instances individually via (for example) ipTables rules on every instance (or perhaps use 3rd party tools). Managing firewall policies involves in a distributed fashion&nbsp;significant overhead to keep track of and manage. Security Groups makes it possible to use self-service API to define a common set of rules and apply them to the Neutron ports (Public/ServiceNet) on Cloud Servers&nbsp;without needing to tweak iptables rules on each server, thereby simplifying administration of security policies.</p>

<h3><span>Where are the docs for Security Groups? <a id="locationofDocsforSecurityGroups" name="locationofDocsforSecurityGroups"></a></span></h3>

<p>Security Groups concepts and introduction :&nbsp;<a href="http://docs.rackspace.com/networks/api/v2/cn-devguide/content/api_ext_security_neutron.html">http://docs.rackspace.com/networks/api/v2/cn-devguide/content/api_ext_security_neutron.html</a></p>

<p>API Guide:&nbsp;<a href="http://docs.rackspace.com/networks/api/v2/cn-devguide/content/api_ext_security_neutron.html">http://docs.rackspace.com/networks/api/v2/cn-devguide/content/api_ext_security_neutron.html</a></p>

<p>Getting Started:&nbsp;<a href="http://docs.rackspace.com/networks/api/v2/cn-gettingstarted/content/security_groups.html">http://docs.rackspace.com/networks/api/v2/cn-gettingstarted/content/security_groups.html</a></p>

<h3><span>What are Security Groups? <a id="whatAreSecurityGroups" name="whatAreSecurityGroups"></a></span></h3>

<p>Security groups are a&nbsp;named collection of network access rules that&nbsp;provide Rackspace Public Cloud users the ability to specify the types of traffic that are allowed to pass through, to and from ports (Public/ServiceNet) on a Cloud server instance.&nbsp;A security group is a container for security group rules.&nbsp;After you launch an instance, you can assign one or more security groups to ports on that instance. &nbsp;Security Groups act as a stateful firewall for your cloud server instances.</p>

<h3><span>Are cloud servers PCI-DSS compliant? <a id="PCIDSScompliant" name="PCIDSScompliant"></a></span></h3>

<p>The Rackspace Cloud environment has not been formally&nbsp;assessed for for compliance with the Payment Card Industry (PCI) Data Security Standard (DSS).&nbsp; For information about PCI-DSS, see <a href="http://www.rackspace.com/security/solutions/#pci">Cloud Security Solutions</a>. For information about PCI-DSS when using Rackspace Dedicated Hosting services, see <a href="http://www.rackspace.com/ecommerce-hosting/pci/">PCI-Compliant Hosting for E-commerce Websites</a>.</p>

<h3><span>Can I run a firewall on my server? <a id="firewallonServer" name="firewallonServer"></a></span></h3>

<p>Definitely and we encourage it! Each Linux server is capable of running the Linux-standard firewall called <strong>iptables</strong>- some even have it pre-configured! Other firewall systems have been tested on Cloud Servers as well.</p>

<h3><span>Is there a limit of number of rules per user? <a id="numberofRulesperUserLimit" name="numberofRulesperUserLimit"></a></span></h3>

<p>There is an aggregate limit of 100 security Group rules per user during Limited Availability. Please contact Rackspace support&nbsp;if you need this limit raised.</p>

<h3><span>Is there a limit of number of rules per Security Group? <a id="numberofRulesperGroupLimit" name="numberofRulesperGroupLimit"></a></span></h3>

<p>There is a limit of 20 security Group rules per Security Group.&nbsp;Please contact Rackspace support&nbsp;if you need this limit raised.</p>

<h3><span>How many Security Groups can I apply per port? <a id="securityGroupsperPort" name="securityGroupsperPort"></a></span></h3>

<p>Up to 5 security Groups are allowed per port.&nbsp;Please contact Rackspace support&nbsp;if you need this limit raised.</p>

<h3><span>Are Security Groups applied to instances? <a id="securityGroupsappliedtoInstances" name="securityGroupsappliedtoInstances"></a></span></h3>

<p>Security Groups are applied to Neutron ports (PublicNet and ServiceNet) on Cloud Server&nbsp;instances.</p>

<h3><span>Can I have a Security Group with no rules? <a id="securityGroupwithNoRules" name="securityGroupwithNoRules"></a></span></h3>

<p>Yes. Such a Security Group will deny/ block all traffic.</p>

<h3><span>What kinds of traffic can be matched by the Security Group rules? <a id="kindsofTraffic" name="kindsofTraffic"></a></span></h3>

<p>TCP, UDP, ICMP traffic can be matched in addition to traffic from a Source IP address or CIDR. Both IPv4 and IPv6 traffic can be matched.</p>

<h3><span>Is there any traffic that is permitted or allowed by default by Security Groups? <a id="trafficTypesDefaultforSecurityGroups" name="trafficTypesDefaultforSecurityGroups"></a></span></h3>

<p>DNS responses from Rackspace Provider DNS servers (UDP source port 53 ) are allowed by default even if they are not explicitly allowed by a Security Group.</p>

<p>Also TCP flags ACK and RST are permitted by default.</p>

<h3>What are the maximum limits for the Cloud Servers service? <a id="maximumLimits" name="maximumLimits"></a></h3>

<p>The maximum limits are as follows:</p>

| Limit Name | Description | Value |
| ---------- | ----------- | ----- |
| maxImageMeta | The maximum number of metadata key value pairs associated with a particular image. | 40 |
| maxPersonality | The maximum number of file path/content pairs that can be supplied when a server is built or rebuilt. | 5 |
| maxPersonalitySize | The maximum size, in bytes, for each personality file. | 1000 |
| maxServerMeta | The maximum number of metadata key value pairs associated with a particular server. | 40 |
| maxTotalCores | This limit is disabled, so no limits exist on the total number of cores. | -1 |
| maxTotalInstances | The maximum number of cloud servers that can exist in your account at any one time. | 100 |
| maxTotalPrivateNetworks | The maximum number of isolated networks that you can create. Set to **0** when Cloud Networks is disabled, **10** when Cloud Networks enabled. |  10 |
| maxTotalRAMSize | The maximum total amount of RAM (MB) of all cloud servers in your account at any one time. | 131072 |

<h3 align="center">&nbsp;</h3>

<h3>When a Cloud Server is deleted how is the data removed from the host server?&nbsp;<a id="secureDataDestruction" name="secureDataDestruction"></a></h3>

<ul>
	<li>First Generation Cloud Servers on xen classic use LVM storage.&nbsp; As such, when a server is deleted it is scrubbed by writing 0's over the partition.</li>
	<li>Next Generation Cloud Servers use VHD storage.&nbsp; Once a server is deleted the VHD is deleted, similar to the way you would do a rm command in Linux.&nbsp; When that is done the VHD is completely removed thus allowing another one to be created.</li>
</ul>

<hr align="center" size="2" width="100%" />
<h2><span>API <a id="API" name="API"></a></span></h2>

<h3><span>Where are your APIs? <a id="whereareyourAPIs" name="whereareyourAPIs"></a></span></h3>

<p>You can find the documentation for the API for Cloud Servers and our other products on&nbsp;our <a href="http://docs.rackspace.com/">API documentation website</a>.</p>

<p>Before you can start using our APIs, you will need your API Key.&nbsp;You can obtain your API key by following the instructions in our article, <a href="/how-to/view-and-reset-your-api-key">Viewing and Regenerating Your API Key</a>.</p>

<p class="MsoNormal">&nbsp;</p>
