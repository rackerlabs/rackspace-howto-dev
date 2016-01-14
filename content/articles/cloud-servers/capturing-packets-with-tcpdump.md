---
node_id: 3434
title: Capturing Packets with Tcpdump
type: article
created_date: '2013-04-25 16:30:27'
created_by: rose.contreras
last_modified_date: '2013-04-25 20:2651'
last_modified_by: jered.heeschen
product: Cloud Servers
body_format: tinymce
---

undefined&rsquo; You
can use logical statements in a tcpdump command. For example, to catch
all the SSH packets going from an SSH server to a client with IP
1.2.3.4:

    sudo  tcpdump "src port 22" and "dst host 1.2.3.4"

Raw packets can be conveniently saved to a file using the '-w' option:

    tcpdump host 1.2.3.4 -w /home/users/demo/demo.dump

Let's read the saved file:

    tcpdump -r /home/users/demo/demo.dump

### Summary

Tcpdump is a powerful packet sniffer and a common tool used by system
administrators to solve network problems and investigate traffic. It can
be used with Boolean expressions to capture only those packets you're
interested.

