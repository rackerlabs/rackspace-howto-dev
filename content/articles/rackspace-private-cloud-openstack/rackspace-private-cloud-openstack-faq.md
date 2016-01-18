---
node_id: 4228
title: Rackspace Private Cloud FAQ
type: article
created_date: '2014-09-09'
created_by: Karin Levenstein
last_modified_date: '2016-01-04'
last_modified_by: Kyle Laffoon
product: Rackspace Private Cloud Powered by OpenStack
body_format: markdown_w_tinymce
---

### Previous section
[Getting Started with Rackspace Private Cloud - OpenStack ](/how-to/rackspace-private-cloud-openstack)

Rackspace Private Cloud is powered by OpenStack and delivers the agility and efficiency of a public cloud combined with the enhanced security, control and performance of a dedicated environment.  It can be deployed in your data center or ours, is managed by our OpenStack experts and backed by Fanatical Support®.  Rackspace Private Cloud gives you all the power of the cloud without the pain of running it, so you can focus on your core business.

Rackspace Private Cloud (RPC) consists of the Rackspace Private Cloud Software powered by OpenStack, deployed in a Customer Data Center (CDC) or at RAX based on our reference architecture and managed by a dedicated team of RPC OpenStack experts.

**General FAQ**

-   [How does Rackspace Private Cloud support Rackspace's position as the #1 managed cloud company?](#a)
-   [What new enhancements were delivered with Rackspace Private Cloud Version 11?](#b)
-   [What support services are available for Rackspace Private Cloud?](#2)
-   [Does Rackspace offer any additional services for RPC customers?](#3)
-   [What are Rackspace Private Cloud's main differentiators?](#3a)
-   [Where can I deploy Rackspace Private Cloud?](#1)
-   [Is Rackspace Private Cloud updated with each new OpenStack version release (e.g. Juno, Kilo, etc)?](#4)
-   [What is the maximum number of nodes for Rackspace Private Cloud?](#7)
-   [Does Rackspace Private Cloud come with any images?](#8)
-   [Is there a proof-of-concept offering to allow a customer to test Rackspace Private Cloud before they buy it?](#5)
-   [What devices are certified for Rackspace Private Cloud compute nodes?](#6)
-   [Where can I get more technical information?](#9)
-   [Where can I learn more?](#10)

**FAQ: Rackspace Private Cloud Solutions Templates**

-   [What are RPC solution templates?](#solutions1)
-   [Why should customers care about these templates?](#solutions2)
-   [What makes these solution templates production-ready?](#solutions3)
-   [What solution templates are available from RPC?](#solutions4)
-   [How much do the solution templates cost?](#solutions5)
-   [Are the solution templates supported by RPC?](#solutions6)
-   [Where are the solutions templates located?](#solutions7)
-   [Does Rackspace plan to offer additional templates in the future?](#solutions8)

## How does Rackspace Private Cloud support Rackspace's position as the #1 managed cloud company? {#a}
Rackspace Private Cloud supports our position as the #1 managed cloud company by offering customers managed private cloud solutions in their data center or ours.  Our team of OpenStack engineers operate our customers’ private clouds so they can focus on their core business and applications.

## What new enhancements were delivered with the July 23 launch of Rackspace Private Cloud Version 11.0? {#b}
Rackspace Private Cloud Version 11.0.0 Release Highlights:

*   Moved to the Kilo release of OpenStack (over 7,200 bugs fixed with Kilo)
*   Fully tested in-place upgrades from RPC 10+ environments
*   Refined workflow between rpc-openstack repository and OpenStack Ansible Deploy project

The following enhancements were delivered with the February 26 launch of Rackspace Private Cloud Version 10.

*   Moved to the Juno release of OpenStack (over 3,200 bugs fixed with Juno)
*   Provided an in-place upgrade path from the previous RPC release
*   Added a “Solutions” tab to the RPC/Horizon dashboard that provides a graphical interface for our customers to easily discover and deploy RPC solution templates
*   Integrated object storage (Swift) into a common control plane architecture leveraging a containerized deployment of the Swift services to enable independent scaling and seamless integration as part of a compute cloud or a stand-alone storage platform

## What support services are available for Rackspace Private Cloud? {#2}

Rackspace offers the following support service, which we define as "**Core Support**". Our support engineers will proactively monitor and maintain the health of your cloud providing installation, configuration, patching, updating, troubleshooting and resizing services.

More information is available at the [Rackspace Private Cloud web page](http://www.rackspace.com/cloud/private/).

## Does Rackspace offer any additional services for RPC customers? {#3}

Yes, Rackspace offers several additional services for RPC customers.  Customers have the option to have a Dedicated OpenStack Engineer for their account, DevOps automation services to help you unlock the full power of your cloud through automation and professional services to help you get started with and optimize your private cloud.

## What are Rackspace Private Cloud's main differentiators? {#3a}
<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/rpc-differentiators.png" width="700" alt="What differentiates Rackspace Private Cloud"  />

>### Stable & Scalable

>We offer an industry leading 99.99% OpenStack API uptime guarantee, a reference architecture that utilizes Linux containers to provide in-place upgrades and independent scaling of each OpenStack service, and a cloud that is designed to scale to hundreds of nodes.

>### Automation

>RPC is deployed using Ansible software, supports OpenStack Orchestration (Heat), can be combined with our DevOps Automation Service to help automate a customer’s process for deploying and scaling applications, and provides solution templates that enable customers to deploy production-ready application stacks in minutes.

>### Fanatical Support

>Dedicated account manager, optional dedicated OpenStack Engineer service, 15 minute live response time guarantee to any emergency ticket with Core support and 24x7x365 access to our team of OpenStack experts.

>### Deploy Anywhere

>Deploy anywhere in the world.  You can host Rackspace private cloud in your data center, in our data center, in a colocation facility or in multiple locations.

>### Expertise

>We manage one of the world’s largest OpenStack powered clouds, are #1 in all-time code contributions to the OpenStack project and offer an extensive OpenStack training curriculum.

>### Hybrid

>Add elasticity to your infrastructure with the capability to automatically add and remove public cloud resources as needed to support your private cloud workloads.


## Where can I deploy Rackspace Private Cloud? {#1}

You can deploy a Rackspace Private Cloud in your own data center, in a Rackspace data center, in a colocation facility or across multiple locations.

## Is Rackspace Private Cloud updated with each new OpenStack version release (e.g. Juno, Kilo, etc)? {#4}

Yes, Rackspace updates and releases a major version of Rackspace Private Cloud software following each OpenStack version release.  We first verify that the new OpenStack version release meets our stability requirements before launching, which typically takes about six weeks.  We also have minor releases throughout the year to introduce new features, fix bugs and provide security patches


## What is the maximum number of nodes for Rackspace Private Cloud? {#7}

Rackspace Private Cloud is designed to scale to hundreds of nodes. The maximum number depends on the specific application.

## Does Rackspace Private Cloud come with any images? {#8}

Currently, Rackspace Private Cloud Software does not include any images. For more information about downloading and creating images, refer to the [OpenStack Virtual Machine Image Guide](http://docs.openstack.org/image-guide/content/).

## Is there a proof-of-concept offering to allow a customer to test Rackspace Private Cloud before they buy it? {#5}

Rackspace has dedicated environments that are accessible to customers for proof-of-concept testing. Please contact the Rackspace Private Cloud sales team at [rpcsales@rackspace.com](mailto:rpcsales@rackspace.com).

## What devices are certified for Rackspace Private Cloud compute nodes? {#6}

All devices certified for Ubuntu Server 14.04 LTS are certified for Rackspace Private Cloud. Refer to the [Ubuntu Server certified hardware page](http://www.ubuntu.com/certification/server/) for the full list.

## Where can I get more technical information? {#9}

Get quick answers to common technical questions about Rackspace Private Cloud in [the Rackspace Private Cloud v11 FAQ](http://docs.rackspace.com/rpc/api/v11/bk-rpc-faq/content/rpc-common-front.html).

## Where can I learn more? {#10}

More information about Rackspace Private Cloud is available on the Rackspace Private Cloud web site at [http://www.rackspace.com/cloud/private](http://www.rackspace.com/cloud/private). You can also visit the Rackspace Private Cloud Forum at [https://community.rackspace.com/products/f/45](https://community.rackspace.com/products/f/45).

# FAQ: Rackspace Private Cloud Solutions templates {#solutionstemplates}

## What are RPC solution templates? {#solutions1}

They are application-stack templates built by Rackspace experts that enable customers to easily deploy a production-ready application stack on top of their OpenStack cloud.  These templates are designed to be used with OpenStack Orchestration (Heat).

## Why should customers care about these templates? {#solutions2}
Customers need to deploy applications on top of their cloud as quickly as possible to start adding business value for their end users.  The challenge is that deploying an application in the cloud can be difficult and time consuming.  It can take the average customer about two months to deploy an application, and typically their deployment ends up being a “snowflake” which isn’t automated and is difficult to reproduce.  These production-ready templates enable customers to deploy popular open-source applications on top of their private cloud in a matter of minutes.  They save customers a significant amount of time and help them quickly start adding business value.

## What makes these solution templates production-ready? {#solutions3}

The templates are built and tested by Rackspace’s OpenStack experts.  They are built using industry standards and best practices and they include software plug-ins for enhanced functionality, network isolation and firewalls for robust security, are designed for high availability (e.g. database failure, redundant caching) and are optimized via extensive performance testing.

## What solution templates are available from RPC? {#solutions4}

We currently offer eight solution templates: Magento, Drupal, Galera, MongoDB, ELK stack, Hortonworks HDP, Gerrit, and Gitlab CE.

## How much do the solution templates cost? {#solutions5}
The RPC solution templates are available for free.

## Are the solution templates supported by RPC? {#solutions6}

The solution templates are not supported by RPC.

## Where are the solutions templates located? {#solutions7}
The general public can download our solution templates at the following GitHub site: [http://rcbops.github.io/templates/](http://rcbops.github.io/templates/). As part of our v10 release, Rackspace Private Cloud customers can now discover and deploy RPC solution templates using the RPC “Solutions” tab in the Horizon dashboard.  Following is a snapshot of the RPC “Solutions” tab in Horizon:
<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/rpc-solutions-tab.png" width="700" alt="Rackspace Private Cloud Solutions tab screen shot"  />

## Does Rackspace plan to offer additional templates in the future? {#solutions8}

Yes, Rackspace plans to continue adding new solution templates to the RPC “Solutions” tab.

### Next section
[Spheres of Support](/how-to/rackspace-private-cloud-spheres-of-support)
