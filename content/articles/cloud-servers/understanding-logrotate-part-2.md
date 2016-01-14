---
node_id: 1261
title: Sample logrotate configuration and troubleshooting
type: article
created_date: '2011-11-23 19:45:35'
created_by: jered.heeschen
last_modified_date: '2015-12-31 17:0617'
last_modified_by: stephanie.fillmon
product: Cloud Servers
body_format: tinymce
---

### Applying knowledge {#applying_knowledge}

In the [previous
article](https://www.rackspace.com/knowledge_center/article/understanding-logrotate-utility "Understanding logrotate - part 1")
we talked about what logrotate does and how you can configure it. In
this article w&rsquo;ll apply this new knowledge to putting together a log
rotation solution for a custom virtual host or two (or three, or four,
etc.). W&rsquo;ll also look at some options for testing and troubleshooting
logrotate.

### Tying it all together: virtual host logs {#tying_it_all_together_virtual_host_logs}

To show how you can use logrotate for your own applications, le&rsquo;s look
at an example that will come in handy for a lot of people: rotating logs
for your custom virtual hosts. W&rsquo;ll use apache for this example, but it
can be tweaked pretty easily for other web servers like nginx or
lighttpd, usually just by changing the postrotate script.

First w&rsquo;ll want to create a file to hold the configuration that will
tell logrotate what to do with the virtual hos&rsquo;s log files. We wo&rsquo;t
edit the main config file or the web serve&rsquo;s config file, since ther&rsquo;s
always a possibility that a future package upgrade might want to
overwrite the config. Instead w&rsquo;ll make our own. Le&rsquo;s call it:

    /etc/logrotate.d/virtualhosts

This example tosses all the virtual hosts into one file, but if you have
one tha&rsquo;s busier than others you may want to create separate config
files to handle the needs of your different domains. W&rsquo;ll also specify
several items that are probably already set in your main config, just so
we cover all the bases.

#### The files {#the_files}

W&rsquo;ll say that we have two virtual domains, domain1.com and domain2.com,
and that the log files for each are in /home/demo/public\_html/(domain
name)/log. The first thing w&rsquo;ll do in our config file is tell logrotate
where to find the log files, then start the config block for them:

    /home/demo/public_html/domain1.com/log/*log /home/demo/public_html/domain2.com/log/*log {

If you have more log directories or files to add, just insert them into
that list.

#### Rotate

Next w&rsquo;ll want to make sure logrotate only keeps as many old logs as we
want:

    rotate 14

W&rsquo;ll use 14 in this example to keep two week&rsquo; worth of logs, but you
can of course adjust that number to something suitable to your
requirements.

#### Interval

Now w&rsquo;ll tell the web server to rotate these logs daily (again, change
it if you prefer a longer interval):

    daily

#### Size (optional) {#size_optional}

The size setting specifies a maximum size for your logs.  When the log
reaches that size a log rotation is triggered.

    size 50M

The size setting is optional here because it actually overrides any
time-based rotation conditions.  You can specify both a time interval
and a max size, but if you do the time interval setting will be ignored.

#### Compression

W&rsquo;ll specify whether or not we want these logs to be compressed when
the&rsquo;re archived. For this example w&rsquo;ll use delaycompress to account
for the graceful restart of apache, which means we also need to turn
compression on:

    compress
    delaycompress

#### Sharedscripts

You might have several virtual hosts, and that would mean several logs
to rotate. To make sure the web server only gets restarted after all the
rotations are done we add:

    sharedscripts

#### Postrotate

W&rsquo;ll specify a postrotate script that will restart the web server:

    postrotate
            /usr/sbin/apachectl graceful > /dev/null
    endscript

And finally, we close the config block with a curly bracket:

    }

#### The whole shebang {#the_whole_shebang}

Once we bring it all together our config file will look like this:

    /home/demo/public_html/domain1.com/log/*log /home/demo/public_html/domain2.com/log/*log {
            rotate 14
            daily
            compress
            delaycompress
            sharedscripts
            postrotate
                    /usr/sbin/apachectl graceful > /dev/null
            endscript
    }

Yo&rsquo;ll want to test that, of course, either by making sure yo&rsquo;re
watching things when the nightly cron jobs are run, or by running
logrotate right now:

    /usr/sbin/logrotate /etc/logrotate.conf

If you do&rsquo;t get any errors back you should be okay. But if you want to
be absolutely certain you can run through some of the tests we would use
when we suspect something is&rsquo;t working right.

### Testing logrotate {#testing_logrotate}

If you suspect logrotate is having some trouble, or you just want to
make sure a new config yo&rsquo;ve put in place will work, there are some
useful flags you can pass to logrotate when you run it from the command
line:

#### Verbose

The verbose flag,&ldquo;-&rdquo;, tells logrotate to say what i&rsquo;s doing while
i&rsquo;s doing it. I&rsquo;s very useful when trying to find out why logrotate
does&rsquo;t rotate a log when you want it to.

#### Debug

The debug flag,&ldquo;-&rdquo;, tells logrotate to go through the motions of
rotating logs but not *actually* rotate them. It can be handy if you
want to test a new config file but do&rsquo;t want any actual log rotation
run when you do (if yo&rsquo;re working on a production server, for example).

The debug flag is good for checking that the config file is formatted
properly and that logrotate can find the log files it would rotate.
However, since it does&rsquo;t actually run the rotations it does&rsquo;t test
some parts of the process like the postrotate scripts.

#### Force

The force flag,&ldquo;-&rdquo;, forces logrotate to rotate all logs when it runs,
whether or not they would normally need to be rotated at that time. If
you want to thoroughly test logrotat&rsquo;s configs this is the flag to use.
Just remember that logrotate will be rotating logs and deleting old ones
according to the configuration yo&rsquo;ve set up, so do&rsquo;t accidentally
rotate out a recent log you needed to keep.

The force flag can be useful if yo&rsquo;re convinced that logrotate should
be rotating a log, but it is&rsquo;t. Forcing the issue will help you tell if
the problem is that logrotate does&rsquo;t think the log needed rotating (if
you run with the force flag and the log is rotated), or if the problem
is that logrotate is&rsquo;t able to affect the log file (if you run it and
nothing happens to the log).

Note that if logrotate is set to add a date to the name of an archived
log, not even using the force flag will get logrotate to make a new
archive in the same day (since the name it would use for the archive is
already taken). In that circumstance you may need to rename the most
recent archive (for each log file in a given config block) before you
can force a log rotation.

#### Combining flags {#combining_flags}

The testing flags can be used together quite effectively. To have
logrotate tell you what it would do if you made it rotate everything,
but not *actually* rotate anything, you can combine all three:

    /usr/sbin/logrotate -vdf /etc/logrotate.conf

Yo&rsquo;ll get treated to a long list of things logrotate would do,
including which log files it would rotate and what it would do during
that process.

If you then want to test all the rotate configs in their entirety&mdash;
including the scripts run after rotations&mdash; you can run logrotate
without the debug flag:

    /usr/sbin/logrotate -vf /etc/logrotate.conf

All the logs will be rotated, and skimming the output should help you
catch any obvious problems. Yo&rsquo;ll also want to make sure that all your
services are still running okay (that there was nothing wrong with the
postrotate scripts), and that all the logs actually did get rotated.

### How logrotate remembers {#how_logrotate_remembers}

If you find that a log is&rsquo;t rotating even though i&rsquo;s old enough that
it should, a simple way to fix the problem is to manually run logrotate
with the&ldquo;-&rdquo; flag. But if yo&rsquo;re the sort who wants to know *why*
somethin&rsquo;s gone wrong, ther&rsquo;s one more file you can check before
forcing a rotation:

    /var/lib/logrotate.status

That file is where logrotate stores information about when it last
rotated each log file. If you look inside yo&rsquo;ll see something like:

    logrotate state -- version 2
    "/var/log/acpid.log" 2010-6-18
    "/var/log/iptables.log" 2010-6-18
    "/var/log/uucp.log" 2010-6-29
    ...

I&rsquo;s a straightforward format - the log file location is on the left,
and the date when it was last rotated is on the right. Sometimes it can
happen that the dates on your server get a little wonky (if you were
tinkering with an NTP service or the like), and the date when a log was
last rotated winds up being a future date. If tha&rsquo;s happened yo&rsquo;ll see
it here.

If you want to check logrotate out with a particular log file but do&rsquo;t
want to force everything to rotate, you can delete the lo&rsquo;s entry from
the logrotate status file. Then when you run logrotate normally it
should create a new entry for the log with toda&rsquo;s date (even though it
may not actually rotate the log - it uses that first run as a baseline
if i&rsquo;s just interval-based).

### Summary

For something that runs quietly in the background and only really
performs one type of task, logrotate does quite a bit. You hopefully
understand logrotate better than you wanted to. At the least you should
be able to set up new logrotate config files for your own purposes,
either creating them from scratch or copying existing configs and
modifying them appropriately. And most importantly, you can keep your
logs from getting out of control.

