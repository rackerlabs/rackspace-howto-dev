---
node_id: 3714
title: 'Best Practices for Backing Up Your Data: Cloud Block Storage versus Cloud Backup'
type: article
created_date: '2013-10-01 19:24:05'
created_by: kyle.laffoon
last_modified_date: '2014-10-30 20:3902'
last_modified_by: jered.heeschen
products: Cloud Backup
body_format: tinymce
---

undefined&rdquo; of the previous backup, which enables faster backup and
restore operations and reduces the storage amount required. If ever
needed, you can revert your data to an earlier date's backup.\
 \
 The Cloud Backup Agent can complete the backup automatically following
a schedule that you identify, so that you can avoid waiting for the
process to complete. Manual backup is also available on Cloud Backup.

**Encryption**

With Cloud Backup, enterprise-grade encryption (Advanced Encryption
Standard, 256-bit key) is available. When encryption is enabled, your
data will be encrypted with a passphrase that only you know. After you
create your AES-256 encryption key, your data is encrypted before it
leaves the server and remains safely encrypted while stored.

**Note**: After AES-encryption is set, it cannot be removed from your
files.

**Limitations**

To use Cloud Backup, you must set up the Cloud Backup Agent. Backups
cannot occur until you have set up the agent and identified what files
to back up and when to back them up. A small amount of space on your
server is required for the Cloud Backup Agent. All backups performed
with Cloud Backup are placed in Cloud Files, so there are no cost
control options with different storage types.

**Getting Started with Cloud Backup**

See [Getting Started with Cloud
Backup](http://www.rackspace.com/knowledge_center/getting-started/cloud-backup)
to get started with Cloud Backup.

