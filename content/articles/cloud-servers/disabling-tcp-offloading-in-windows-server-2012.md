---
node_id: 3855
title: Disabling TCP Offloading in Windows Server 2012
type: article
created_date: '2014-01-16 14:43:38'
created_by: kyle.laffoon
last_modified_date: '2014-07-18 19:5224'
last_modified_by: kyle.laffoon
product: Cloud Servers
body_format: tinymce
---

TCP offload engine is a function used in network interface cards (NIC)
to offload processing of the entire TCP/IP stack to the network
controller. By moving some or all of the processing to dedicated
hardware, a TCP offload engine frees the system's main CPU for other
tasks. However, TCP offloading has been known to cause some issues, and
disabling it can help avoid these issues.

**NOTE:** We recommend **keeping TCP offloading enabled **in any source
images that you use to build new servers, and then disabling TCP
offloading in the source image after the new server is built. If TCP
offloading is disabled on an image, a server build from that image might
fail. We are working on a solution for this issue. However, as this is a
multiple vendor issue the resolution will depend on the vendors'
cooperative efforts.

### Disable TCP Offloading

1.  In the Windows server, open the Control Panel and select **Network
    Settings **\> **Change Adapter Settings**.

    ![](/knowledge_center/sites/default/files/field/image/TCPOffloading8.png)

2.  Right-click on each of the adapters (**private **and **public**),
    select **Configure **from the **Networking **menu, and then click
    the **Advanced **tab. The TCP offload settings are listed for the
    Citrix adapter.

    ![](/knowledge_center/sites/default/files/field/image/TCPOffloading9.png)

3.  Disable each of the following TCP offload options, and then click
    **OK**:
    -   IPv4 Checksum Offload
    -   Large Receive Offload
    -   Large Send Offload
    -   TCP Checksum Offload



