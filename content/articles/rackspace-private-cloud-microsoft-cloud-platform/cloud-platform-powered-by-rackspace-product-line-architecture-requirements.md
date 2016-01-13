---
node_id: 4574
title: Architecture requirements for Rackspace Private Cloud powered by Microsoft
type: article
created_date: '2015-03-02 14:51:37'
created_by: gerry.lecanu
last_modified_date: '2015-06-02 16:2244'
last_modified_by: David Hendler
products: Rackspace Private Cloud - Microsoft Cloud Platform
body_format: tinymce
---

undefined&rdquo;}
-------------------------

Base Cloud is a basic System Center 2012 R2 plus Windows Azure Pack that
allows for the minimum compliant Cloud Platform. It is composed of the
following applications and roles:

+------------+------------+------------+------------+------------+------------+------------+
| **Applicat | **VM       | **Quantity | **Software | **vCPU**   | **vRAM**   | **vDisk**  |
| ion        | name**     | **         | suite**    |            |            |            |
| or role**  |            |            |            |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Microsoft  | DB         | 2          | System     | 2          | 8 GB       | 60 GB      |
| SQL Server |            |            | Center     |            |            |            |
| Standard   |            |            |            |            |            |            |
| Edition    |            |            |            |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Operations | SCOM       | 2          | System     | 2          | 4 GB       | 60 GB      |
| Manager    |            |            | Center     |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Service    | SPF        | 2          | System     | 2          | 4 GB       | 60 GB      |
| Provider   |            |            | Center     |            |            |            |
| Foundation |            |            |            |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Virtual    | VMM        | 2          | System     | 2          | 8 GB       | 60 GB      |
| Machine    |            |            | Center     |            |            |            |
| Manager    |            |            |            |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Operations | OMRP       | 1          | System     | 2          | 4 GB       | 60 GB      |
| Manager    |            |            | Center     |            |            |            |
| Reporting  |            |            |            |            |            |            |
| Server     |            |            |            |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Orchestrat | OR         | 1          | System     | 2          | 4 GB       | 60 GB      |
| or         |            |            | Center     |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Service    | SR         | 1          | System     | 2          | 4 GB       | 60 GB      |
| Reporting  |            |            | Center     |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Service    | SM         | 3          | System     | 2          | 4 GB       | 60 GB      |
| Manager    |            |            | Center     |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Library    | LIB        | 1          | System     | 2          | 4 GB       | 1 TB       |
| Server     |            |            | Center     |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Service    | SMA        | 2          | Windows    | 2          | 4 GB       | 60 GB      |
| Management |            |            | Azure Pack |            |            |            |
| Automation |            |            |            |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Service    | SMARW      | 1          | Windows    | 2          | 4 GB       | 60 GB      |
| Management |            |            | Azure Pack |            |            |            |
| Automation |            |            |            |            |            |            |
| Reporting  |            |            |            |            |            |            |
| Worker     |            |            |            |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Management | WAPADMIN   | 1          | Windows    | 2          | 4 GB       | 60 GB      |
| Portal for |            |            | Azure Pack |            |            |            |
| administra |            |            |            |            |            |            |
| tors       |            |            |            |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Management | WAPTENANT  | 1          | Windows    | 2          | 4 GB       | 60 GB      |
| Portal for |            |            | Azure Pack |            |            |            |
| tenants    |            |            |            |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Admin      | WAPADMINAU | 1          | Windows    | 2          | 4 GB       | 60 GB      |
| Authentica | TH         |            | Azure Pack |            |            |            |
| tion       |            |            |            |            |            |            |
| Site       |            |            |            |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Admin API  | WAPADMINAP | 1          | Windows    | 2          | 4 GB       | 60 GB      |
|            | I          |            | Azure Pack |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Tenant API | WAPTENANTA | 1          | Windows    | 2          | 4 GB       | 60 GB      |
|            | PI         |            | Azure Pack |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Tenant     | WAPTENPUBA | 1          | Windows    | 2          | 4 GB       | 60 GB      |
| Public API | PI         |            | Azure Pack |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Tenant     | WAPTENAUTH | 1          | Windows    | 2          | 4 GB       | 60 GB      |
| Authentica |            |            | Azure Pack |            |            |            |
| tion       |            |            |            |            |            |            |
| Site       |            |            |            |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Active     | DC         | 2          | Windows    | 2          | 4 GB       | 160 GB     |
| Directory  |            |            | Server     |            |            |            |
| Domain     |            |            |            |            |            |            |
| Controller |            |            |            |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Remote     | RD         | 1          | Windows    | 2          | 4 GB       | 60 GB      |
| Desktop    |            |            | Server     |            |            |            |
| Services   |            |            |            |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Windows    | WSUS       | 1          | Windows    | 2          | 4 GB       | 100 GB     |
| Server     |            |            | Server     |            |            |            |
| Update     |            |            |            |            |            |            |
| Services   |            |            |            |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Active     | PKI        | 1          | Windows    | 2          | 4 GB       | 60 GB      |
| Directory  |            |            | Server     |            |            |            |
| Certificat |            |            |            |            |            |            |
| e          |            |            |            |            |            |            |
| Authority  |            |            |            |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Fileserver | FS         | 1          | Windows    | 2          | 4 GB       | 200 GB     |
|            |            |            | Server     |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+

 

The minimum system requirements to run the Base Cloud components are 60
vCPU, 136 GBs of RAM, and 3 TB of storage.  This workload is split
across two physical host servers that are configured in a failover
cluster.

Additional Cloud Platform components
------------------------------------

In addition to the Base Cloud offering, there are three optional add-on
services that you can use to enhance your Microsoft Cloud Platform at
Rackspace.  You can deploy one, two, or all three of these services. 
Keep in mind that if you add any of them, the minimum required compute
and storage needs to account for the additional compute and storage
loads.

### Web Sites Cloud {#CloudPlatformPoweredByRackspace-ProductLineArchitectureRequirements-WebSitesCloud}

Web Sites Cloud is a service that helps you provide a high-density,
scalable, shared web hosting platform for ASP.NET, PHP, and Node.js web
applications. The Web Sites Cloud service includes a customizable web
application gallery of open source web applications that integrate with
source control systems for custom-developed websites and applications.

With Microsoft SQL Server and MySQL Server, you can create the ideal
environment to leverage database as a service (DBaaS) for your company,
bringing it into the cloud era while maintaining private cloud security.
You can add one or more Microsoft SQL Server or MySQL Server instances
for tenants to deploy and use. Tenants use these databases with the Web
Sites Cloud service.

+------------+------------+------------+------------+------------+------------+------------+
| **Applicat | **VM       | **Quantity | **Software | **vCPU**   | **vRAM**   | **vDisk**  |
| ion        | name**     | **         | suite**    |            |            |            |
| or role**  |            |            |            |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Management | WAPWEBMN01 | 1          | Windows    | 2          | 4 GB       | 60 GB      |
| Server     |            |            | Azure Pack |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Controller | WAPWEBCN   | 1          | Windows    | 2          | 4 GB       | 60 GB      |
|            |            |            | Azure Pack |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Database   | WAPWEBDB   | 1          | Windows    | 2          | 4 GB       | 300 GB     |
|            |            |            | Azure Pack |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Publisher  | WAPWEBPUB  | 2          | Windows    | 2          | 4 GB       | 60 GB      |
|            |            |            | Azure Pack |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Fileserver | WAPWEBFS   | 1          | Windows    | 2          | 4 GB       | 100 GB     |
|            |            |            | Azure Pack |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Front End  | WAPWEBFE   | 1          | Windows    | 2          | 4 GB       | 60 GB      |
|            |            |            | Azure Pack |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Shared Web | WAPWEBWWS  | 1          | Windows    | 2          | 4 GB       | 60 GB      |
| Worker     |            |            | Azure Pack |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Reserved   | WAPWEBWR   | 1          | Windows    | 2          | 4 GB       | 60 GB      |
| Worker     |            |            | Azure Pack |            |            |            |
| Server     |            |            |            |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| SQL Server | SQLCLOUD   | 1          | Windows    | 2          | 8 GB       | 60 GB      |
| DBaaS      |            |            | Azure Pack |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| MySQL      | MYSQL      | 1          | Windows    | 2          | 8 GB       | 60 GB      |
| DBaaS      |            |            | Azure Pack |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| App        | AC         | 1          | System     | 2          | 4 GB       | 60 GB      |
| Controller |            |            | Center     |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+

The minimum system requirements to run the Web Sites Cloud components
are 24 vCPU, 56 GB of RAM, and 1 TB of storage.  This workload is in
addition to the Base Cloud system, which is split across two physical
host servers configured in a failover cluster.

### Service Bus {#CloudPlatformPoweredByRackspace-ProductLineArchitectureRequirements-ServiceBus}

The Service Bus service provides reliable messaging services between
distributed applications. The Service Bus service includes queued and
topic-based publish and subscribe capabilities.

+------------+------------+------------+------------+------------+------------+------------+
| **Applicat | **VM       | **Quantity | **Software | **vCPU**   | **vRAM**   | **vDisk**  |
| ion        | name**     | **         | suite**    |            |            |            |
| or role**  |            |            |            |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Service    | SB         | 1          | Windows    | 2          | 4 GB       | 60 GB      |
| Bus        |            |            | Azure Pack |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+

The minimum system requirements to run the Service Bus component are 2
vCPU, 4 GB of RAM, and 60 GB of storage.  This workload is in addition
to the Base Cloud system, which is split across two physical host
servers configured in a failover cluster.

### Active Directory Federation Services {#CloudPlatformPoweredByRackspace-ProductLineArchitectureRequirements-ADFS}

Active Directory Federation Services (ADFS) provides simplified, secured
identity federation and web single sign-on (SSO) capabilities for end
users who want to access applications within an ADFS-secured enterprise,
in federation partner organizations, or in the cloud.

+------------+------------+------------+------------+------------+------------+------------+
| **Applicat | **VM       | **Quantity | **Software | **vCPU**   | **vRAM**   | **vDisk**  |
| ion        | name**     | **         | suite**    |            |            |            |
| or role**  |            |            |            |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+
| Active     | ADFS       | 2          | Windows    | 2          | 4 GB       | 60 GB      |
| Directory  |            |            | Azure Pack |            |            |            |
| Federation |            |            |            |            |            |            |
| Services   |            |            |            |            |            |            |
+------------+------------+------------+------------+------------+------------+------------+

The minimum system requirements to run the ADFS component are 4 vCPU, 8
GB of RAM, and 120 GB of storage.  This workload is in addition to the
Base Cloud system, which is split across two physical host servers
configured in a failover cluster.

 

