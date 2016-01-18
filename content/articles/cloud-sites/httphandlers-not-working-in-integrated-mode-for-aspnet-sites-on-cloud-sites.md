---
node_id: 118
title: HttpHandlers not working in integrated mode for ASP.NET sites on Cloud Sites
type: article
created_date: '2011-03-10'
created_by: Rackspace Support
last_modified_date: '2015-05-06'
last_modified_by: Kelly Holcomb
product: Cloud Sites
body_format: tinymce
---

If your website is running in
<a href="http://www.code-magazine.com/Article.aspx?quickid=060103" class="external text" title="http://www.code-magazine.com/Article.aspx?quickid=060103">integrated mode</a>,
you might have noticed that your
<a href="http://msdn.microsoft.com/en-us/library/aa903367(VS.71).aspx" class="external text" title="http://msdn.microsoft.com/en-us/library/aa903367(VS.71).aspx">HttpHandlers</a>
no longer function even though they are set in your **web.config** file.

Explanation
-----------

This behavior is expected because integrated mode changed the way that
modules and handlers are defined in the **web.config** file, compared to
classic mode in IIS 7 or IIS 6. Integrated mode is the default for IIS 7
and currently the default for all new IIS/ASP.NET websites created in
the Rackspace Cloud. If your website code was originally written for
classic mode or using IIS 6, the **web.config** file might need to be
updated.

Solutions
---------

-   Peter Kellner's article,
    <a href="http://peterkellner.net/2008/09/06/iis7-httphandlers-handlers-integrated-mode-webfarm/" class="external text" title="http://peterkellner.net/2008/09/06/iis7-httphandlers-handlers-integrated-mode-webfarm/">How to use HttpHandlers such as .ashx files with IIS7 Integrated Mode</a>,
    briefly covers the differences between the *old way* to set up
    handlers and the *new way*.
-   The Microsoft Developer Network also explains
    <a href="http://msdn.microsoft.com/en-us/library/46c5ddfy.aspx" class="external text" title="http://msdn.microsoft.com/en-us/library/46c5ddfy.aspx">how to set up HttpHandlers for each of the above situations</a>.
    This article covers the differences in detail.


