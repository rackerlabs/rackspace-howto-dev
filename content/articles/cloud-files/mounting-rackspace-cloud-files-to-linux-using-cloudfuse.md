---
node_id: 1121
title: Mounting Rackspace Cloud Files to Linux Using CloudFuse
type: article
created_date: '2011-06-07 23:24:14'
created_by: RackKCAdmin
last_modified_date: '2015-09-01 17:5256'
last_modified_by: catherine.richardson
product: Cloud Files
body_format: tinymce
---

undefined&rsquo;s use CloudFuse to mount our Cloud Files.

You'll have to create a configuration file for CloudFuse in your home
directory and put your Rackspace Cloud Files username and API key in it,
as shown below. (For information on viewing your Rackspace API key, see
[View and reset your API
key](http://www.rackspace.com/knowledge_center/article/view-and-reset-your-api-key).)

    $HOME/.cloudfuse
    username=[username]
    api_key=[api key]
    region=[region-name]

 

### Auth URLs:

Cloud Files account:
[https://auth.api.rackspacecloud.com/v1.0](http://docs.rackspace.com/files/api/v1/cf-devguide/content/ "http://docs.rackspace.com/files/api/v1/cf-devguide/content/")

The following entries are optional. You can define these values in the
**.cloudfuse** file.

    use_snet=[True to use snet for connections]
    cache_timeout=[seconds for directory caching, default 600]

After creating the above configuration file, run the **cloudfuse**
command as follows. The syntax should be as simple as:

     
    cloudfuse [mount point]

So, you should be able to mount Cloud Files like this

    root@ubuntu-test:/# mkdir cloudfiles
    root@ubuntu-test:/# cloudfuse /cloudfiles

If you run the **\# ls -la** command inside the /cloudfiles directory
you should see your Cloud Files containers.

If you are not logged in as the user root on the system, then your
username will need to be part of the *"fuse"* group. This can be
accomplished with the following command:

     
    sudo usermod -a -G fuse [username]

If you are unable to see any containers inside the mountpoint, then one
or more of the above steps didn't work properly. You will need to repeat
the process, and verify that all of the above steps were followed
precisely.

