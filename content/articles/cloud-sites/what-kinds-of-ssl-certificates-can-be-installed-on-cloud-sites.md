---
node_id: 117
title: Supported SSL certificates on Cloud Sites
type: article
created_date: '2011-03-10 17:24:46'
created_by: RackKCAdmin
last_modified_date: '2015-11-06 19:5432'
last_modified_by: kyle.laffoon
product: Cloud Sites
body_format: tinymce
---

The following SSL certificates are supported on Cloud Sites:

-   Apache + OpenSSL (PEM format).
-   Single Root Level certificates.Chained Root SSL certificates.
-   Extended Validation (EV) Certificates. See the following section for
    installation information.
-   Subject Alternative Name certificates to be used with a primary
    domain and their aliases. The common name must matchs the primary
    FQDN, and each alias must be listed as a Subject Alternative.
-   Multi-domain (UCC) and wildcard certificates. We do not directly
    support the intermediate chains required for them, because they need
    to be provided by the issuer. See the following section for
    installation information.

**Note:** Cloud Sites does not support self-signed SSL certificates.

 

Installing EV, multi-domain or wildcard certificates {.Syntax}
----------------------------------------------------

When you install EV, multi-domain or wildcard certificates, the
certificate must be installed to the name contained in the certificate's
**Common Name** field. If you are unsure what the name is,
visit https://www.sslshopper.com/certificate-decoder.html and enter the
certificate. The information is displayed as shown in the following
example:

![](/knowledge_center/sites/default/files/field/image/cert_info.png)

After installation you must point the DNS records of any domains in the
**Subject Alternative Names** field to the IP address provided for the
main site.

If you encounter any errors during installation, contact a member of our
Support team to help complete the installation.

For instruction on how to install an SSL certificate for your website on
Cloud Sites, see [Getting started with Cloud Sites: Configuring SSL on
your
websites](https://www.rackspace.com/knowledge_center/article/getting-started-with-cloud-sites-configuring-ssl-on-your-websites).

