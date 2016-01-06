---
node_id: 4859
title: RackConnect Global user workflow
permalink: article/rackconnect-global-user-workflow
type: article
created_date: '2015-10-16 17:35:08'
created_by: sameer.satyam
last_modified_date: '2015-10-22 13:0845'
last_modified_by: Nate.Archer
products: RackConnect
body_format: tinymce
---

### RackConnect Global

RackConnect Global provides highly available, secure, private network
connectivity between Rackspace and your off-premises data centers or
your infrastructure at other cloud hosting providers, such as Microsoft
Azure. It allows you to share application workloads and data across
environments.  Please see
[http://www.rackspace.com/cloud/hybrid/rackconnect/global](http://www.rackspace.com/cloud/hybrid/rackconnect/global) for
more details on the product.

This document shows the steps needed to establish a RackConnect Global
virtual circuit with Rackspace.

### Establishing a RackConnect Global (RCG) dedicated connection {#magicdomid4}

Only use this procedure if you are colocated in the same facility as
Rackspace. 

**NOTE:** If you are part of the Equinix Cloud exchange or a Microsoft
Azure customer and need to establish a RackConnect Global
connection with Rackspace, please see below.

1.  You can order RackConnect Global service using the dedicated
    connection method via our sales account team or appropriate
    Rackspace representative.\
      
2.  You are repsonsible for the physical cross-connection to Rackspace's
    RCG Edge devices. Rackspace generates and provides a Letter of
    Authority (LOA) which identifies the physical port and cage location
    for the RackConnect Global edge device.  \
      
3.  Customer submits the LOA and orders the cross connect via the
    colocation provider's portal. Currently, the only supported
    colocation provider is Equinix.\
      
4.  The colocation provider makes the physical connection between
    customer and RackConnect Global edge device(s).\
      
5.  Rackspace configures the RackConnect Global edge device(s)  while
    customer configures their side to establish the Virtual Connection.
    The virtual circuit is established.\
      

### Establishing a RackConnect Global connection via Equinix Cloud Exchange

Use this procedure if you are an Equinix Cloud Exchange customer. 

**NOTE:****If you need to connect your on-premise infrastructure to
Rackspace via a dedicated connection or a Microsoft Azure customer
needing to establish RackConnect Global connectivity with Rackspace,
please see the section above/below 

1.  You can order RackConnect Global (RCG) service using a cloud
    exchange connection method via your sales account team or
    appropriate Rackspace representative.\
      
2.  Rackspace generates a Service Key and provides it to the customer.
    The service key will be used when requesting a new VC. \
      
3.  Customer orders a VC via the Equinix Cloud Exchange portal and
    initiates the virtual circuit using the service key.\
      
4.  Rackspace completes the RackConnect Global Edge configuration.\
      
5.  Rackspace accepts the virtual circuit request from the customer
    within the Cloud Exchange. \
      

### Establishing a RackConnect Global connection if you use Microsoft Azure (via Microsoft ExpressRoute) {#magicdomid46}

This procedure applies if you are Microsoft Azure customer requiring a
private connection to your infrastructure at Rackspace.

**NOTE:** If you need to connect your on-premise infrastructure to
Rackspace via a dedicated connection or if you need to establish
RackConnect Global connectivity with Rackspace via Equinix Cloud
Exchange, please see the relevant sections above

1.  You can order RackConnect Global service to connect to Microsoft
    Azure via your sales account team or appropriate Rackspace
    representative. If you are a fanatical Azure customer please contact
    your appropriate Rackspace support representative.\
      
2.  Customer configures Azure's dedicated virtual circuit and and
    provides the Azure Service Key to Rackspace for provisioning the
    Virtual Connection. \
      
3.  Rackspace orders a VC on behalf of the customer via the Equinix
    Cloud Exchange portal and initiates the virtual circuit provisioning
    using the service key.\
      
4.  Customer completes the configuration on the cloud to establish the
    VC and BGP connection.\
      
5.  Rackspace completes the configuration on the RCG Edges and backbone
    devices to establish the VC connection.

 

 

