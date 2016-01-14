---
node_id: 1499
title: Set Up SPF and DKIM Records
type: article
created_date: '2012-07-24 00:17:26'
created_by: RackKCAdmin
last_modified_date: '2016-01-11 20:5102'
last_modified_by: rose.contreras
product: Rackspace Email
body_format: tinymce
---

DomainKey Identified Mail (DKIM) and Sender Policy Framework (SPF) are
two different methods that can protect you from email spamming,
spoofing, and phishing attempts. The SPF model lets you specify which
email servers are legitimate servers for your domain. The DKIM model
lets you attach a DomainKey signature to your outgoing mail. The
receiving server then verifies the validity of the key and either
accepts or rejects the mail. SPF and DKIM are frequently used in
combination since they attack email problems from two different angles.

For instructions on how to create DNS TXT Records for DKIM and SPF, see
the following articles:

[Creating a DKIM TXT
Record](http://www.rackspace.com/knowledge_center/node/2407 "Creating a DKIM TXT Record")

[Creating a SPF TXT
Record](http://www.rackspace.com/knowledge_center/node/2408 "Creating a SPF TXT Record")

