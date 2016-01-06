---
node_id: 665
title: How to redirect a subdomain to a subdirectory with ASP?
permalink: article/how-to-redirect-a-subdomain-to-a-subdirectory-with-asp
type: article
created_date: '2011-03-16 21:57:40'
created_by: RackKCAdmin
last_modified_date: '2015-06-26 19:1300'
last_modified_by: kelly.holcomb
products: Cloud Sites
body_format: tinymce
---

You can redirect a subdomain to a subdirectory by using ASP or ASP.net
code.

When the requests are redirected using an ASP file, the URL in browser
for redirected domains will show the correct domain name and the
directory name where the request is being redirected. You can also
redirect the requests to a specific file.

For example:

http://subdomain1.YourHostedDomainName.com --\>
http://subdomain1.YourHostedDomainName.com/subdomain1

http://subdomain2.YourHostedDomainName.com --\>
http://subdomain2.YourHostedDomainName.com/subdomain2

http://subdomain3.YourHostedDomainName.com --\>
http://subdomain3.YourHostedDomainName.com/subdomain3/home.asp

The following is a sample script that you can use to redirect a
subdomain. You will need to place it as default document on your
document root.

    <%
    If InStr( UCase(Request.ServerVariables("SERVER_NAME")),  UCase("subdomain1.YourHostedDomainName.com") ) > 0 Then
            Response.Redirect("/subdomain1")
    ElseIf InStr( UCase(Request.ServerVariables("SERVER_NAME")), UCase("subdomain2.YourHostedDomainName.com") ) > 0 Then
            Response.Redirect("/subdomain2")
    ElseIf InStr( UCase(Request.ServerVariables("SERVER_NAME")), UCase("subdomain3.YourHostedDomainName.com") ) > 0 Then
            Response.Redirect("/subdomain3/home.asp")
    End If
    %>

Note:

1.  Replace subdomain\#.YourHostedDomainName.com with your actual
    subdomain URL.
2.  Replace /subdomain\# with your actual subdirectory name.
3.  In the last redirection statement in the example, we show how to
    redirect to a specific file.


