---
node_id: 4658
title: Add and manage domains in Rackspace CDN
type: article
created_date: '2015-05-08 21:51:01'
created_by: Rackspace Support
last_modified_date: '2016-01-08 17:4008'
last_modified_by: catherine.richardson
product: Rackspace CDN
body_format: tinymce
---

You can add an additional domain to your service, and you must always
create a CNAME for your service. The following sections provide
information for these steps.

### Add a domain

To add an additional domain to your service, following these steps:

1. On the **CDN Service** page in the **Domains**section, click **Add a
Domain**.

2. Select HTTP or HTTPS from **Choose Traffic Type**.

3. For HTTP traffic, enter the **Domain Name**.

4. For HTTPS traffic, select **Shared SAN Certificate** or **Shared
Rackspace Domain Certificate** from **Choose Certificate Type**. Then
enter the **Domain Name** of the domain that you want to add. For secure
domains, the name must be a single word and cannot contain periods (.),
but can contain hyphens (-).

 

![](/knowledge_center/sites/default/files/field/image/Screen%20Shot%202015-12-16%20at%203.28.18%20PM.png)

 

5. Click **Add Domain**.  In the **Domains** section, you can see the
Domain Name, along with the **Certificate Type**, and the **Status** of
the domain. Status will not show as **Active** until the SSL certificate
has been provisioned and you have set the CNAME record for the domain.
If the **Status** is **Domain Not Configured**, click on that text to
get instructions and to see the Rackspace CDN URL (see the figure below)
that you need for the CNAME record creation.

![](/knowledge_center/sites/default/files/field/image/Screen%20Shot%202015-12-16%20at%203.39.21%20PM.png)

The instructions that see see when you click on **Domain Not
Configured** are similar to those in the following figure:

![](/knowledge_center/sites/default/files/field/image/Screen%20Shot%202015-12-16%20at%203.57.27%20PM.png)

It might take some time for your DNS change to propagate across the
internet. After this has happened (based on the TTL you have set with
your DNS provider), you will be able to access your website via the CDN
edge.

For more information, see [Change DNS to enable Rackspace
CDN](https://www.rackspace.com/knowledge_center/article/change-dns-to-enable-rackspace-cdn).

 

#### [\< Create a Rackspace CDN service](https://www.rackspace.com/knowledge_center/article/create-a-rackspace-cdn-service)    -    [Work with origins and origin rules in Rackspace CDN \>](https://www.rackspace.com/knowledge_center/article/work-with-origins-and-origin-rules-in-rackspace-cdn)

 

 

