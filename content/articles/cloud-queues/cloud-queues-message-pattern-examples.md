---
node_id: 4040
title: Cloud Queues message patterns
type: article
created_date: '2014-04-24 20:36:08'
created_by: megan.meza
last_modified_date: '2015-07-16 17:4406'
last_modified_by: stephanie.fillmon
products: Cloud Queues
body_format: tinymce
---

undefined&rdquo;-like script, or a passive server process logging everything as it
comes through.\
 \
 Auditing helps in diagnosing problems or bugs in the message producers.
It can also ensure that messages were processed correctly, for example,
if users were using Cloud Queues as part of a metering solution and they
wanted to audit their records to ensure billable events were all
submitted to the billing system correctly.\
 \
 However, having the ability to delay messages from being claim-able for
a certain period of time is a feature still needed in order to make
auditing work really well. Such a feauture would give the auditor a
chance to list a message before the worker deletes it. Today, workers
can pause a specified number of seconds after claiming a message before
deleting it, but this process will be more graceful after message delays
are implemented.

