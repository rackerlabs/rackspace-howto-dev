---
node_id: 266
title: Backing up your files with rsync
type: article
created_date: '2011-03-16 21:57:40'
created_by: RackKCAdmin
last_modified_date: '2015-12-29 17:3946'
last_modified_by: Nate.Archer
products: Cloud Servers
body_format: tinymce
---

undefined(a) is archive mode which basically keep the permission settings for
the files. (v) is verbose mode. You can leave it out or increase it by
appending two v's (-vv). (l) preserves any links you may have created.

--delete: deletes files from the destination folder that are no longer
required (i.e. they have been deleted from the folder being backed up).

--stats: Adds a little more output regarding the file transfer status.

--progress: shows the progress of each file transfer. Can be useful to
know if you have large files being backup up.

demo@123.45.67.890:/home/demo: The originating folders to backup.

The syntax here is very important - naturally you need the username and
IP address of the originating server - but note in this example there is
no trailing slash (/).

If you leave the trailing slash off, the named folder and contents will
be downloaded. So in this case I would have a folder called 'demo' in my
backup directory.

If I added the trailing slash (demo@123.45.67.890:/home/demo/) then I
would have the contents of demo in my backup. So I may have folders
called 'public\_html' or 'configs' or 'bin' and so on.

/backup/: Identifies the folder on the backup server to place the files.

Output
------

So from the command above, my storage server would start to output
something like this:

     
    receiving file list ...
    31345 files to consider
    ./
    tuning-primer.sh
           42596 100%  533.30kB/s    0:00:00 (xfer#2, to-check=31331/31345)
    bin/
    bin/Backup
             618 100%    7.74kB/s    0:00:00 (xfer#3, to-check=31310/31345)
    bin/Search
             455 100%    5.70kB/s    0:00:00 (xfer#4, to-check=31309/31345)
    configs/
    configs/php.ini
             114 100%    1.43kB/s    0:00:00 (xfer#5, to-check=31307/31345)
    public_html/
    ...
    ...

As you can see, it receives a list of files (31,345 of them) and, for
the first run, downloads them all.

Running rsync again will only download files that have changed so,
depending on how busy your home directory is, a much smaller download
will be conducted.

Summary
-------

This was a quick introduction to rsync. The command shown is a simple
but effective and secure means of creating an incremental backup of your
files.

