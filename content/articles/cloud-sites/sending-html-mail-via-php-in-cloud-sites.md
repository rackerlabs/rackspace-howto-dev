---
node_id: 3838
title: Sending HTML Mail via PHP in Cloud Sites
type: article
created_date: '2013-12-18'
created_by: Bryon Farris
last_modified_date: '2013-12-19'
last_modified_by: Ross Diaz
product: Cloud Sites
---

*This article is an expansion of an existing article regarding basic
SMTP authentication with PHP, which can be found
[here](/how-to/test-php-smtp-functionality). *

Within the Cloud Sites environment, it is possible to craft an HTML
formatted email message for delivery when using SMTP authentication for
delivery by making use of the built in Mail\_Mime function provided by
the PHP Pear framework.

**Sending HTML Enabled Mail via SMTP**

The following variables will need to be adjusted as needed:

-   <span style="line-height: 1.538em;" data-mce-mark="1">\$from</span>
-   <span style="line-height: 1.538em;" data-mce-mark="1">\$to</span>
-   <span style="line-height: 1.538em;"
    data-mce-mark="1">\$subject</span>
-   <span style="line-height: 1.538em;" data-mce-mark="1">\$text</span>
-   <span style="line-height: 1.538em;" data-mce-mark="1">\$html</span>
-   <span style="line-height: 1.538em;" data-mce-mark="1">\$file</span>
-   <span style="line-height: 1.538em;"
    data-mce-mark="1">\$mimetype</span>
-   <span style="line-height: 1.538em;" data-mce-mark="1">\$host</span>
-   <span style="line-height: 1.538em;"
    data-mce-mark="1">\$username</span>
-   <span style="line-height: 1.538em;"
    data-mce-mark="1">\$password</span>

The code below requires that you supply a valid SMTP hostname along with
user credentials for authenticating against. If using a third party mail
service, you will need to replace mail.emailsrvr.com with the
appropriate SMTP server hostname relative to the service you are
employing. The code also allows for the attachment of files from your
Cloud Sites filesystem to the message, as long as a valid MIME type
definition is supplied.

``` {#pre-0}
setTXTBody($text);
 // define body for HTML capable recipients
 $mime->setHTMLBody($html);

 // specify a file to attach below, relative to the script's location
 // if not using an attachment, comment these lines out
 // set appropriate MIME type for attachment you are using below, if applicable
 // for reference see http://svn.apache.org/repos/asf/httpd/httpd/trunk/docs/conf/mime.types

 $file = "attachment.jpg";
 $mimetype = "image/jpeg";
 $mime->addAttachment($file, $mimetype);

 // specify the SMTP server credentials to be used for delivery
 // if using a third party mail service, be sure to use their hostname
 $host = "mail.emailsrvr.com";
 $username = "webmaster@example.com";
 $password = "yourPassword";

 $headers = array ('From' => $from,
  'To' => $to,
  'Subject' => $subject);
 $smtp = Mail::factory('smtp',
  array ('host' => $host,
    'auth' => true,
    'username' => $username,
    'password' => $password));


 $body = $mime->get();
 $headers = $mime->headers($headers);

 $mail = $smtp->send($to, $headers, $body);

 if (PEAR::isError($mail)) {
  echo("" . $mail->getMessage() . "");
} else {
  echo("Message successfully sent!");
}
?>
```

**Note**<span
style="color: #333333; font-family: arial; font-size: 13.333333969116211px; line-height: 18.19444465637207px;">: </span>[Mail.php](http://pear.php.net/package/Mail "http://pear.php.net/package/Mail")<span
style="color: #333333; font-family: arial; font-size: 13.333333969116211px; line-height: 18.19444465637207px;"> and
[Mail/mime.php](http://pear.php.net/package/Mail_Mime/)
are </span>[PEAR](http://pear.php.net/ "http://pear.php.net/")<span
style="color: #333333; font-family: arial; font-size: 13.333333969116211px; line-height: 18.19444465637207px;"> modules
and are installed on the server. They are included in the
default </span>[include\_path](http://www.php.net/manual/en/ini.core.php "http://www.php.net/manual/en/ini.core.php#ini.include-path")<span
style="color: #333333; font-family: arial; font-size: 13.333333969116211px; line-height: 18.19444465637207px;"> for
PHP,
so </span>[requiring](http://php.net/manual/en/function.require.php "http://php.net/manual/en/function.require.php")<span
style="color: #333333; font-family: arial; font-size: 13.333333969116211px; line-height: 18.19444465637207px;"> it
here will work by default without any additional effort on your
part.</span>

**<span
style="color: #333333; font-family: arial; font-size: 13.333333969116211px; line-height: 18.19444465637207px;">See
Also</span>**

-   [<span style="color: #333333; font-family: arial;"><span
    style="line-height: 18.1875px;">How do I test PHP SMTP
    functionality?</span></span>](/how-to/test-php-smtp-functionality)


