---
node_id: 3904
title: Moving a Software RAID Cloud Block Storage Volume from One Cloud Server to Another
type: article
created_date: '2014-02-14 19:52:54'
created_by: trenton.guthrie
last_modified_date: '2014-10-30 20:2756'
last_modified_by: kyle.laffoon
products: Cloud Block Storage
body_format: tinymce
---

undefined12. Remount the RAID.

        mkdir /newraid
        mount /dev/md0p1 /newraid

