---
node_id: 2155
title: Protect your Cloud Files CDN Bill from Unexpected Usage
type: article
created_date: '2012-09-11 19:19:57'
created_by: megan.meza
last_modified_date: '2015-09-04 19:5520'
last_modified_by: constanze.kratel
product: RackConnect
body_format: tinymce
---

When choosing to use the content delivery network (CDN) to accelerate
your website and images/videos/etc. on that website, you are responsible
for all bandwidth costs associated with delivery of your content over
the public Internet, including bandwidth incurred due to piracy.  This
article is designed to help you monitor and protect your CDN usage. 

When using the CDN, all your assets are assigned a CDN URL.  As you
probably know, your website will then have that CDN URL in its source
code and display it when a user requests to see it.  There are companies
and individuals that target website&rsquo; asset URLs and serve them without
the site owne&rsquo;s permission.  This is known as&ldquo;hot linkin&rdquo; and can
result in a massive increase to your CDN bill if the problem goes
unnoticed. 

 There are two basic ways to protect yourself, your content, and your
invoice from hot linking:  (1) constant monitoring and alerts for
abnormal CDN bandwidth usage, and (2) proactive measures to make it more
difficult to access your sit&rsquo;s source code.  &rsquo;ll review some options
of both below.

 

Monitoring/Alerting: {style="margin-left: -27.0pt;"}
--------------------

***Control Panel***

Customers can always see their current usage in the Cloud Control
Panel.  You can find this information by going to
[http://mycloud.rackspace.com](http://mycloud.rackspace.com).  Under
your username, click on the option for&ldquo;First Generation Control Pane&rdquo;

 ![Link to First Gen Control
Panel](http://www.rackspace.com/knowledge_center/sites/default/files/field/image/cfoncp_0.jpg)

 Once yo&rsquo;re in the First Generation Control Panel, you will see usage
for all your products.  These usage numbers will reflect all usage on
your current billing period.  If you are using multiple Rackspace cloud
products, you may need to scroll down to Find your Cloud Files usage. 

![Home Page
Usage](http://www.rackspace.com/knowledge_center/sites/default/files/field/image/cfusage_0.jpg)

***CDN Logs***

Every CDN customer has the ability to turn on CDN logs for their
containers that are CDN enabled.  You can easily enable these logs via
the Cloud Files API [link] or from your Cloud Control Panel at
[http://mycloud.rackspace.com](http://mycloud.rackspace.com).

![Enabling
Logs](http://www.rackspace.com/knowledge_center/sites/default/files/field/image/enablelogs_0.jpg) 

Once you have enabled CDN logs for your content, Cloud Files will create
a container for you and deliver logs to that container.  The frequency
of log delivery can vary by how heavy traffic is on the CDN, but logs
are usually delivered every four hours. 

 The log files inside of the container, named&ldquo;.CDN\_ACCESS\_LOG&rdquo; will
be prefixed with the container they are logging, followed by the date
and time stamp.   This makes it easy to find logs for a specific time
period. 

![Sample CDN Log
Container](http://www.rackspace.com/knowledge_center/sites/default/files/field/image/cfaccesslogs_0.jpg)\
 

If you find that your content has been hot linked, you can use your CDN
logs to find which URLs are compromised and take action immediately. 

 

***Third Party Log Analysis***

 There are several companies in the market that will take the hassle out
of parsing the logs in your CDN log container.  These companies take the
raw logs that Rackspace delivers to your account and make them easy to
consume and understand.  For example, they will show you peak traffic
times, geographic regions that access your data the most, etc. 

 For monitoring purposes, most of these tools allow you to set up alerts
for when usage reaches a certain level, or if it has increased by a
certain amount.  This is a great way to get monitoring without having to
code a solution yourself.

 Rackspace has two [Cloud Tools
Partners](https://cloudtools.rackspace.com/home) that provide these
features, [Cloud
Ability](https://cloudtools.rackspace.com/apps/445?1601080659) and
[QloudStat](https://cloudtools.rackspace.com/apps/399?1814232928).   

 

Hiding Source Code: {style="margin-left: -.5in;"}
-------------------

While completely hiding your source code is impossible, below are some
common tools that can serve as a first line of defense against those
looking to pirate content.  While someone with more technical knowledge
will find ways around these, it may take long enough for them to give
up. 

**No Right Click Scripts**

There are scripts that will prevent visitors from using the right-click
menu to copy your conten&rsquo;s link or view your sit&rsquo;s source code.  There
are other ways to find this information, like using the toolbar at the
top of the browser, but preventing right click can be an easy first step
to protecting yourself.  If you attempt this method, be sure to check
its functionality in a variety of browsers, as the code can be difficult
to implement across all of them. 

 **JavaScript Encryption**

The method involves taking your code, using a custom made function to
"encrypt" it somehow, and then putting it in an HTML file along with a
function that will decrypt it for the browser. While website visitors
will still be able to view your source code, they will not be able to
use it without decrypting.  There are plenty tools online that will help
encrypt your source code.  Here are some links and examples that might
be helpful. 

 
&middot;      [Encrypting Source
Code](http://www.blackbeltcoder.com/Articles/mfc/encrypting-source-code)
&middot;      [Simple Encrypting
Tool](http://www.webtoolhub.com/tn561359-html-encrypter.aspx) 
&middot;      [Article discussing options for
Encryption](http://www.htmlguard.com/articles/about-html-source-code-encryption/)

 As mentioned, this method requires the use of JavaScript, meaning that
you need to expect your legitimate website traffic to be using browsers
and settings that support it. 

 

