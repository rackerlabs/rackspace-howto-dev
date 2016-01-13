---
node_id: 130
title: Modified Medium Trust on Cloud Sites
type: article
created_date: '2011-03-15 15:49:06'
created_by: RackKCAdmin
last_modified_date: '2015-10-02 19:4107'
last_modified_by: kyle.laffoon
products: Cloud Sites
body_format: tinymce
---

undefined&rsquo;s documentation regarding
Partially Trusted Callers
[here](http://msdn.microsoft.com/en-us/library/wyts434y.aspx "http://msdn.microsoft.com/en-us/library/wyts434y.aspx")
and
[here](http://msdn.microsoft.com/en-us/library/ms364059%28VS.80%29.aspx#prtltrstpro_topic7 "http://msdn.microsoft.com/en-us/library/ms364059%28VS.80%29.aspx#prtltrstpro_topic7")
(these are components that will **NOT** work with Partially Trusted
Callers).

Many components also have support documentation concerning functioning
in a Medium Trust.

Other Items
-----------

### AspJpeg

The Rackspace Cloud has been working with Persists, the creator of
AspJpeg, to determine if their component will work under .NET in our
modified Medium Trust environment. It should be noted, however, that the
AspJpeg component is fully functional under Classic ASP.

### Configurations {.p1}

To facilitate your ability to test your applications on your local
development machine, we have made our modified Medium Trust
configuration available:\
 [Click here to download modified Medium Trust configuration file for
.NET 3.5](http://c4959820.r20.cf2.rackcdn.com/web_customtrust.config)

[Click here to download modified Medium Trust configuration file for
.NET 4.0](http://c4959820.r20.cf2.rackcdn.com/web_custom40.config)

