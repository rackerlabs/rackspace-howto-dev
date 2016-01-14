---
node_id: 5012
title: Cloud Sites - FAQ
type: article
created_date: '2015-12-10 14:41:21'
created_by: stephanie.fillmon
last_modified_date: '2016-01-11 23:1117'
last_modified_by: kyle.laffoon
product: Cloud Sites
body_format: full_html
---

Getting Started
---------------

### How do my sub-accounts access their control panel?

The Rackspace Cloud sub-account log in page can be found at
[https://www.websitesettings.com](https://www.websitesettings.com).

^[back\\ to\\ top](#top)^

### What goes in to calculating a compute cycle?

Mostly, CPU processing time. However, compute cycles also account for
the disk I/O your application's operations consume. For example, a page
with heavy database queries will consume more compute cycles in part due
to the larger volume of disk I/O it requires.

^[back\\ to\\ top](#top)^

### How do I track my compute cycle usage?

The compute cycles you use are presented in your control panel in near
real time.

^[back\\ to\\ top](#top)^

### What are compute cycles?

Compute cycles measure the amount of processing time your applications
take to execute in order to serve content to users from the Cloud Sites
environment.

^[back\\ to\\ top](#top)^

* * * * *

Account Services
----------------

### Where can I find your Acceptable Use Policy (AUP)?

You can find a copy of our
[AUP](http://www.rackspace.com/information/legal/aup), [Terms of
Service](http://www.rackspace.com/information/legal/cloud/tos) (TOS) and
[Service Level
Agreement](http://www.rackspace.com/information/legal/cloud/sla)
(SLA) on our website.

^[back\\ to\\ top](#top)^

### How many compute cycles will my applications use?

Since web applications vary so greatly, it's hard to make a perfect
guess. There are, however, some guidelines that can help. For example,
10,000 compute cycles would power approximately:

-   2.1 million page views using a database-driven content management
    system
-   11 million page views of rackspacecloud.com
-   25 million requests for a static 15KB image

^[back\\ to\\ top](#top)^

### How far can I really scale?

We currently have users pushing hundreds of millions of requests on
single domains. There are many factors that impact how easily a web
application can scale, including the application's code and its
architecture. Rackers are ready to review your web application/solution
and provide guidance on how to optimize it for Cloud Sites. If an
application is not properly built for scale, Cloud Sites will not be
able to compensate for it.

Also, if you are expecting a massive surge in traffic (perhaps your site
was featured on Oprah) please contact us via chat, phone, or ticket in
advance and we will help you prepare for it. The information we will
need can be found at the end of the article [Optimize your website on
Cloud
Sites](http://www.rackspace.com/knowledge_center/article/optimize-your-website-on-cloud-sites). 

^[back\\ to\\ top](#top)^

### What happens if I exceed the included amount?

While most customers will fall well below the included amount, we have
created fair and simple pricing beyond the base amount that means you
pay ONLY for what you use and nothing more. There are no onerous
penalties for exceeding the included plan amounts. The prices for all
scaling metrics can be found on the [Cloud Sites pricing
page](http://www.rackspace.com/cloud/sites).

^[back\\ to\\ top](#top)^

### What is included for \$150?

We have included enough resources in the Cloud Sites base package to
power most business needs. You get 50 GB of high performance storage as
well as 500 GB of bandwidth permonth. In addition, Cloud Sites uses
compute cycles to monitor your computing usage. You get 10,000 compute
cycles per month across all your sites and applications. Unlike many
hosting companies, the Rackspace Cloud will never cut you off for using
what we sell you.

The base package does not include the cost of MySQL/MSSQL database
storage, SSL, or domain registration. More details can be found on our
[pricing page](http://www.rackspace.com/cloud/sites).

^[back\\ to\\ top](#top)^

### I've had shell access (SSH) in the past. Why isn't it offered on Cloud Sites?

Shell access (also commonly known as SSH) is not offered on Cloud Sites,
primarily for security reasons. Keep in mind, however, that many
functions typically accessed via shell are available on the Rackspace
Cloud, including cron jobs, file permissions, and unzip. You can also do
many SSH type functions by mounting your FTP location locally using
SSHFS. More information can be found
[here](https://www.rackspace.com/knowledge_center/article/getting-started-with-cloud-sites-ftpsshfsftp-clients). 

^[back\\ to\\ top](#top)^

### Will Rackspace ever suspend my site if it receives tons of visitors?

Rackspace will never suspend a site as long as the traffic is legitimate
and the hosted content doesn't violate our TOS or our AUP. As a company,
we succeed when you succeed, so we will always encourage legitimate
traffic to your sites. We have several domains on Cloud Sites that
receive millions of hits each month. We have never limited or throttled
their accounts, as that is one of the many benefits of going with a
cloud offering like the Rackspace Cloud Sites service. On the other
hand, we will stop illegitimate spikes in traffic, such as runaway
scripts or DDOS attacks.

^[back\\ to\\ top](#top)^

### Can I use Cloud Sites as an audio or video encoder?

Audio and video encoding is a task that is better suited for a Cloud
Server. Cloud Sites was built to be a highly specialized and optimized
computer cluster for serving web content. That means that it is not
really designed for audio processing, video processing, or streaming
tasks. You can have some audio or video content on Cloud Sites, but the
service was not designed to be a processing farm for audio conversion,
video conversion, or a Shoutcast system to use for live audio streaming.
See [FFMPeg on Cloud
Servers](https://www.rackspace.com/knowledge_center/article/ubuntu-intrepid-installing-ffmpeg).

^[back\\ to\\ top](#top)^

### Can I host adult content sites on Cloud Sites?

Please refer to our Acceptable Use Policy for details on what content
can be hosted with us. You can find a copy of our
[AUP](http://www.rackspace.com/information/legal/aup) on our website.

^[back\\ to\\ top](#top)^

* * * * *

Compromised Sites
-----------------

### What is a domain compromise?

A domain compromise is when a domain has been exploited for various
reasons. That is, a domain using exploitable code becomes infected with
a code injection and proceeds to send out email without the owner's
knowledge, infect visitors with malware, or perform other malicious
activity.

^[back\\ to\\ top](#top)^

### What can I do to avoid a domain suspension resulting from a domain compromise?

To avoid suspension, you may not use the Cloud Sites platform or
services to knowingly or unknowingly store, execute, promote, or
facilitate malicious content or action to include:

-   Mail spam
-   Code or file injection
-   Outbound DDOS attacks
-   Personally identifiable information scraping
-   Brute force attacks
-   MySQL/MSSQL spam request

^[back\\ to\\ top](#top)^

### How can I get my domain unsuspended?

Following suspension, domains cannot be activated until all listed files
are removed from our systems and the domains pass a security scan
performed by our team. Due to the security of other customers, domains
will not be activated if they do not meet these criteria.

^[back\\ to\\ top](#top)^

### What if a domain is compromised and it was not my fault? Will I get a credit from this issue?

Domains and their content are the responsibility of their owner. If
domains are compromised, the final responsibility will be with the
owner. Accounts will not be eligible for credits due to interruptions of
service resulting from any AUP violation.

^[back\\ to\\ top](#top)^

### Why doesn't Cloud Sites keep my domains secure?

Cloud Sites is a platform-as-a-service web hosting product. We manage
the infrastructure and you manage your domains' data and content. While
our systems will conduct scans for malicious activity, we do not enforce
minimum requirements on content management systems or conduct code
audits to ensure security. We do, however, recommend keeping the content
up-to-date.

^[back\\ to\\ top](#top)^

### How can I increase the security of my domains?

We are committed to ensuring the security of our infrastructure and the
reputation of our hosting environment. Additional resources you may
utilize to improve your security posture are third party products. There
are many resources out in the marketplace if you search for the security
of your website. Many popular content management systems (CMS) also
recommend specific security plugins.

^[back\\ to\\ top](#top)^

* * * * *

Security
--------

### How do I deny certain IP addresses from accessing my site on Cloud Sites?

Visitors to a Cloud Sites website come through our load balancers, which
means the IP address reported to your site will be that of our load
balancers. We store the visitor's IP address in the
**X-Cluster-Client-Ip** variable to work around this behavior. The value
of **X-Cluster-Client-Ip** can be used when configuring allow and deny
rules.

For instructions, see [Controlling access to Linux Cloud Sites based on
the client IP
address](https://www.rackspace.com/knowledge_center/article/controlling-access-to-linux-cloud-sites-based-on-the-client-ip-address).

^[back\\ to\\ top](#top)^

* * * * *

Backups
-------

### How often do Cloud Sites backup information?

The entire Cloud Sites FTP structure is backed up in an [FTP
Snapshot](https://www.rackspace.com/knowledge_center/article/ftp-snapshot)
at the top of every hour, going back 32 hours. Those backups are rolled
into a nightly backup, which are retained for two days. However, these
backups are for disaster recovery on the server side. If for any reason
a storage node on our side were to crash, our backups will be there to
replace any lost data.

That said, we recommend that you make periodic backups of your site and
data to your local computer since we are unable to extract an individual
site's data from the nightly backups. If you need a backup of your MySQL
or MS SQL databases, they can be exported through our online utilities
(MySQL or MS SQL) or by connecting directly to the servers using desktop
software.

^[back\\ to\\ top](#top)^

### What does Rackspace use for a storage system? Have you done anything there to make it redundant?

Nothing as important as your website should be served from a single hard
drive, but you'd be surprised by how many web hosts have little more
redundancy than a pair of crossed fingers. We're different - and for
good reason.

The advanced architecture powering our hosting solution uses groups of
high-performance, network-attached storage devices to reliably serve
every web page, image, and email. Inside each storage device, drives are
mirrored to each other in a RAID configuration to create a first level
of redundancy. And, as a final precautionary measure, all data on the
system is automatically backed up on a repeating schedule.

^[back\\ to\\ top](#top)^

* * * * *

Web Servers
-----------

### How do I set up error pages for my PHP site?

You can use a .htaccess file to create custom error pages for your sites
defaulted to PHP.

    ErrorDocument "code" "location of error document"

For example, with a 404 error:

    ErrorDocument 404 /404.html

You can use this directive to create error pages for other error codes
as well. You will need to specify the path to the error page relative to
the location of the .htaccess file. For more information, see the
[Comprehensive guide to
.htaccess](http://www.javascriptkit.com/howto/htaccess2.shtml).

^[back\\ to\\ top](#top)^

### How do I stop PHP scripts from executing in a directory?

Include the following line in an .htaccess file placed in the directory
you want to stop scripts:

    removehandler .php

Then add the file extensions you wise to stop.

^[back\\ to\\ top](#top)^

### How do I enable directory listing in PHP?

In an .htaccess file, insert the following line:

    Options +Indexes

Directory listing is disabled by default on our system.

^[back\\ to\\ top](#top)^

### How do I change the PHP memory limit value?

Include this line in an .htaccess file in the same directory as the
script:

    php_value memory_limit ?M

Replace "?" with the appropriate megabyte value. Our default size is set
to 128 MB, and a successful modification of the memory limit will show
in your PHP info file. For more information, see [How can I view server
configuration information for
PHP?](https://www.rackspace.com/knowledge_center/article/view-server-configuration-information-for-php)

^[back\\ to\\ top](#top)^

### How do I change the PHP maximum upload file size?

In an .htaccess file in the same directory as the upload script, include
this line:

    php_value upload_max_filesize ?M

Replace "?" with the applicable value. Our default size is set to 8 MB
and a successful modification of the max upload size will show in your
PHP info file.

If you're running WordPress and continue to have problems after
increasing the upload\_max\_filesize value, you can try adding these
settings as well:

    php_value post_max_size ?M
    php_value max_execution_time 200
    php_value max_input_time 200

If you are continuing to encounter issues, please contact support.

^[back\\ to\\ top](#top)^

### How can I view any PHP errors?

On a PHP-based site, a blank white screen is usually indicative of a PHP
error. By default, Cloud Sites will store PHP errors under
the **/log** folder in FTP to a file named **php\_errors.log**.

To view the error on the page itself, you can create or edit an
.htaccess file in the same directory as the executing script or content,
and include these lines:

    php_flag display_errors 1
    php_value error_reporting 8191

If you are continuing to encounter issues, please contact support.

^[back\\ to\\ top](#top)^

### How do I change the PHP maximum execution time?

In an .htaccess file in the same directory as the executing script,
include this line:

    php_value max_execution_time ?

Replace "?" with the value you need to for the maximum execution time in
seconds. Our default time is set to 30 seconds and a successful
modification of the maximum execution will show in your PHP info file.

^[back\\ to\\ top](#top)^

### How do I change the default character set for PHP?

In an .htaccess file placed in the directory you want to have the
character set changed on, include this line:

    php_value default_charset ?

Replace "?" with the character set required for your site, such as
ISO-8859-1.

**Note**: Cloud Sites has a default character set of UTF-8 if otherwise
unspecified in your .htaccess file.

^[back\\ to\\ top](#top)^

### How do I change the post max size value?

In an .htaccess file in the same directory as the executing script,
include this line:

    php_value post_max_size ?M

Replace "?" with the required value needed, such as 16. Our default
post\_max\_size value is set to 8 MB.

^[back\\ to\\ top](#top)^

### How do I prevent hotlinking on Cloud Sites?

Using the .htaccess file, you can prevent hotlinking--presenting
pictures, videos, or other media from one site on another by means for a
link--by denying access to specific files based on the domain requesting
the file. Hotlinking makes the person who hosts the media pay for the
bandwidth to present it, while not getting any of the viewers on her own
website. You can deny domains who would hotlink your media by using
**mod\_rewrite**, so don't forget to use RewriteBase.

**Fully denying**

Below is an example that will only allow **.gif**, **.jpg**,
and **.png** files to be accessed
from **www.example.com** and **example.com**:

    RewriteEnging on
    RewriteBase /
    RewriteCond %{HTTP_REFERER} !^http://(www\.)?example.com/.*$ [NC]
    RewriteRule \.(gif|jpg|png)$ - [F]

Using the above example, another website embedding one of your .gif,
.jpg or .png images would see a broken image or the alt text specified
in the img tag.

**Denying with another image**

If you want to be even more creative, you can even submit a different
image to the other website, such as one that reads *Stop Hotlinking or
Stop Stealing My Bandwidth!* Replacing the images with one like that
will usually deliver the right message to the offenders and you could
even advertise your own site if you make a custom image--though the
above example will ultimately save you more bandwidth since it denies
the image altogether. Below is an example that will only allow **.gif**,
**.jpg** and **.png** files to be accessed from **www.example.com** and
**example.com**, while serving **hotlinking.png** to any other websites
requesting these files:

    RewriteEngine on
    RewriteBase /
    RewriteCond %{HTTP_REFERER} !^http://(www\.)?example.com/.*$ [NC]
    RewriteCond %{REQUEST_URI} !^/hotlinking.png$ [NC]
    RewriteRule \.(gif|jpg|png)$ http://www.example.com/hotlinking.png [R,L]

Using the above example, another website embedding one of your images
would see **hotlinking.png** instead.

^[back\\ to\\ top](#top)^

### How can I password protect my Cloud Sites website?

You can password protect your website, or any of its directories,
through basic authentication using a .htaccess file. PHP must be set as
the default technology for a site in order to utilize a .htaccess file.
If used on a site where ASP is also an enabled technology, please be
aware that this will not protect ASP pages.

**Create the .htaccess file**

This file sets up the requirement for basic authentication and also
points to the file containing a list of authorized users.

-   Open a simple text editor, such as Notepad
-   Insert the following code:

<!-- -->

    # The name of the area
    AuthName "Name of Password Protected Area"
     
    # Type of authentication. Always basic
    AuthType Basic
     
    # Path to .htpasswd file for the site.
    # It's preferable to not have this in any
    # of the site's content directories.
    AuthUserFile /mnt/Target01/[DDI_ID]/[CLIENT_ID]/[WEBSITE_NAME]/.htpasswd
     
    # The requirements to view the site. This
    # requires that the browser provide
    # credentials matching on of the users in
    # the .htpasswd file specified above.
    Require valid-user

-   Replace the text inside of the quotation marks on the AuthName line
    to the name of your password protected area (Ex. AuthName "My
    Password Protected Directory").
-   The text after AuthUserFile must be changed to match your site's
    server side path to a .htpasswd file we will create soon (Ex.
    /mnt/Target01/000000/www.mywebsite.com/web/content/.htpasswd).
-   Save the file as "htaccess.txt" and upload it to the directory you
    want protected.
-   Rename the file to ".htaccess".

**Create the .htpasswd file**

This file will contain a list of usernames and password sets. Each line
should contain one set and the username and password should be separated
by a colon.

1.  Open a simple text editor, such as Notepad
2.  Use a .htpasswd encryption tool, such as the one available
    [here](http://www.htaccesstools.com/htpasswd-generator/). This will
    automatically generate the content for the .htpasswd file
3.  Copy the output of the encryption tool to your text editor
4.  Save the file as "htpasswd.txt" and upload it to your site to the
    path you are pointing to in the .htaccess file
5.  Rename the file to ".htpasswd"

Following these steps will setup basic authentication password
protection to the directory indicated. If you are unable to view the
.htaccess and .htpasswd files after you renamed them, you will need to
configure your FTP client to view hidden files.

^[back\\ to\\ top](#top)^

### How do I use a .htaccess file?

For a comprehensive explanation on how to use a .htaccess file and how
to create one, please see one or both of the following links:
.htaccess-Guide.com's [How to use
.htaccess](http://www.htaccess-guide.com/how-to-use-htaccess/) and
JavascriptKit.com's [Comprehensive guide to
.htaccess](http://www.javascriptkit.com/howto/htaccess.shtml).

^[back\\ to\\ top](#top)^

### Why is mod\_rewrite not working on my site?

On Cloud Sites, due to our unique hosting environment, we require a
slight addition to the code used for mod\_rewrite. You will also need to
make sure that the site is using either PHP4 or PHP5 as the default
technology.

In the .htaccess file containing your rewrite rules, add the following
lines:

    RewriteEngine on
    RewriteBase /

Depending on the application, you may need to further specifiy the
RewriteBase / to include the subdirectory the application is installed
in. For example:

    RewriteBase /subdirectory

You can find more information on mod\_rewrite at [Apache's
website](http://httpd.apache.org/docs/2.0/mod/mod_rewrite.html).

^[back\\ to\\ top](#top)^

### How do I enable SSI?

 

You can activate Server Side Includes (SSI) by using .htaccess with the
following directives:

    AddType text/html .shtml
    AddHandler server-parsed .shtml
    Options Indexes FollowSymLinks Includes

**Note**: You cannot serve PHP content using SSI. For PHP content, we
recommend using PHP's include or require statements or using an inline
frame, such as shown in the following example:

    <html>
    <head></head>
    <body>
    <iframe src="/test.php"> </iframe>
    </body>
    </html>

^[back\\ to\\ top](#top)^

### How do I change the default character set for HTML?

In an .htaccess file placed in the directory you want to have the
character set changed on, include the following lines:

    AddDefaultCharset ?
    # Or AddType 'text/html; charset=?' html
    DefaultLanguage en-US

Replace the "?" with the character set required for your site, such as
UTF-8.

**Note**: Cloud Sites has a default character set of UTF-8 if otherwise
not specified in .htaccess

^[back\\ to\\ top](#top)^

### How can I do a 301 redirect?

**Note**: The following examples are specific to PHP technology and will
only work if the Cloud Site is configured to utilize this technology.
This will not work for IIS (ASP / ASP.NET).

Please see this article for converting a site from Windows (IIS) to
Linux (PHP) technology: [Change your site's default
technology](https://www.rackspace.com/knowledge_center/article/change-your-sites-default-technology).

You can also view this article for assistance with rewriting from
ASP.NET: [How do I rewrite URLs from
ASP.NET?](https://www.rackspace.com/knowledge_center/article/how-do-i-rewrite-urls-from-aspnet-on-cloud-sites)

^[back\\ to\\ top](#top)^

### How do I install my own PEAR module?

You can deploy PEAR modules and other useful scripts locally on your
site by modifying [PHP's
include\_path](http://php.net/manual/en/ini.core.php). The default
include\_path on a Cloud Site is:

    .:/usr/share/pear:/usr/share/php

To add another location for PHP to search for modules, just append a
directory separator (colon) and the path to your PEAR modules. For
example, you might add this to your .htaccess:

    php_value include_path ".:/usr/share/pear:/usr/share/php:/mnt/stor1-wc1-dfw1/123456/www.domain.com/web/pear_modules"

You will want to change the path in the example above to use your
website's absolute path. Please see [this
article](http://www.rackspace.com/knowledge_center/article/locate-the-linux-path-for-your-cloud-sites-website)
to locate your website's absolute path.

Your website's absolute path should resemble this:
**/mnt/stor1-wc1-dfw1/123456/www.domain.com/web/content**.

**Install the modules**

Following the above example, you would login to your FTP and create a
directory at the location: **/www.domain.com/web/pear\_modules**.

Then you would place the PEAR modules into this directory.

**Use the modules**

Now when you reference your modules in your script using a PHP function
like include() or require(), the server will know where to look for
them.

^[back\\ to\\ top](#top)^

* * * * *

Web Technologies
----------------

### How can I implement an e-commerce site?

While Cloud Sites is not designed for credit card storage and is not PCI
compliant, it can be used as a flexible front-end to a payment gateway.
For more information, see our article on [utilizing Cloud Sites in an
e-commerce
solution](https://www.rackspace.com/knowledge_center/article/how-to-utilize-cloud-sites-in-an-e-commerce-solution).

^[back\\ to\\ top](#top)^

* * * * *

Billing
-------

### How can I cancel my Cloud Sites account?

To cancel your Cloud Sites account, you must complete the cancellation
from the Cloud Sites Control Panel.

1.  Log in to the [Cloud Sites Control
    Panel](https://manage.rackspacecloud.com/).
2.  Click **Your Account** and then click **Cancel Account**.
3.  Complete the cancellation form and then click **Submit**.

If you want to cancel your Cloud Sites subscription but leave the
account open for Cloud Servers or other products, open a support ticket
for this request.

1.  Log in to the [Cloud Sites Control
    Panel](https://manage.rackspacecloud.com/).
2.  At the top of the window, click **Tickets**.\
     You are redirected to the Support Tickets page in the Cloud Control
    Panel.
3.  Click **Create Ticket**.
4.  Complete the form and then click **Submit Ticket**.

^[back\\ to\\ top](#top)^

### Is there a referral bonus or any discounts available?

Please visit [our website](http://www.rackspace.com/cloud/partners/) for
updates on the referral program.

^[back\\ to\\ top](#top)^

### Will there be a discount if I prepay for a full year?

We currently only offer month-to-month billing terms. It's our belief
that we have to earn your business every month.

^[back\\ to\\ top](#top)^

### How can I found out if a bill wasn't collected or a payment wasn't processed?

You can access billing information for Cloud Sites by clicking **Your
Account** \> **Billing**in the Cloud Sites Control Panel. This action
opens the Billing & Payments section of the Cloud Control Panel. This
section displays important information like your total outstanding
balance, the date of your most recent invoice, and which credit card is
being used for payments on the account.

-   The Recent Activity section lists a summary of your most recent
    invoice. This summary includes the date and amount of your most
    recent invoice and your current balance.
-   In the Payment Information section, you can update your billing
    information and change the credit card attached to the account.
-   The Billing History section displays a summary of your invoice
    history. Click an ID number for an invoice to view additional
    information or download the invoice in your preferred format.

^[back\\ to\\ top](#top)^

### When am I billed for my account?

When you sign up for products under the Managed Infrastructure, Managed
Operations SysOPs, or Managed Operations DevOps Automation service
levels, your credit card is charged a US \$1.00 authorization charge to
confirm it is an active card. The authorization charge returns to your
card normally within 24-72 hours.

Thirty days after you sign up, your first invoice is processed. Your
charges consist of service usage accrued within the first 30 days.
**Note**: The exception is Cloud Sites, which charges for the first 30
days at sign up and continues to charge in advance of monthly usage.

After the first billing cycle, you are billed every month on the same
date that you first signed up for service. If you have any questions
about account billing, call us at 1-877-934-0410.

^[back\\ to\\ top](#top)^

### What information will appear on my credit card invoice?

Any payments made to Rackspace will be listed as **Rackspace Cloud** on
your credit card statement.

^[back\\ to\\ top](#top)^

### What forms of payment does Rackspace accept?

At this time, Rackspace only accepts credit card payments. We allow
payment by Visa, MasterCard, and American Express.

^[back\\ to\\ top](#top)^

### Is there a discount if I purchase multiple hosting accounts with Rackspace?

No, at this time we do not offer a discount if you purchase multiple
accounts.

^[back\\ to\\ top](#top)^

### I live outside the United States. Can I use my foreign credit card to pay for my account?

Yes, international credit cards are accepted. We allow payment by Visa,
MasterCard, and American Express.

^[back\\ to\\ top](#top)^

### How do I update my billing information?

Use the following instructions to change your credit card and billing
information from the **Cloud Sites Control Panel**.

**To change credit card information**

1.  Log in to your control panel at
    [https://mycloud.rackspace.com](https://mycloud.rackspace.com/).
2.  In the left navigation menu, click **Your Account** \> **Billing**.\
     You are redirected to the Billing & Payments section of the Cloud
    Control Panel.
3.  To edit your credit card, click **Edit Credit Card** under Payment
    Information.
4.  When you are done making changes, click **Save Credit Card.**

**To edit billing information**

1.  Log in to your control panel at
    [https://manage.rackspacecloud.com](https://manage.rackspacecloud.com/).
2.  In the left navigation menu, click **Your Account** \>**Billing**.\
     You are redirected to the Billing & Payments section of the Cloud
    Control Panel.
3.  Click the pencil icon next to **Billing Address.**
4.  When done making changes, click **Save Contact**.

Use the following instructions to change your credit card and billing
information from the **Cloud Control Panel**.

**To change credit card information**

1.  Log in to your control panel at
    [https://mycloud.rackspace.com](https://mycloud.rackspace.com/).
2.  Open the **Account:**menu in the top right corner of the screen, and
    click **Billing & Payments**.\
     The Billing & Payments section is displayed.
3.  To edit your credit card, click **Edit Credit Card** under Payment
    Information
4.  When you are done making changes, click **Save Credit Card.**

**To edit billing information**

1.  Log in to your control panel at
    [https://mycloud.rackspace.com](https://mycloud.rackspace.com/).
2.  Open the **Account:**menu in the top right corner of the screen, and
    click **Billing & Payments**.\
     The Billing & Payments section is displayed.
3.  Click the pencil icon next to **Billing Address.**
4.  When done making changes, click **Save Contact**.

^[back\\ to\\ top](#top)^

### Am I charged bandwidth for FTPing data to or from my Cloud Sites?

No, FTP bandwidth does not count against your monthly transfer.

^[back\\ to\\ top](#top)^

* * * * *

Linux and PHP
-------------

### What are the PHP configuration limits for Cloud Sites?

The maximum values for PHP configuration options via .htaccess are:

-   Memory (**memory\_limit**): 512M
-   Upload size (**upload\_max\_filesize**): 550M
-   Execution time in seconds (**max\_execution\_time**): 30

**Note**: Under some circumstances, PHP may grant an additional 30
seconds to a process that is still executing at the 30 second mark.

^[back\\ to\\ top](#top)^

### What version of Linux does Cloud Sites run? What about for Windows?

Cloud Sites removed the ability to host disparate technologies due to
changes in our technology options. The hybrid technology option removal
allows us to release new changes more quickly.

^[back\\ to\\ top](#top)^

* * * * *

MySQL
-----

### How do I import a large MySQL database?

You should be able to use the *Online Manager* (see [PHPmyAdmin Database
Management
Interface](/knowledge_center/index.php/Working_with_a_MySQL_database "Working with a MySQL database"))
to import databases that are less than 16 MB in size without issue.

However, if you need to import database data that exceeds 16 MB into
your Cloud Sites environment, you can use a script which you can
schedule via a cron job.

Following is an example to help you set up this script:

    #!/bin/sh
    mysql -h DB_HOST -u DB_USER -p'DB_PASSWORD' DB_NAME < /path/to/file/db_import.sql

1.  Create a new text file, add the preceding code to it, and save it as
    restore.sh. In the preceding script, replace the placeholders with
    your actual information, as follows:
    -   *pathToFile*&mdash;This is the absolute path to your files. You can
        find this path by clicking on Hosting \> Cloud Sites \> Features
        in the Cloud Sites Control Panel and scrolling down the page.
        This path is the Linux Path listed there. An example is
        /mnt/target02/123456/www.domain.com. (Note that the file name is
        not included in this path.)

    -   *databaseHost* - The name of the database host. An example is
        mysql5-9.wc1.

    -   *database*User - The name of the database user.

    -   databae\_Password - The password of the target database.

    -   *databaseName* - The name of the database to which you are
        restoring.

2.  Upload this file to your Cloud Site (for security purposes, we
    recommend keep this file outside your webroot) and create a "perl"
    cron job to schedule the task (the perl option runs shell scripts as
    well). For instructions on how to create a cron job, see
    [How\_do\_I\_enable/disable\_a\_cron\_job?](/knowledge_center/index.php/How_do_I_enable/disable_a_cron_job%3F "How do I enable/disable a cron job?").\
     **Note**: For security purposes, we recommend that you keep this
    file outside your webroot directory.
3.  Put the name of the file, which in this example is import.sh, in the
    "Command To Run" field.
4.  Select **Perl** as the Command Language and then select the minimum
    interval at which you want to run that script (5 minutes is
    recommended).\
     Logs are available in your `/logs/` folder each time a cron job is
    performed and you receive an email confirmation informing you if the
    job was successful or not.

**Note**: The cron job has 15 minutes to complete. If the script takes
longer than 15 minutes to complete, it will time out. If this is a
problem for you please break up the import into smaller pieces (several
.sql files) and reschedule the job as necessary.

For more information about cron and related tasks, please see the
following articles:

**Cron FAQ's:**

-   **[What is a cron
    job?](/knowledge_center/index.php/What_is_a_cron_job%3F "What is a cron job?")**
-   **[How do I enable/disable a cron
    job?](/knowledge_center/index.php/How_do_I_enable/disable_a_cron_job%3F "How do I enable/disable a cron job?")**
-   **[How do I schedule a cron
    job?](/knowledge_center/index.php/How_do_I_schedule_a_cron_job%3F "How do I schedule a cron job?")**
-   **[How do I create a cron job to backup my MySQL
    database?](/knowledge_center/index.php/How_do_I_create_a_cron_job_to_backup_my_MySQL_database%3F "How do I create a cron job to backup my MySQL database?")**

^[back\\ to\\ top](#top)^

 

 

