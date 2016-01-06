---
node_id: 3902
title: Cloud Block Storage Quotas
permalink: article/cloud-block-storage-quotas
type: article
created_date: '2014-02-12 21:14:18'
created_by: rose.contreras
last_modified_date: '2014-10-16 17:3434'
last_modified_by: kyle.laffoon
products: Cloud Block Storage
body_format: tinymce
---

By default, all new Cloud Block Storage users are assigned a 10 TB / 50
volume quota in each region. This quota is primarily to help with
capacity planning and to prevent system abuse. If your application
requires more storage or volumes than the default quota, simply submit a
support request to ask for an increase. In your request, be sure to
include the storage amount that you need (TBs or volume count), storage
type (SATA or SSD), and region (for example, DFW or LON).

Note: Your Cloud Block Storage quota is independent from any other
account quotas that you might have.

You can use the OpenStack Cinder API to see your current block storage
quota. The following is an example of the cURL request to use:

    curl https://dfw.blockstorage.api.rackspacecloud.com/v1/<Customer Number>/os-quota-sets/<
                -H "X-Auth-Project-Id: <Customer Number>" \
                -H "User-Agent: python-cinderclient" \
                -H "Accept: application/json" \
                -H "X-Auth-Token: <My Auth Token>"

The result of this request follows:

    {
        "quota_set": {
            "gigabytes": 10240,
            "id": &ldquo;<Customer Number>",
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

 

