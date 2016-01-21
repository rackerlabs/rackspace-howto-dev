---
node_id: 3714
title: 'Best Practices for Backing Up Your Data: Cloud Block Storage versus Cloud Backup'
type: article
created_date: '2013-10-01'
created_by: Kyle Laffoon
last_modified_date: '2014-10-30'
last_modified_by: Jered Heeschen
product: Cloud Backup
product_url: cloud-backup
---

When backing up the data disk or disks on your General Purpose Cloud
Servers you have two convenient choices: Cloud Block Storage or Cloud
Backup. Identifying which one to use depends on what features are most
important to you.

#### Cloud Block Storage for Portability

Cloud Block Storage works much like a portable drive. It can be attached
to one server and later detached and attached to another server. This
makes moving data between servers convenient, as all files and folders
can be moved by detaching the drive from your old server and attaching
it to the new server. Cloud Block Storage offers two drive types: a SATA
option, which helps control costs, and an SSD option for higher
performance. Unlike Cloud Backup, there is no agent to install. You
simply copy your files to the attached volume.

**Limitations**

Cloud Block Storage attaches a traditional data volume to your server,
so there is no built-in mechanism to track or retrieve overwritten data.
If you select the SATA option, you might find that transferring large
files or a large number of files is slower than other file transfer
options. Additionally, the Cloud Block Storage process cannot be
automated. You must copy the data to the volume after configuring it on
your server.

**Getting Started with Cloud Block Storage**

To get started with Cloud Block Storage, see [Create and Attach a Block
Storage
Volume](/how-to/create-and-attach-a-cloud-block-storage-volume).

#### Cloud Backup for Incremental Backups

After the initial setup, including installation of the Cloud Backup
Agent and capture of all the initial files, Cloud Backup uses
deduplicaiton to only capture only data that has actually changed. With
the exception of your first complete backup, every subsequent backup is
just a &ldquo;delta&rdquo; of the previous backup, which enables faster backup and
restore operations and reduces the storage amount required. If ever
needed, you can revert your data to an earlier date's backup.

The Cloud Backup Agent can complete the backup automatically following a
schedule that you identify, so that you can avoid waiting for the
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
Backup](/how-to/cloud-backup)
to get started with Cloud Backup.

