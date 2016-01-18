---
node_id: 130
title: Modified Medium Trust on Cloud Sites
type: article
created_date: '2011-03-15'
created_by: Rackspace Support
last_modified_date: '2016-01-13'
last_modified_by: Stephanie Fillmon
product: Cloud Sites
body_format: tinymce
---

The Rackspace Cloud&rsquo;s Windows environment operates in modified Medium
Trust.

-   [<span class="toctext">Overview</span>](#Overview)
-   [<span class="toctext">Running Applications under Medium
    Trust</span>](#Running_Applications_under_Medium_Trust)
    -   [<span class="toctext">DotNetNuke</span>](#DotNetNuke)
    -   [<span
        class="toctext">ASPDotNetStoreFront</span>](#ASPDotNetStoreFront)
    -   [<span class="toctext">Umbraco</span>](#Umbraco)
    -   [<span class="toctext">BlogEngine</span>](#BlogEngine)
    -   [<span class="toctext">mojoPortal</span>](#mojoPortal)
-   [<span class="toctext">Partially Trusted
    Callers</span>](#Partially_Trusted_Callers)
-   [<span class="toctext">Other Items</span>](#Other_Items)
    -   [<span class="toctext">AspJpeg</span>](#AspJpeg)
    -   [<span class="toctext">Configurations</span>](#Configurations)

<a href="" id="Overview"></a><span style="line-height: 1.2;">Overview</span>
----------------------------------------------------------------------------

The "trust level" refers to permissions set in the Web.config file that
dictate what operations can and cannot be performed by web applications.
Our ASP.NET 3.5 servers use the default **Medium Trust** level with the
addition of **OleDbPermission**, **OdbcPermission**,
**ConfigurationPermission**, **ReflectionPermission**, a
less-restrictive **WebPermission** and **SocketPermission** as detailed
below:

-   WebPermission Unrestricted="true"
-   OleDbPermission Unrestricted="true"
-   OdbcPermission Unrestricted="true"
-   SocketPermission Unrestricted="true"
-   ConfigurationPermission Unrestricted="true"
-   ReflectionPermission Unrestricted="true"

Using a Medium Trust level prevents applications from accessing shared
system resources and eliminates the potential for application
interference. Adding **OleDbPermission** and **OdbcPermission** allows
applications to use those data providers to access databases.
**WebPermission** is modified to allow outbound HTTP and HTTPS traffic.
**SocketPermission** is modified to allow better access to payment
services. Adding **ConfigurationPermission** allows methods or classes
to access configuration files. Adding **ReflectionPermission** allows
access to non-public types and members.

Applications operating under a Medium Trust level have no registry
access, and no access to the Windows event log. Both network and file
system access will be limited.

<span class="mw-headline"><a href="" id="Running_Applications_under_Medium_Trust"></a>Running Applications under Medium Trust</span>
------------------------------------------------------------------------------------------------------------------------------------

### <span class="mw-headline"><a href="" id="DotNetNuke"></a>DotNetNuke</span>

DotNetNuke can be installed in our modified Medium Trust environment by
following [our
guide](/how-to/install-dotnetnuke-on-cloud-sites "DotNetNuke"). If you do
encounter any issues with the installation of the CMS, please report the
issue to our support team, post in our forums, or
<a href="http://www.dotnetnuke.com/tabid/795/default.aspx" class="external text" title="http://www.dotnetnuke.com/tabid/795/default.aspx">visit DotNetNuke's community forums</a>.

### <span class="mw-headline"><a href="" id="ASPDotNetStoreFront"></a>ASPDotNetStoreFront</span>

Per
<a href="https://support.aspdotnetstorefront.com/index.php?_m=knowledgebase&amp;_a=viewarticle&amp;kbarticleid=105" class="external text" title="https://support.aspdotnetstorefront.com/index.php?_m=knowledgebase&amp;_a=viewarticle&amp;kbarticleid=105">this article at ASPDotNetStoreFront's website</a>:
"Beginning with version 7.0.2.5, the software will run in Medium Trust
natively. Customers on earlier versions than that will need to contact
<a href="http://www.aspdotnetstorefront.com/t-support.aspx" class="external text" title="http://www.aspdotnetstorefront.com/t-support.aspx">ASPDotNetStoreFront's support</a>
with their original order number for a special medium trust build."

### <span class="mw-headline"><a href="" id="Umbraco"></a>Umbraco</span>

[Umbraco](http://umbraco.com/) can be configured to run in a Medium
Trust environment.

### <span class="mw-headline"><a href="" id="BlogEngine"></a>BlogEngine</span>

BlogEngine works in our modified Medium Trust environment. If you do
encounter any issues with the installation of the CMS, please report the
issue to our support team, post in our forums, or
<a href="http://www.codeplex.com/blogengine/Thread/List.aspx" class="external text" title="http://www.codeplex.com/blogengine/Thread/List.aspx">visit BlogEngine&rsquo;s community forums</a>.

### <span class="mw-headline"><a href="" id="mojoPortal"></a>mojoPortal</span>

mojoPortal works in our modified Medium Trust environment. If you do
encounter any issues with the installation of the CMS, please report the
issue to our support team, post in our forums, or
<a href="http://www.mojoportal.com/forums.aspx" class="external text" title="http://www.mojoportal.com/forums.aspx">visit mojoPortal's community forums</a>.

<span class="mw-headline"><a href="" id="Partially_Trusted_Callers"></a>Partially Trusted Callers</span>
--------------------------------------------------------------------------------------------------------

If you do experience trust-related issues, it may relate to assemblies
that do not allow *Partially Trusted Callers*. For additional
information on this, please review Microsoft&rsquo;s documentation regarding
Partially Trusted Callers
<a href="http://msdn.microsoft.com/en-us/library/wyts434y.aspx" class="external text" title="http://msdn.microsoft.com/en-us/library/wyts434y.aspx">here</a>
and
<a href="http://msdn.microsoft.com/en-us/library/ms364059%28VS.80%29.aspx#prtltrstpro_topic7" class="external text" title="http://msdn.microsoft.com/en-us/library/ms364059%28VS.80%29.aspx#prtltrstpro_topic7">here</a>
(these are components that will **NOT** work with Partially Trusted
Callers).

Many components also have support documentation concerning functioning
in a Medium Trust.

<span class="mw-headline"><a href="" id="Other_Items"></a>Other Items</span>
----------------------------------------------------------------------------

### <span class="mw-headline"><a href="" id="AspJpeg"></a>AspJpeg</span>

The Rackspace Cloud has been working with Persists, the creator of
AspJpeg, to determine if their component will work under .NET in our
modified Medium Trust environment. It should be noted, however, that the
AspJpeg component is fully functional under Classic ASP.

### <span class="mw-headline"><a href="" id="Configurations"></a>Configurations</span> {#configurations .p1}

To facilitate your ability to test your applications on your local
development machine, we have made our modified Medium Trust
configuration available:

-   [Click here to download modified Medium Trust configuration file for
    .NET
    3.5](http://c4959820.r20.cf2.rackcdn.com/web_customtrust.config)
-   [<span>Click here to download modified Medium Trust configuration
    file for .NET
    4</span>.0](http://c4959820.r20.cf2.rackcdn.com/web_custom40.config)


