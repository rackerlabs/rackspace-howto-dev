---
node_id: 518
title: ASP/.NET Integrated Mode on Cloud Sites
type: article
created_date: '2011-03-16 21:57:40'
created_by: RackKCAdmin
last_modified_date: '2011-09-07 15:2109'
last_modified_by: matt.wheeler
products: Cloud Sites
body_format: tinymce
---

undefined&rsquo;s web.config:

\<system.webServer\>

      <security>
          <requestFiltering>
              <requestLimits maxQueryString="NEW_VALUE_IN_BYTES" />
          </requestFiltering>
      </security>

\</system.webServer\>

\
 DefaultHttpHandler is not supported. Applications relying on
sub-classes of DefaultHttpHandler will not be able to serve requests.

If your application uses DefaultHttpHandler or handlers that derive from
DefaultHttpHandler, it will not function correctly. In Integrated mode,
handlers derived from DefaultHttpHandler will not be able to pass the
request back to IIS for processing, and instead serve the requested
resource as a static file. Integrated mode allows ASP.NET modules to run
for all requests without requiring the use of DefaultHttpHandler.

Change your application to use modules to perform request processing for
all requests, instead of using wildcard mapping to map ASP.NET to all
requests and then using DefaultHttpHandler derived handlers to pass the
request back to IIS.

Source:
[http://mvolo.com/blogs/serverside/archive/2007/12/08/IIS-7.0-Breaking-Changes-ASP.NET-2.0-applications-Integrated-mode.aspx](http://mvolo.com/blogs/serverside/archive/2007/12/08/IIS-7.0-Breaking-Changes-ASP.NET-2.0-applications-Integrated-mode.aspx "http://mvolo.com/blogs/serverside/archive/2007/12/08/IIS-7.0-Breaking-Changes-ASP.NET-2.0-applications-Integrated-mode.aspx")

