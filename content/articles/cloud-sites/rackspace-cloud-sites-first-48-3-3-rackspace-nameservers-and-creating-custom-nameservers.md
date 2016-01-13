---
node_id: 100
title: Getting Started With Cloud Sites - Rackspace Nameservers and Creating Custom Nameservers
type: article
created_date: '2011-03-09 18:53:26'
created_by: RackKCAdmin
last_modified_date: '2015-12-29 17:0247'
last_modified_by: stephanie.fillmon
products: Cloud Sites
body_format: tinymce
---

**Note**: This article is written for our [Cloud Sites Control
Panel](https://manage.rackspacecloud.com/). You can get to it from the
Cloud Control Panel by clicking your name in the upper-right corner and
selecting [Cloud Sites Control
Panel](https://manage.rackspacecloud.com/).

### Previous section

[Getting Started with Cloud
Sites](https://www.rackspace.com/knowledge_center/getting-started/cloud-sites)

To change your nameservers from your current registrar's to point to the
Rackspace Cloud:

1.  Access your account with your current registrar (godaddy.com,
    register.com, etc).
2.  Change the nameservers to **dns1.stabletransit.com** and
    **dns2.stabletransit.com**.

Your current registrar may offer "transfer lock" or a similar service as
a security measure to prevent unauthorized transfer of your domain name.
If this feature is activated, you will need to log on to your account
with your current registrar in order to unlock the domain.

To unlock the domain, you must have access to the administrative email
address you used when first registering the domain. Your current
registrar will send an email to this account that will require a reply
from you, confirming that the transfer is authorized. If you do not have
access to this email address, contact [customer
support](http://manage.rackspacecloud.com/SupportMain.do "http://manage.rackspacecloud.com/SupportMain.do")
for help. You can do a WHOIS search to find the administrative email and
the current registrar for the domain. 

All DNS changes take up to 48 hours to take effect. During this time you
can check your website by using the test URL (i.e.
www.yourdomain.com.websitetestlink.com).

**What about custom nameservers?** Let's discuss how custom nameservers
can be configured.

Configuring custom nameservers can be done differently depending on
where your DNS is currently hosted.

Below we've gathered the steps to setup custom nameservers based on some
of the most commonly used DNS providers.

+--------------------------------------------------------------------------+
| -   [GoDaddy](#GoDaddy)                                                  |
| -   [OpenSRS/Tucows/RackSpace Cloud](#OpenSRS_Tucows_RackSpace_Cloud)    |
| -   [Dotster](#Dotster)                                                  |
| -   [eNom](#eNom)                                                        |
| -   [Directi](#Directi)                                                  |
| -   [Name.com](#Name.com)                                                |
+--------------------------------------------------------------------------+

GoDaddy
-------

[Setting up Custom Nameservers in
GoDaddy](http://help.godaddy.com/article/3952 "http://help.godaddy.com/article/3952")

OpenSRS/Tucows/RackSpace Cloud
------------------------------

To register new nameservers or update existing nameservers with OpenSRS,
follow the directions below.

1.  Login to your account
    at [manage.opensrs.net](http://manage.opensrs.net/ "http://manage.opensrs.net") by
    entering your domain name, user and password, then clicking "Manage
    Domain"
2.  On the domain management page you will scroll to the bottom of the
    page where you will see a link titled "If you want to create or
    modify a nameserver which is based on yourhostdomain.com click here"
    (Ignore the nameservers link in the main top menu!)
3.  On the next page scroll down to the section titled "Create
    nameserver". In the first field enter the host prefix for you first
    server (example: ns1). In the second box enter the IP address for
    the nameserver you wish to create. Click the "Create Nameserver"
    button.
4.  Repeat step 3 for your second DNS server (ns2)
5.  You will now see your DNS servers listed on the page where you can
    edit or delete the

Dotster
-------

To register new or update current nameservers with Dotster, follow the
directions below.

1.  Open up your account information at Dotster and click the My Domains
    tab.
2.  Click the domain name you want to add the nameservers for. (not the
    checkbox)
3.  In the Name Servers section, choose the 'Register NameServer' link.
4.  Fill in the form with your nameserver name and IP address.

eNom
----

If your domain is registered with Enom, follow the directions below to
register new or update current DNS servers

1.  Log in to your account at enom.com
2.  From the site menu select.. Domains \>\> Advanced Tools \>\>
    Register a Name Server
3.  That will bring up a page with forms for adding new nameservers and
    updating old.
4.  Add the nameserver name to the form (i.e. ns1.yourdomain.com), enter
    the old IP for the DNS server (if updating), and enter the new one
    provided in your migration complete email.
5.  Click the Update button and you are done.

Directi
-------

To register new nameservers or update existing nameservers with Directi,
follow the directions below.

1.  Login to your Domain Control Panel
2.  Search for the Domain Name you wish to manage Child Name Servers for
    from Domains \>\> Search \>\> Domain Registration Search
3.  Click the domain name you want to create Child Name Servers under
4.  Click the "Manage Child Name Server" button
5.  Enter the hostname (example ns1.youhost.com) of the Child Name
    Server you wish to create in the Add New Child Name Server box, then
    enter it's IP address in the second box.
6.  To Modify a DNS server make the modifications in the IP Address text
    box and click on "Modify IP Address"

Name.com
--------

To register new nameservers or update existing nameservers with
Name.com, follow the instructions below.

1.  Log into your account.
2.  Click on the "My Account" image at the top of the page.
3.  Click on the appropriate domain name.
4.  Click on "Manage Name Servers" under the Control Panel navigation
    list.
5.  To add a new name server, enter the Host Name and IP address for
    each name server you wish to create.
6.  To modify an existing name server, enter the appropriate new IP
    address for the respective hostname and click Add. Click the
    "remove" link next to the old IP address for each hostname.

If you are hosting DNS at a provider that is not currently listed,
please contact your DNS provider for steps showing how you would be able
to configure custom nameservers.

### Next section

[Creating Sub-domains and/or domain
aliases](http://www.rackspace.com/knowledge_center/article/getting-started-with-cloud-sites-creating-sub-domains-andor-domain-aliases)

