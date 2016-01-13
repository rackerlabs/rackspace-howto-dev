---
node_id: 3486
title: Using dig to query nameservers
type: article
created_date: '2013-05-28 16:55:15'
created_by: jered.heeschen
last_modified_date: '2013-06-18 13:1025'
last_modified_by: kyle.laffoon
products: Cloud Servers
body_format: tinymce
---

undefined&mdash; catch up on the change over
a week or so.

Some advanced techniques can be employed to reduce propagation delay but
they are beyond the scope of this article.

#### Which DNS server is responding to my queries?

We can see which DNS server is resolving the client's requests by
issuing the "dig" command with no arguments. The client's default DNS
server is listed on the "SERVER" line close to the end of the output.

    dig

    ; <<>> DiG 9.5.1-P2 <<>>
    ;; global options:  printcmd
    ;; Got answer:
    ;; ->>HEADER<

#### Summary

In this article we discussed how to check the authoritative nameservers
for a domain. We've also seen how we can verify record propagation by
querying external DNS servers.

In the final[placeholder for link to new article address] article in
this series we will take a closer look at the results when we omit the
+short option (like we did in that last example), and answer some common
questions about using dig.

