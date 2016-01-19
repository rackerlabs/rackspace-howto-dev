---
node_id: 4970
title: Cloud Servers - FAQ
type: article
created_date: '2015-12-01'
created_by: Rackspace Support
last_modified_date: '2016-01-19'
last_modified_by: Stephanie Fillmon
product: Cloud Servers
body_format: markdown_w_tinymce
---

<h2>- Getting started -</h2>

<h3>I want to install version x.y of software in Linux, but your system doesn't allow me to? How do I install it?</h3>

<p>Chances are that the repository for your operating system's package manager has an older approved version. This is fairly common, and you will need to remove that installation and then compile the newer version yourself. Refer to the software vendor for instructions.</p>

<h3>Will you help me install my software package?</h3>

<p>It depends on your service level. For Managed Infrastructure Cloud accounts, you are responsible for installing and maintaining all software on your server. Rackspace does provide support for specific software and server configurations on Cloud Servers with Managed Operations. For more information on supported systems and third party packages, see <a href="https://www.rackspace.com/knowledge_center/article/cloud-servers-with-managed-service-level-spheres-of-support">Cloud Servers with Managed Operations - Spheres of Support</a>.</p>

<h3>Do you support Ruby/Python/(insert language or application here)?</h3>

<p>All of our Cloud Servers can be configured as development stacks, database servers and web servers. Apache, Lighttpd and Mongrel, Visual Studio are all options.</p>

<p>You can use the programming language of your choice to interact with Cloud Servers. For help getting started with that, use any of the Software Development Kits (SDKs) documented at <a href="https://developer.rackspace.com/sdks/">https://developer.rackspace.com/sdks/</a>.</p>

<h3>Do you host DNS?</h3>

<p>Yes. Our Control Panel has a DNS menu for maintaining domain records for your Cloud Servers. See <a href="https://www.rackspace.com/knowledge_center/article/create-dns-records-for-cloud-servers-with-the-control-panel">Create DNS records for Cloud Servers with the Control Panel</a> for more information.</p>

<h3>What are the DNS servers for my Cloud Server?</h3>

<p><em>dns1.stabletransit.com</em> and <em>dns2.stabletransit.com</em></p>

<h3>How many domains can I host?</h3>

<p>This is a question familiar to those who use shared hosting. There is no limit, since you are in control of everything on your Cloud Server.</p>

<h3>I’m kind of new to this, will it be difficult?</h3>

<p>Maybe. That mostly depends on your experience as a Systems Administrator for Linux and/or Windows Server. Our Linux Cloud Servers are full Linux distributions with root-level access. Our Windows Cloud Servers give you Administrator access, and are built with nothing but the default applications on install. Cloud Servers are geared towards customers who want to start from scratch and tune a system for their own purposes.</p>

<p>If, after wearing the Systems Administrator hat for a while, you feel that you are out of your league - don't despair! We also offer Cloud Servers with a Managed Operations. Read here for more information on <a href="http://www.rackspace.com/cloud/managed_cloud/">Cloud Servers with Managed Operations</a>.</p>

<h3>What level of support comes with Cloud Servers?</h3>

<p>We have two Service Levels: <strong>Managed Infrastructure</strong> and <strong>Managed Operations</strong>. At the Managed Infrastructure level, we support the Cloud Server hardware, datacenter environment, and Internet connectivity - but do not support the software installed on your server, including the operating system and its configuration. When you provision a Cloud Server, you will be given a server with unrestricted access. The Managed Infrastructure support team will not assist in the installation of software or troubleshooting any kind of issue related to the software installed. We have some articles in the Knowledge Center covering basic installation of common applications. We also have community forums where you can share tips and tricks with other customers.</p>

<p>If you would like to have a <a href="https://www.rackspace.com/knowledge_center/article/cloud-servers-with-managed-cloud-service-level-spheres-of-support">Managed Operations</a> on your Cloud Servers, we offer that service. This operations level provides additional support on Cloud Servers, which includes monitoring, operating system and application infrastructure layer support, and technical guidance.</p>

<h3>What can I do with a Cloud Server?</h3>

<p>Anything you want to (within the law and our <a href="http://www.rackspace.com/cloud/legal/aup/">Acceptable Use Policy</a>, of course)! The Rackspace Cloud Server solution is a fully unrestricted, root/Administrator level access, Linux or Windows environment. Any application or service that you can run from a traditional, physical, dedicated-unmanaged operations can be run from your Cloud Server.</p>

<h3>Can I reinstall a different distribution or start over?</h3>

<p>Of course you can! Simply press the <strong>Rebuild</strong> button in the Control Panel and you will be able to select a new distribution. Be sure you have a backup of your data because this process will destroy any data that is on the server. The rebuild process does allow you to save you IP address.</p>

<h3>What if I mess up my Cloud Server?</h3>

<p>You can <a href="https://www.rackspace.com/knowledge_center/article/managing-your-server-3-reboot-your-server-0">reboot your server</a>. You can <a href="https://www.rackspace.com/knowledge_center/article/cloud-essentials-4-creating-an-image-backup-cloning-and-restoring-a-server-from-a-saved">restore from a backup</a>. You can <a href="https://www.rackspace.com/knowledge_center/article/managing-your-server-8-deleting-your-server-0">delete your server</a> and start over. You can <a href="https://www.rackspace.com/knowledge_center/article/rackspace-cloud-essentials-3-rescue-mode-on-linux-cloud-servers-1">boot into an emergency rescue mode</a> and attempt fix the problem. There are many options for recovering from mistakes, but the easiest is to keep regular backups and to <a href="https://www.rackspace.com/knowledge_center/article/best-practices-for-backing-up-your-data-cloud-block-storage-versus-cloud-backup">make a fresh backup</a> before attempting any major configuration changes or before installing new software.</p>

---------

<h2>Account services</h2>

<h3>What are security groups?</h3>

<p><em>Security groups</em> are named collections of network access rules that&nbsp;enable Rackspace Public Cloud users to specify the types of traffic that are allowed to pass through PublicNet and ServiceNet ports on a Cloud Servers instance.&nbsp;A security group is a container for <em>security group rules</em>. After you launch an instance, you can assign one or more security groups to ports on that instance. &nbsp;Security groups act as a stateful firewall for your Cloud Server instances.</p>

<h3>Where is the documentation?</h3>

<p><a href="https://developer.rackspace.com/docs/cloud-networks/v2/developer-guide/#document-concepts/concepts-security-groups">Cloud Networks Developer Guide</a></p>

<p><a href="https://developer.rackspace.com/docs/cloud-networks/v2/developer-guide/#document-api-operations/sec-group-operations">Cloud Networks API Reference</a></p>

<h3>What are the benefits of using security groups?</h3>

<p>Prior to the release of this feature, users had to manage traffic to and from their instances individually via iptables rules (as an example) on every instance, or perhaps use third-party tools such as CloudPassage. Managing firewall policies involves significant overhead. Security groups make it possible to use a self-service API to define a common set of rules and apply them to the servers without needing to manage iptables rules on each server. Security groups simplify security policy administration for customers across their deployments.</p>

<h3>What is being launched?</h3>

<p>We are launching security groups as limited availability in all data centers, so customers can request the security groups feature and receive provisioned endpoints in their service catalog. Security groups are supported for Managed Infrastructure (non RackConnect) customers at launch.</p>

<h3>What features are supported at launch?</h3>

<p>With the limited availability launch in early 2015, we support only inbound security groups on both PublicNet and ServiceNet interfaces. This means that customers can filter incoming traffic to their PublicNet and ServiceNet ports. We will add outbound security group support later in 2015.</p>

<h3>Will security groups be supported via the neutron client?</h3>

<p>Yes. Users can provision security groups via the neutron client.</p>

<h3>Is this functionality integrated with and available from the Cloud Control Panel?</h3>

<p>Not yet. The product will be available soon. In the interim, you can use either the neutron client or the API.</p>

<h3>Are security groups supported for OnMetal users?</h3>

<p>No. We currently support security groups only for virtual cloud servers.</p>

<h3>Is a default security group applied to my instances?</h3>

<p>No default security groups are applied. Users must create a security group themselves and apply it to ports on an instance.</p>

<h3>Can I apply security groups to ports on an instance at boot time?</h3>

<p>No. Security groups can be applied only after the instance is active.</p>

<h3>What happens when a security group rule is added to the security group?</h3>

<p>Traffic that matches the new security group rule is allowed to go through.</p>

<h3>Can traffic be blocked or denied based on a security group rule?</h3>

<p>No. Traffic that matches a rule is permitted, and any traffic that is not part of the ruleset for that security group is denied or blocked. Because of OpenStack API design requirements, you cannot specify that traffic matching a rule should be denied. The security groups API is a whitelist. Thus, traffic that doesn't match any of the rules in the whitelist is automatically blacklisted.</p>

<h2>Is there any traffic that is permitted or allowed by default by security groups?</h2>

<p>DNS responses from Rackspace Provider DNS servers (UDP source port 53) are allowed by default even if a security group does not explicitly allow them. Also the TCP flags ACK and RST are permitted by default.</p>

<h3>What kinds of traffic can be matched by the security group rules?</h3>

<p>The following types of traffic can be matched (for both IPv4 and IPv6 addresses):</p>

<ul>
	<li>TCP traffic</li>
	<li>UDP traffic</li>
	<li>ICMP traffic</li>
	<li>Traffic from a Source IP address</li>
	<li>Traffic from a CIDR</li>
</ul>

<h3>Can I have a security group with no rules?</h3>

<p>Yes. Such a security group will deny or block all traffic.</p>

<h3>Are security groups applied to instances?</h3>

<p>No. Security groups are applied to a Neutron port on a network that is attached to an instance and not to an instance itself.</p>

<h3>What are the limits for security groups and rules?</h3>

<p>You can apply up to 5 security groups per port.</p>

<p>You can have up to 20 security group rules per security group</p>

<p>You can have up to 100 security group rules (aggregate) per user during the limited availability release.</p>

<h3>Are Rackspace Cloud Servers HIPAA compliant?</h3>

<p>Rackspace cannot determine if a given customer is meeting their obligations under the laws applicable to them, and it remains our customers’ obligation to understand the laws applicable to their use of the services and select appropriate services to meet those obligations. We do understand the needs of many of our customers in the healthcare space to implement appropriate security measures to protect the sensitive information they work with.&nbsp;</p>

<p>To help customers in the healthcare industry meet their compliance requirements with regards to HIPAA, Rackspace offers a <a href="http://www.rackspace.com/information/legal/hipaabaa">Business Associate Agreement</a> in all of our dedicated hosting services segments, and it is included by default in our agreements with customers for those services.</p>

<h3>How does Cloud Servers handle my data from potentially becoming visible when I delete a server?</h3>

<p>For your security, the Virtual Hard Drive (VHD) on the hypervisor is deleted when you delete a server. Once it is deleted, data cannot be retrieved and customers do not have logical or direct access to the physical drive.</p>

<h3>What are PVHVM images?</h3>

<p>PVHVM refers to the virtualization mode used by the hypervisor to run the virtual machine. PVHVM images are virtual machine images that use the PVHVM virtualization mode. In general, PVHVM offers better performance than PV, especially for disk and network IO, but is not well supported in Linux operating systems with a kernel version earlier than 2.6.36. The availability of PV and PVHVM images in the Rackspace Cloud is determined by the effectiveness of each virtualization mode for that particular operating system.</p>

<p><strong>Note</strong>: Work-optimized servers (Compute, I/O, and Memory) require PVHVM images. If you try to create a work-optimized server by using a non-PVHVM image, the following error message is displayed: <code>Image cannot be built with provided flavor</code>.</p>

<p>For more information about PVHVM, see <a href="https://www.rackspace.com/knowledge_center/article/choosing-a-virtualization-mode-pv-versus-pvhvm">Choosing a Virtualization Mode (PV versus PVHVM)</a>.</p>

<h3>What do I enter in the Server Name field?</h3>

<p>The information that you enter in the <strong>Server Name </strong>field helps you identify this server in the API and Cloud Control Panel. The name that you enter when you create a server is used as the server’s host name. If you rename the server later, the name that is displayed in the API and Cloud Control Panel is updated. However, the host name on the computer is not updated.</p>

<h3>Can I connect to a server by using the server name?</h3>

<p>To connect to the server from outside of the server’s local network, you need to configure an A record in Cloud DNS. To access Cloud DNS, in the top navigation bar of the Cloud Control Panel, select <strong>Networking &gt; Cloud DNS</strong>.</p>

<p>For example, if you name your server <strong><a href="http://mywebserver1.myexampledomain.com/">MyWebServer1.MyExampleDomain.com</a></strong>, you must add an A record for <strong><a href="http://mywebserver1.myexampledomain.com/">MyWebServer1.MyExampleDomain.com</a> </strong>to your DNS zone (<a href="http://myexampledomain.com/">MyExampleDomain.com</a>) that points to the public IP address of the server. The information that you enter in the <strong>Server Name</strong> field helps you identify this server in the API and <a href="https://mycloud.rackspace.com/">Cloud Control Panel</a>.</p>

<h3>Can I read your SLA?</h3>

<p>Sure, it's <a href="https://www.rackspace.com/information/legal/cloud/sla" title="Rackspace Cloud SLA">right here</a>.</p>

<h3>How do I contact Support?</h3>

<p>At Rackspace, our goal is to make the Cloud easy for you to use. To meet that goal, we have created many different ways for you to get the support that you need to get the most out of the Cloud.</p>

<ul>
	<li>Your first stop should be our <a href="/how-to/">Knowledge Center</a>, which is the best source for articles and tutorials to help you get the precise answers that you need.
	<p>The Knowledge Center contains the <a href="/how-to/">Getting Started with Cloud Servers Guide</a>, which provides you with the most important information that you need to set up a server.</p</li>
	<li>Our <a href="https://community.rackspace.com/products/f/25">Open Cloud Forum</a> in the Rackspace Community is always open. Use the forum to get your questions answered by a Racker.</li>
	<li>Do you have a quick question that you can't find an answer for in the Knowledge Center? Open Chat and talk with our Fanatical Support® staff anytime, 24x7x365.</li>
	<li>Do you have a specialized Service Request or are you experiencing a problem with our service? Open a ticket. From the Rackspace <a href="http://mycloud.rackspace.com/">Cloud Control Panel</a>, select <strong>Support Tickets</strong> from the Account menu. Click <strong>Create Ticket</strong> to open a ticket directly with our support teams to report a problem or make a service request.</li>
	<li>Call us 24x7x365 at 800 961 4454 (toll-free) or +1 210 312 4000 (international).</li>
</ul>

---------

<h2>Server Management</h2>

<h3>Do you host DNS?</h3>

<p>Yes. Our Control Panel has a DNS menu for maintaining domain records for your Cloud Servers. Read this article for <a href="https://www.rackspace.com/knowledge_center/article/getting-started-with-cloud-sites-managing-dns-records">detailed information on using the Rackspace Cloud DNS Control Panel</a>.</p>

<h3>How do I get reverse DNS setup for my Cloud Server?</h3>

<p>You can setup reverse DNS from your control panel. This article will show you how: <a href="https://www.rackspace.com/knowledge_center/article/create-a-reverse-dns-record-0">Create a reverse DNS record.</a></p>

<h3>Is there a throughput limit on my server's network interface card?</h3>

<p>The amount of network throughput varies based on the Cloud Server flavor. For more details, see <a href="http://www.rackspace.com/cloud/public-pricing/#cloud-servers">here</a>.</p>

<h3>Do you offer internal IPs?</h3>

<p>Yes. Each server comes with an internal IP address that is used to communicate between servers. The traffic that flows over this interface (eth1) on your server is unmetered and is not billed. This network is also referred to as ServiceNet. ServiceNet is an internal only, multi-tenant network connection within each Rackspace datacenter. ServiceNet IPs are not accessible from the public Internet and are local per datacenter.</p>

<h3>Can I buy extra public IPs?</h3>

<p>Yes. For more information on the IP request process, see <a href="https://www.rackspace.com/knowledge_center/article/requesting-additional-ipv4-addresses-for-first-and-next-generation-cloud-servers">Requesting Additional IPv4 Addresses for First and Next Generation Cloud Servers</a>.</p>

<h3>I would like to set up multiple servers from the same image. Can I do this?</h3>

<p>As a Cloud Servers customer, you have access to create both on-demand images and scheduled images of your cloud server. All Cloud Server images will be stored in your Cloud Files account. This enables you to keep these images even after the Cloud Server they were created on is deleted. It also allows the flexibility to create an unlimited number of on-demand images of your Cloud Server. All Cloud Server images can be used to create new Cloud Servers or restore an existing Cloud Server. For details, see <a href="https://www.rackspace.com/knowledge_center/article/creating-an-image-of-your-performance-flavor-server-with-the-control-panel">Creating an Image of Your Performance Flavor Server with the Control Panel</a>.</p>

<h3>Do you offer on-demand images (snapshots) and scheduled images and what are the prices?</h3>

<p>You can create an image of any General Purpose&nbsp;Cloud Server, and you can use this image to restore a server or clone a new one. You can create an unlimited number of images on-demand, or you can schedule an automatic daily or weekly image.</p>

<p>Images will be compressed and stored on Rackspace Cloud Files at the <a href="http://www.rackspace.com/cloud/cloud_hosting_products/files/pricing/">current storage rates</a>. Please also read this list of <a href="https://www.rackspace.com/knowledge_center/article/rackspace-cloud-essentials-cloud-server-image-limitations">Snapshot Limitations</a>.</p>

<p>If using a virtual cloud server, see <a href="https://www.rackspace.com/knowledge_center/article/creating-an-image-of-your-performance-flavor-server-with-the-control-panel">Creating an image of your General Purpose Cloud Server with the control panel</a> for more information on the image options associated with virtual cloud servers.</p>

<h3>I would like to use the GUI interface for my Linux Cloud Server. Is this possible?</h3>

<p>Yes it is! An article on how to install VNC and X-Windows is located here: <a href="/how-to/vnc-install" title="VNC Install">VNC Install</a>. Keep in mind that this will use up a large amount of bandwidth on your server.</p>

<h3>Do you have a control panel?</h3>

<p>Yes, the Rackspace <a href="https://mycloud.rackspace.com/">Cloud Control Panel</a> is a web-based management interface for restarting your cloud server, starting support discussions, viewing stats, and scheduling snapshots. However, we do not offer a control panel like Plesk or cPanel. You’re free to install such packages for your own cloud server.</p>

<p>You may be interested in installing the free monitoring agent on your server and using the <a href="https://intelligence.rackspace.com/">Cloud Intelligence dashboard</a>, which offers many of the same functions as a control panel.</p>

<h3>Do you provide Console access?</h3>

<p>Yes, via a Java web terminal accessible through the Details section of each webserver, in the Actions menu under the section labeled Manage, you will see a link to Connect Via Terminal.</p>

<p><strong>Note</strong>: Console access is via a secure HTTP connection which is different connection from the traditional way to connect via SSH for Linux or RDP for Windows. Console can be a useful troubleshooting tool if your server is unresponsive or you have locked yourself out.</p>

<h3>Can I reboot my machine?</h3>

<p>Yes. All Cloud Servers can perform both soft (reset button) and hard (power cycle) reboots. These are performed instantly and handled via the Cloud Server Control Panel.</p>

<h3>Will I be billed if my server is powered off?</h3>

<p>Yes. You will be billed for the resources that are used on the host while your server is in the <strong>Active</strong> status. When your server is created, you are given a dedicated amount of RAM and hard drive space. As long as your server exists, no one else will be able to use those resources that have been allocated to you - this is why you are billed per hour even while powered off. If you would like to stop incurring charges for a given server, you must delete that server in the Control Panel.</p>

<p>If you want to stop paying for a server, but still need to retain the configurations from it, your best option is to <a href="https://www.rackspace.com/knowledge_center/article/creating-an-image-of-your-performance-flavor-server-with-the-control-panel">create an image</a> of the Cloud Server. Your system configurations on your system disk will be preserved in the image. The image will be saved in Cloud Files and accessible through the Saved Images tab in the Control Panel. There is a fee associated with Cloud Files storage but it is much less than the cost of an active server. You will also need to save the data from your data disk out to Cloud Block Storage or Rackspace Cloud Backup to have available on your next server. Then you will be free to delete the original server, safe in the knowledge that you can always provision a new server using the saved image of your old server and you saved data.&nbsp; After restoring your server from the saved image, the primary difference will be that your new server has a different IP address from the old one. Putting the new server into production may require you to update any associated DNS records to reflect the new IP address.</p>

<h3>How do I power my server back on after shutting it down?</h3>

<p>Please see the following article: <a href="https://www.rackspace.com/knowledge_center/index.php/Shutting_Down_and_Restarting_a_Cloud_Server" title="Shutting Down and Restarting a Cloud Server">Shutting Down and Restarting a Cloud Server</a></p>

<h3>Which distributions do you offer?</h3>

<p>The Features section of our <a href="http://www.rackspace.com/cloud/servers/">product page</a> has information regarding the Linux distributions and Windows operating systems that we have available.</p>

<h3>Can I upgrade down the road?</h3>

<p>Yes. With General Purpose&nbsp;Cloud Servers, you can change the size of your data storage space in one of two ways:</p>

<ul>
	<li>Increase Available Storage with Cloud Block Storage. For more information on Cloud Block Storage, see <a href="https://www.rackspace.com/knowledge_center/article/create-and-attach-a-cloud-block-storage-volume">Create and Attach a Cloud Block Storage Volume</a>.</li>
	<li>Migrate to a larger size server with more RAM, disk space, and vCPUs. For&nbsp; more information on resizing, see <a href="https://www.rackspace.com/knowledge_center/article/changing-the-size-of-your-performance-cloud-server">Changing the Size of Your First Generation Cloud Server</a>.</li>
</ul>

<h3>How many users go onto each machine?</h3>

<p>The number of customers on a Cloud Server host machine depends on the size of the customers’ Cloud Servers, and the type of operating system.</p>

<h3>How does the CPU scheduling work on Standard Next Generation servers?</h3>

<p><strong>Note</strong>: <a href="https://www.rackspace.com/knowledge_center/article/what-is-new-with-performance-cloud-servers">General Purpose Cloud Servers</a> have specific virtual CPU allocations, as detailed on the <a href="http://www.rackspace.com/cloud/servers/pricing/">Cloud Servers pricing page</a>. The following information on CPU scheduling applies only to next-generation standard (for example, not General Purpose) Cloud Servers.</p>

<p>For Windows images, each Cloud Server is assigned a number of virtual cores based on the size of the Cloud Server. The Standard 1 GB Cloud Server receives 1 virtual core, the standard 2 GB and 4 GB Cloud Servers receive 2 virtual cores, the standard 8 GB and 15.5 GB Cloud Servers receive 4 virtual cores, and the standard 30GB servers receive 8 virtual cores. Each of these cores is given equal weight when allocating CPU cycles.</p>

<p>For Linux distributions, each Standard Cloud Server is assigned the number of virtual cores and the CPU cycles allocated to these cores, as selected when creating the server in the Control Panel.</p>

<p>All standard Cloud Servers receive a guaranteed minimum amount of CPU cycles with the ability to burst when excess cycles are available.</p>

<h3>How long does a standard Cloud Server resize take?</h3>

<p>The amount of time a resize takes varies by the size of the server and the time of day you are performing the resize. If you have a brand-new server with no additional data or software installed, then you might be looking at 10 minutes. However, if you have data installed on your server and have been installing software then it can take up to 30 minutes or more. Peak times for resize activity tend to be at the start and end of the business day. Expect a short period of downtime while your server is being resized.</p>

<p>Note also that resizing a server down can take longer than resizing up because the system needs to consolidate and copy data to a smaller disk container rather than expand the existing container. Cleaning up unneeded files (like old logs and session files) can improve the speed of a resize operation.</p>

<p>There are different processes of resizes, as follows:</p>

<ul>
	<li><strong>Online Resizes</strong>: Allow for the original sized Cloud Server to be powered on during the "Prep-Resize" step, and only powers down during the second step of the resize process.
	<p>This includes: First Generation Server resize up and resize down, and Standard resize up.</p></li>
	<li><strong>Offline Resizes</strong>: Power down as the first "Prep-Resize" step.
	<p>This includes: Standard resize down.</p></li>
</ul>

<p><strong>NOTE</strong>: Resizing is not available for workload-optimized Cloud Servers. For information on your available options, see <a href="https://www.rackspace.com/knowledge_center/article/changing-the-size-of-your-performance-cloud-server">Changing the size of your workload-optimized Cloud Server</a>.</p>

<h3>Can I buy extra storage?</h3>

<p>While the native storage allocation for a Cloud Server is based on the Cloud Server flavor that you select, you can also add extra storage at any time with our <a href="http://www.rackspace.com/cloud/blockstorage/">Cloud Block Storage</a> service.</p>

---------

<h2>Performance</h2>

<h3>What is the difference between Standard and General Purpose Cloud Servers?</h3>

<p>There are several noteworthy differences between Standard and General Purpose Cloud Servers:</p>

<ul>
	<li>General Purpose Cloud Servers use faster solid state drives (SSD) compared to the standard spinning disk allocation for Standard Cloud Servers.</li>
	<li>Up to 120 GB of RAM is available on General Purpose servers, whereas Standard Servers provide up to 30 GB of RAM.</li>
	<li>You can have up to 32 vCPUs running on General Purpose Cloud Servers, comapred to the maximum of 8 on the Standard Cloud Servers.</li>
	<li>Maximum network bandwidth on Standard Cloud Servers is 300 Mbps public network and 600 Mbps private network. Maximum network bandwidth on General Purpose Cloud Servers is 10,000 Mbps to divide between public and private networks as you choose.</li>
</ul>

<p>For more information about General Purpose Cloud Servers, see <a href="https://www.rackspace.com/knowledge_center/article/what-is-new-with-performance-cloud-servers">What is new with General Purpose Cloud Servers</a>.</p>

---------

<h2>Billing and Account</h2>

<h3>Do you offer discounts for Cloud Servers?</h3>

<p>Yes. We offer different types of discounts based on usage. Please see the <a href="http://www.rackspace.com/cloud/servers/discounts/">Cloud Servers discounts page</a> for details.</p>

---------

<h2>Support</h2>

<h3>Can I have traffic blocked or denied based on a Security Group rule?</h3>

<p>Traffic that matches a rule is permitted. Any traffic that is not part of the ruleset for that Security Group is denied / blocked. There is no way to specify that traffic matching a rule should be denied. This is how the OpenStack Security Groups API was designed. Hence the Security Groups API is a white-list. Traffic that doesn't match any of the rules in the white-list is automatically black-listed.</p>

---------

<h2>Security</h2>

<h3>What happens when a Security Group rule is added to the Security Group?</h3>

<p>Traffic matching a Security Group rule is allowed to go through.</p>

<h3>Can I apply Security Groups to ports on an instance at boot time?</h3>

<p>No. Security Groups can only be applied after the instance is active.</p>

<h3>Is there a default Security Group that gets applied to my instances?</h3>

<p>No, there is no default security Group that gets applied. Users have to create a Security Group themselves and apply them to ports on an instance.</p>

<h3>Are Security Groups supported for OnMetal users?</h3>

<p>No, Security Groups are currently only supported for Virtual Cloud servers.</p>

<h3>Will this be integrated and available to use via the Control Panel / Reach?</h3>

<p>The product will be available via Control panel very soon. In the interim, customers can use either the Neutron client or the API.</p>

<h3>Will Security Groups be supported via Neutron client?</h3>

<p>Yes. Users can provision security groups via Neutron client.</p>

<h3>Are Security Groups on Cloud Networks supported?</h3>

<p>No. Rackspace will add Security Group support for Cloud Networks&nbsp;in the near future.</p>

<h3>Are Outbound Security Groups supported?</h3>

<p>No. Rackspace will add Outbound security Group support in the near future.</p>

<h3>What features are supported at launch for Security Groups?</h3>

<p>Inbound Security Groups on PublicNet and ServiceNet interfaces are supported. This means customers can filter incoming traffic to their PublicNet and ServiceNet ports.</p>

<h3>Is the security group feature supported for all Cloud customers?</h3>

<p>Security Groups will only be supported for Managed Infrastructure, non-RackConnect customers at launch.</p>

<h3>Is Security Groups available to all Rackspace Public Cloud users?</h3>

<p>Security Grouos is in&nbsp;Limited Availability in all Data Centers. Please contact Rackspace support to enable this feature.</p>

<h3>What are the benefits of using Security Groups?</h3>

<p>Prior to this feature being available, customers had to manage traffic to/from their instances individually via (for example) ipTables rules on every instance (or perhaps use 3rd party tools). Managing firewall policies involves in a distributed fashion significant overhead to keep track of and manage. Security Groups makes it possible to use self-service API to define a common set of rules and apply them to the Neutron ports (Public/ServiceNet) on Cloud Servers without needing to tweak iptables rules on each server, thereby simplifying administration of security policies.</p>

<h3>What are Security Groups?</h3>

<p>Security groups are a&nbsp;named collection of network access rules that&nbsp;provide Rackspace Public Cloud users the ability to specify the types of traffic that are allowed to pass through, to and from ports (Public/ServiceNet) on a Cloud server instance. A security group is a container for security group rules. After you launch an instance, you can assign one or more security groups to ports on that instance. Security Groups act as a stateful firewall for your cloud server instances.</p>

<h3>Are cloud servers PCI-DSS compliant?</h3>

<p>The Rackspace Cloud environment has not been formally assessed for for compliance with the Payment Card Industry (PCI) Data Security Standard (DSS). For information about PCI-DSS, see <a href="http://www.rackspace.com/security/solutions/#pci">Cloud Security Solutions</a>. For information about PCI-DSS when using Rackspace Dedicated Hosting services, see <a href="http://www.rackspace.com/ecommerce-hosting/pci/">PCI-Compliant Hosting for E-commerce Websites</a>.</p>

<h3>Can I run a firewall on my server?</h3>

<p>Definitely and we encourage it! Each Linux server is capable of running the Linux-standard firewall called <strong>iptables</strong>- some even have it pre-configured! Other firewall systems have been tested on Cloud Servers as well.</p>

<h3>Is there a limit of number of rules per user?</h3>

<p>There is an aggregate limit of 100 security Group rules per user during Limited Availability. Please contact Rackspace support if you need this limit raised.</p>

<h3>Is there a limit of number of rules per Security Group?</h3>

<p>There is a limit of 20 security Group rules per Security Group. Please contact Rackspace support if you need this limit raised.</p>

<h3>How many Security Groups can I apply per port?</h3>

<p>Up to 5 security Groups are allowed per port. Please contact Rackspace support if you need this limit raised.</p>

<h3>Are Security Groups applied to instances?</h3>

<p>Security Groups are applied to Neutron ports (PublicNet and ServiceNet) on Cloud Server instances.</p>

<h3>Can I have a Security Group with no rules?</h3>

<p>Yes. Such a Security Group will deny/ block all traffic.</p>

<h3>What kinds of traffic can be matched by the Security Group rules?</h3>

<p>TCP, UDP, ICMP traffic can be matched in addition to traffic from a Source IP address or CIDR. Both IPv4 and IPv6 traffic can be matched.</p>

<h3>Is there any traffic that is permitted or allowed by default by Security Groups?</h3>

<p>DNS responses from Rackspace Provider DNS servers (UDP source port 53 ) are allowed by default even if they are not explicitly allowed by a Security Group.</p>

<p>Also TCP flags ACK and RST are permitted by default.</p>

<h3>What are the maximum limits for the Cloud Servers service?</h3>

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

<h3>When a Cloud Server is deleted how is the data removed from the host server?</h3>

<ul>
	<li>First Generation Cloud Servers on xen classic use LVM storage. As such, when a server is deleted it is scrubbed by writing 0's over the partition.</li>
	<li>Next Generation Cloud Servers use VHD storage. Once a server is deleted the VHD is deleted, similar to the way you would do a rm command in Linux. When that is done the VHD is completely removed thus allowing another one to be created.</li>
</ul>

---------

<h2>API</h2>

<h3>Where are your APIs?</h3>

<p>You can find the documentation for the API for Cloud Servers and our other products on the <a href="https://developer.rackspace.com/docs/">Rackspace Developer Docs</a>.</p>

<p>Before you can start using our APIs, you will need your API Key. You can obtain your API key by following the instructions in our article, <a href="https://www.rackspace.com/knowledge_center/article/rackspace-cloud-essentials-1-viewing-and-regenerating-your-api-key">Viewing and Regenerating Your API Key</a>.</p>
