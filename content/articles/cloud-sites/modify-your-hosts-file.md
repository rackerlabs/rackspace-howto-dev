---
node_id: 629
title: Modify your hosts file
type: article
created_date: '2011-03-16 21:57:40'
created_by: RackKCAdmin
last_modified_date: '2015-09-18 21:0739'
last_modified_by: kyle.laffoon
products: Cloud Sites
body_format: tinymce
---

undefined&ndash; local host). Add your new mappings after the default mappings.
5.  Save the hosts file by pressing **Control+x** and answering **y**.
6.  Make your changes take effect by flushing the DNS cache with the
    following command:

        dscacheutil -flushcache

    The new mappings should now take effect.



