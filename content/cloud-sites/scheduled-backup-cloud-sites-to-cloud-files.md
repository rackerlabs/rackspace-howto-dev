---
node_id: 3624
title: Scheduled Backup -- Cloud Sites to Cloud Files
type: article
created_date: '2013-07-22'
created_by: Jereme Hancock
last_modified_date: '2016-01-11'
last_modified_by: Margaret Eker
product: Cloud Sites
product_url: cloud-sites
---

**Note:** This article is written for our [Cloud Sites Cloud Control
Panel](https://manage.rackspacecloud.com). You can access this interface
from the [Cloud Control Panel](https://mycloud.rackspace.com) by
clicking your username in the upper-right of the control panel and
selecting "Cloud Sites Control Panel".*

This article provides a simple installer for setting up scheduled
backups via a cron task. The installer will setup all the necessary
files for backing up your site files and database. It will also setup
the Cloud Files API for moving your backups to your Cloud Files storage.

If you want a web-based tool to manage manual and scheduled backups
instead, the [Zipit
tool](/how-to/zipit-backup-utility-for-cloud-sites-linux) can
offer that additional functionality.

**Limitations:**

-   Cloud Sites has a 15 minute limit on anything run via cron task. If
    your site backup takes longer than the 15 minute limit your backups
    will not complete or may result in partial backups.
-   Backups are limited to a total of 4gb.
-   For Linux sites only.

**Installation/Setup:**

-   Download [this
    file](https://raw.github.com/jeremehancock/cron-backup-script-setup/master/cron-backup-setup.php) and
    save it to your local machine as "cron-backup-setup.php" without
    the quotes.
-   Upload the cron-backup-setup.php file to the content folder of the
    site you want to backup.
-   Open your web browser and navigate to
    http://*yourdomain.com*/cron-backup-setup.php to access
    the installer.

**Note:** Replace "*<span>http://</span>*yourdomain.com" with your actual
domain name.

-   Enter your database credentials. (Leave this section blank if your
    site does not have a database)

**Note:** Be sure to use the hostname and not the IP address for your
database.*

-   Enter your Cloud Files username and API Key.

[Click here for instructions on generating Cloud Files API
Key](/how-to/view-and-reset-your-api-key)

<span>For more information regarding Cloud Files pricing visit:</span>

<http://www.rackspace.com/cloud/files/pricing/>

-   Click "Install"

Here is a screenshot of the Cron Backup Setup interface:

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/cron-backup-setup.png" width="419" height="755" />

Once the installation is complete you will see one new directory that
contains the Cloud Files API files and two files used to backup your
site. These files will be found in the "root" of your site (ie.
www.yoursite.com directory). Below is a list of the additions to your
site.

1.  cron-backup-api (directory containing API files)
2.  cron-backup.php (main backup file)
3.  cron-backup-config.php (configuration file)

Now that you have the backup script and all necessary files installed
you can setup your cron job to backup your site.

For more information on setting up a cron task in Cloud Sites, see the
article [*How do I schedule a cron job for Cloud
Site*s?](/how-to/how-do-i-schedule-a-cron-job-for-cloud-sites)

Here are the basics of what you will use for the cron task:

-   Command Language: php
-   Command to Run: cron-backup.php (You do not need to include any
    path information. Simply put cron-backup.php in this field)

*Note: It is highly recommended that you choose the option to send the
results via email. This will help ensure that you are aware if your
backups fail for any reason.*

Here is a screenshot of the the cron setup in the Cloud Control Panel:

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/cron-setup.png" width="624" height="598" />

That's it! You should now have scheduled backups setup for your Cloud
Site. Your backups can be found within your Cloud Files section of the
*[Cloud Control Panel](https://mycloud.rackspace.com).*

The container for the backups will be named with the following syntax:

**domain.com-cron-backups**

The backups will be named with the following syntax:

**domain.com-backup-DATE.zip** where DATE is the date that the backup
was taken

*By installing this backup script you agree that this feature is an
Unsupported Service (as defined herein) and you also agree to the terms
of the GPL License! See: [GPL
v3](http://www.gnu.org/licenses/gpl-3.0.en.html)*

If you use the tool described in this article, you agree that the tool
is an &ldquo;Unsupported Service&rdquo;. Rackspace makes no representation or
warranty whatsoever regarding any Unsupported Service, and you agree
that Rackspace will not be liable to you for any loss or damage arising
from the provision of the Unsupported Service.  The Service Level
Guaranties will not apply to the Unsupported Service, or any other
aspect of your services that are adversely affected by the Unsupported
Service.  You acknowledge that Unsupported Services may not interoperate
with Rackspace&rsquo;s other services or other third party services you use.



