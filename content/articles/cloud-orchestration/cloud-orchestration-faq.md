---
node_id: 5008
title: Cloud Orchestration - FAQ
type: article
created_date: '2015-12-09'
created_by: Stephanie Fillmon
last_modified_date: '2016-01-19'
last_modified_by: Stephanie Fillmon
product: Cloud Orchestration
body_format: markdown_w_tinymce
---

<h2>General</h2>

<h3>What is Cloud Orchestration?</h3>

<p>Cloud Orchestration is a service that allows you to create, update and manage groups of cloud resources and their software components as a single unit and then deploy them in an automated, repeatable fashion via a template. Cloud Orchestration is based off the OpenStack Heat project. Our service runs upstream OpenStack Heat code with only a few slight modifications to ensure a positive customer experience on our cloud.</p>

<p>Using the <a href="http://mycloud.rackspace.com">Cloud Control Panel</a> UI, API or the CLI you can create, edit, update and delete full stack configurations. In addition to this service, Orchestration also provide “Rackspace Templates” section in the Control Panel. This include several pre-built templates that incorporate industry best practices and allow customers to quickly deploy specific application and platform stacks such as WordPress, LAMP, PHP, etc.</p>

<p>Cloud Orchestration API currently supports declaration and configuration of:</p>

<ul>
	<li>Cloud Servers</li>
	<li>Cloud Load Balancers</li>
	<li>Cloud Databases</li>
	<li>Cloud Block Storage</li>
	<li>Cloud DNS</li>
	<li>Auto Scaling</li>
	<li>Bash scripts, and</li>
	<li>Chef Cookbooks and Berkshelf</li>
</ul>

<h3>Can I access Cloud Orchestration API using a command-line client?</h3>

<p>Yes. Rackspace does not currently provide a Rackspace specific command-line client for Cloud Orchestration, however we recommend you use the open source Heat python client developed by the OpenStack community. The Python Heat Client is compatible with Rackspace’s Cloud Orchestration Service. Instructions on obtaining and installing the command line client can be found in the Orchestration <a href="https://developer.rackspace.com/docs/cloud-orchestration/v1/developer-guide/#document-getting-started">Getting Started Guide</a>.</p>

<p>The Heat python client provides command-line access to the orchestration API operations. We recommend that you use this client to run simple commands that make API calls. You can specify a --debug parameter on any command to show the underlying API request for the command. This is a good way to become familiar with the API requests.</p>

<h3>Can I access Cloud Orchestratino through the Cloud Control Panel?</h3>

<p>Yes. Log in to the <a href="http://mycloud.rackspace.com">Cloud Control Panel</a> and click on the&nbsp;<strong>Orchestration</strong>&nbsp;tab.</p>

<h3>Is Orchestration a Platform as a Service (PaaS)?</h3>

<p>No. Although Orchestration does contain much of the structure of a PaaS, it has additional transparency and control that a PaaS does not usually offer. Orchestration has capabilities similar to a PaaS, such as application launch on various platforms, but differs from a formal PaaS in that it deploys full instances of servers, load balancers, and databases. Orchestration gives you the additional control of knowing exactly what resources are used and what software is installed. Orchestration provides the convenience of automating the resource stack, and gives you full knowledge and additional control beyond what many PaaS solutions offer.</p>

---------
<h2>Billing and Account</h2>

<h3>Where can I find pricing and service level information for Cloud Orchestration?</h3>

<p>The Cloud Orchestration service is offered at no cost, and you pay standard charges for cloud resources instantiated and consumed, and any applicable software license fees.</p>

<p>Cloud Orchestration is a Non-Standard Rackspace Service. Applicable SLAs for the underlying infrastructures apply for successfully launched cloud products.</p>

<h3>Is there a cost associated with the Orchestration service?</h3>

<p>There is no cost for using the Orchestration service, but any infrastructure components such as Cloud Servers, Cloud Databases, and Cloud Load Balancers used in a stack are billed at standard pricing.</p>

---------
<h2>Support</h2>

<h3>How do I recover application passwords?</h3>

<p>Recovering passwords for applications is different from recovering server passwords. Some passwords might be available in configuration files or in databases on your server. Other passwords might need to be reset using a series of steps defined by that application vendor. Check documentation and FAQ information with the application vendor for the specific steps to reset application or user passwords. Remember that you might also need to change configured passwords in client or other applications that use the credentials that you are resetting.</p>

<h3>How do I recover my server password?</h3>

<p>After your stack has completed, you are provided with private keys and passwords for your cloud resources. To reset your server passwords, use the <a href="/how-to/how-to-change-your-server-rootadmin-password-from-your-account">Change Password</a> function.</p>

<h3>How do I log in to my servers?</h3>

<p>After your stack has completed, you are provided with the credentials to your servers. If you are not sure how to log in with those credentials, see the https://www.rackspace.com/knowledge_center/article/connect-to-a-cloud-server article.</p>

<h3>How do I access my application?</h3>

<p>It depends on the application. After a stack is complete, you are provided with the necessary passwords, keys, and URLs to log in to your servers and newly deployed application.</p>

<h3>Can I create a stack with different versions of an application?</h3>

<p>We are working to add a number of common application templates to our catalog. There are thousands of different versions of applications, frameworks, databases, and support software. While we attempt to offer the latest versions, offering multiple versions of applications might not always be possible. If you have specific requests for additions to the Orchestration service, submit your request through <a href="https://feedback.rackspace.com/">Rackspace Product Feedback</a>.</p>

<h3>What do I do if an error occurs when creating a stack?</h3>

<p>If you receive an error, you have the following options:</p>

<ul>
	<li>You can delete the stack and start a new one. Many times trying again results in a successful stack.</li>
	<li>You can submit a support ticket to get help with the error state. The support team can assist in completing the stack on your behalf.</li>
</ul>

<h3>What is the service level agreement for the Orchestration service?</h3>

<p>The Orchestration service is offered as a convenience feature to customers. It interacts with an assortment of cloud resources and automates a large number of tasks. The risk of failure is increased because of the number of tasks. We are aware of this and are constantly working to improve the success rates and build times of orchestration. At this time there is always a potential for failure in the stack setup process. As a result, Rackspace does not provide a service level agreement(SLA) for this Control Panel feature, nor does Rackspace guarantee a successful completion of a stack within a specified period of time. Any stack that does not complete should be deleted to avoid possible usage fees. After the stack is completed successfully, the SLA for the deployed cloud resources applies. Any problem that occurs after stack should be directed to your support team.</p>

<h3>Do I need my own domain?</h3>

<p>It depends on the application that you want to run. Most templates require a domain name and provide an explanation of how the domain is used. In some cases, the domain name is for setting host names; in other cases, it is used to set up a web server and application to run from that domain. For any web-based application, it is best to use your own domain.</p>

<h3>How do I enable monitoring on the servers?</h3>

<p>Information about how to configure monitoring on the servers in your stack is located in the <a href="https://developer.rackspace.com/docs/cloud-orchestration/v1/developer-guide/#document-getting-started">Cloud Monitoring Getting Started Guide</a>.</p>

---------
<h2>Features</h2>

<h3>Does deleting a stack remove all infrastructure?</h3>

<p>Yes. Deleting a stack removes all servers, databases, load balancers, and any other resources that were created when the stack was built. You no longer see any associated resources in the lists of servers, databases, and so on.</p>

<p>You can choose to delete these resources individually through the Cloud Control Panel, but be aware that deleting one or more of the resources within a stack will likely make the stack unstable and possibly inoperable.</p>

<h3>Can the Orchestration service deploy a hybrid cloud or dedicated infrastructure?</h3>

<p>Not at this time. Orchestration deploys only Rackspace Cloud resources. However, customers with RackConnect accounts can still use Orchestration to deploy cloud resources and then connect those resources to a hybrid environment.</p>

<h3>Can a template be applied on top of an existing stack?</h3>

<p>Yes. You can use the update operation in the Orchestration API to apply a template to an existing stack.</p>

<p><strong>WARNING</strong>: The template might rebuild all the existing resources and cause you to lose your data if it is unable to detect your existing software. Back up your data before you begin this task.</p>

<h3>Can a Rackspace template be installed on existing deployed infrastructure?</h3>

<p>Yes. You can use the adopt stack operation in the Cloud Orchestration API to use existing cloud resources in a new stack. Read more about the operation in the <a href="https://developer.rackspace.com/docs/cloud-orchestration/v1/developer-guide/">Cloud Orchestration Developer Guide</a>.</p>

<h3>Does Orchestration manage the stack after creation?</h3>

<p>The Orchestration service does not include automatic maintenance of the stack, such as updating software. Depending on your managed service level, your support team can tell you how they can help you manage your stack.</p>

<h3>How long does it take to create a stack?</h3>

<p>The time that it takes to create a completed stack depends on several infrastructure services and also depends on the level of traffic in a specific data center at the time of the build.</p>

<h3>How do I know when the stack is complete?</h3>

<p>All infrastructure resources show an active status, and the stack changes from the yellow</p>

<h3>What are the different build states?</h3>

<ul>
	<li>Build</li>
	<li>Up</li>
	<li>Error</li>
</ul>

<h3>What happens during the build of a stack?</h3>

<ol>
	<li>The Orchestration engine plans and executes a series of tasks that build and configure cloud resources.</li>
	<li>The applications are loaded and configured.</li>
	<li>The Orchestration service ensures that everything works as expected. If any issues occur during the build, the status is updated to reflect this.</li>
</ol>

<p>You can see the status of the stack and resources on the Stack page.</p>

---------
<h2>OpenStack</h2>

<h3>Can I re-use heat templates that I created on Rackspace Cloud Orchestration on other OpenStack heat based service offerings?</h3>

<p>Since Rackspace Cloud Orchestration is built from OpenStack Heat, the thumb rule is yes, you can re-use templates on other Open Stack Heat based offerings. The major exceptions to this thumb rule would be the use of Rackspace resources (resource names beginning with Rackspace) or if the alternate OpenStack Heat service is running an older version of resources versus newer versions used in your template.</p>

<h3>Does Cloud Orchestration support the CFN template format from Amazon?</h3>

<p>Yes, but with the following caveats. Although OpenStack Heat documentation claims support for a subset of this format, there are a variety of nuances and underlying compatibility tools that must be run on the service provider’s cloud to support that format. Rackspace supports the CFN template format and is slowly adding support for individual resources. Currently, the server and loadbalancer resources are supported implying that customers can re-use CFN templates with these. However, if the existing CFN template contains syntax that invokes resources (AutoScale group for example), it will need to be tweaked before use. Customers are encouraged to provide feedback and request new features. This helps us prioritize our roadmap.</p>

<h3>Can I take my heat template from another OpenStack service provider and deploy it at Rackspace?</h3>

<p>Yes, since Rackspace Cloud Orchestration is based off OpenStack Heat, in general, you will be able to easily deploy your existing Heat template on Rackspace Cloud. The only exception is that the template must use resources that are in the <a href="http://orchestration.rackspace.com/raxdox/">supported resource list</a>.</p>

<p>The latest list of resources can be obtained by listing them out via CLI.</p>

<h3>Are there any differences between Cloud Orchestration and OpenStack heat?</h3>

<p>Yes. There are two main differences to note:</p>

<ol>
	<li>
	<p>Additional support for custom defined “Rackspace” resources While Cloud Orchestration is based off the OpenStack Heat project, each service provider running Heat can choose which cloud resource plug-ins to support. In an effort to provide our customers breadth of orchestration support for our public cloud, we run some custom resource plug-ins that other service providers may choose not to run or may not be compatible with other service provider clouds. Templates that use these custom resources may need modification in order to work properly on other service provider or private OpenStack installations.</p>

	<p>Rackspace specific resources are clearly marked in our documentation and begin with Rackspace.” For a full list of supported resource types, please refer to our Orchestration documentation to see instructions for how to <a href="https://developer.rackspace.com/docs/cloud-orchestration/v1/developer-guide/#list-resource-types">list resource types</a>.</p>

	<p><strong>Note</strong>: The “OS:Heat:ChefSolo” resource in this list is a Rackspace contributed resource that is incorrectly labeled as Heat. This will be corrected in subsequent updates.</p>
	</li>
	<li>
	<p>Our Service’s version of Heat is often ahead of the last official OpenStack version At Rackspace, we strive to provide our customers with reliable community developed features of Heat as often as possible. However, to ensure a positive customer experience, our Cloud Orchestration service may at times run newer or older feature code from that developed in the open community. We do this because we employ Test Driven Development methodologies and automation, which allows us to quickly deploy the latest and greatest features ahead of the official OpenStack six-month release cycle. We may lag in supporting an upstream feature in order to ensure we appropriately test all scenarios that could affect our customers. Both Heat and our Orchestration service have versioned APIs and DSL syntax so you can compare our service versions against other installations of Heat.</p>
	</li>
</ol>

---------
<h2>Software</h2>

<h3>What software does the template install?</h3>

<p>The software that is installed is detailed in the description column of the template selector. As part of your template configuration, you have the option to select the operating system and other software. All software listed in the description column, in addition to dependencies, is installed automatically. In some cases, you can specify additional software packages to install.</p>

<h3>What if there is a security vulnerability in the verstion of software installed by Orchestration?</h3>

<p>Orchestration installs software versions that, in many cases, are the most commonly used and have the most popular features, but some versions of these applications might be vulnerable to security exploits. Although Rackspace does not intentionally choose to offer software with known vulnerabilities, this might occur. Customers should always use appropriate security precautions when accessing and using any software, even when deployed with the Rackspace Orchestration service. Always update those versions when security vulnerabilities are identified by the application provider or community.</p>

<h3>Does Rackspace support the software that is installed using the Orchestration service?</h3>

<p>The stack is supported at the system level with the Managed Operations Service Level of support. Only the software in our <a href="https://www.rackspace.com/knowledge_center/article/cloud-servers-with-managed-operations-support-for-linux">Spheres of Support</a> is supported. Software installed on top of a web server or database server (like WordPress or Drupal) is not directly supported, bu the underlying system, web server, and database server are supported.</p>

<p>The underlying structure of the stack is supported at all service levels.</p>

<h3>What are the license files or the GPL for the installed software?</h3>

<p>These licenses are installed on the server where the software is installed. The location varies depending on the software.</p>

---------
<h2>Templates</h2>

<h3>How are Cloud Orchestration templates different from Chef or Puppet?</h3>

<p>Cloud Orchestration is not a replacement for server configuration tools such as Puppet and Chef. Cloud Orchestration is very complementary with Chef or Puppet. You will continue to use Chef and Puppet to “template-ize” your server software configurations, while Cloud Orchestration templates will help you create a full stack that includes all the infrastructure resources required for your stack. Cloud Orchestration allows you to quickly bootstrap your preferred software configuration management solution on to your servers. With Chef, we have gone several steps further and provide direct support to specify the cookbooks and Berksfile you want deployed.</p>

<h3>Where can I find example templates for Cloud Orchestration?</h3>

<p>Cloud Orchestration template examples are currently located on Github in the <a href="https://github.com/rackspace-orchestration-templates">rackspace-orchestration-templates</a> organization.</p>

<h3>What is a Cloud Orchestration template?</h3>

<p>A Cloud Orchestration template is a text file that declares what resources you want as part of a stack and how to configure those resources, including references to any installation scripts or software configuration management artifacts needed to install appropriate applications. Templates are written using the HOT (Heat Orchestration Template) syntax (currently written in YAML). Documentation on how to write templates can be found under the Orchestration topic at <a href="https://developer.rackspace.com/docs/">https://developer.rackspace.com/docs/</a>.</p>

<h3>What is the difference between Rackspace templates and Custom Templates?</h3>

<p>Cloud Orchestration allows customers to deploy their own custom templates (via UI, API, CLI) or leverage pre-built pre-tested templates.</p>

<p>If a customer has built or wants to build their own template, the “Custom Templates” tab in Orchestration section in Control Panel can be used to create stacks via UI.</p>

<p>If a customer wants to save time and effort and take advantage of industry best practices, the “Rackspace templates” section provides several pre-built pre-tested options that allow fully configured stacks to be spun up in quickly. This includes initial software configuration as well as orchestrating the requisite cloud resources.</p>

<h3>Which Rackspace template should I choose?</h3>

<p>The Orchestration service enables you to select the template that is appropriate for your needs. Each template has a simple description or flavor, and a detailed description that you can access when you select a template on the Cloud Control Panel. Follow these recommended guidelines to select the right type of stack:</p>

<ul>
	<li>Single-server template: All-in-one orchestration in which the database, application, and all other resources are on the same compute instance. Single-server orchestration are useful for testing or low-traffic situations where there is no intention of increasing capacity. If you think you will need greater capacity, then deploy a load-balanced multi-server template with a dedicated back-end database instead. Not all applications are offered with the single-server template.</li>
	<li>Multiple-server template: Orchestration based on a multiple-tier architecture. Multiple-server templates generally include load-balanced servers and a dedicated back-end database service. Multiple-server templates are ready for production traffic and scale more easily.</li>
	<li>Rackspace Cloud Databases or Cloud Servers with MySQL: Back-end choice is based on your needs. Cloud Databases offers a high, consistent level of performance. However, Cloud Databases does not currently offer replication or automated backups, although both features are currently in development.</li>
</ul>
