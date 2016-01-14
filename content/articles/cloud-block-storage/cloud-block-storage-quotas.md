---
node_id: 3902
title: Cloud Block Storage Quotas
type: article
created_date: '2014-02-12 21:14:18'
created_by: rose.contreras
last_modified_date: '2014-10-16 17:3434'
last_modified_by: kyle.laffoon
product: Cloud Block Storage
body_format: tinymce
---

undefined&ldquo;<Customer Number>",
            "snapshots": -1,
            "volumes": 50
        }
    }

For Cinder client users, the request looks like the following example:

    MFTUG6DH2G->$ cinder quota-show <Customer Number>
    +-----------+-------+
    |  Property | Value |
    +-----------+-------+
    | gigabytes | 10240 |
    | snapshots |   -1  |
    |  volumes  |   50  |
    +-----------+-------+

 

