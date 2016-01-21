---
node_id: 4859
title: RackConnect Global user workflow
type: article
created_date: '2015-10-16'
created_by: Sameer Satyam
last_modified_date: '2015-10-22'
last_modified_by: Nate Archer
product: RackConnect
product_url: rackconnect
---

### RackConnect Global

<span
class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">RackConnect
Global provides highly available, secure, private network connectivity
between Rackspace and your off-premises data centers or your
infrastructure at other cloud hosting providers, such as Microsoft
Azure. It allows you to share application workloads and data across
environments.  Please see
</span><http://www.rackspace.com/cloud/hybrid/rackconnect/global><span
class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo"> for more
details on the product.</span>

<span class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">This
document shows the steps needed to establish a RackConnect Global
virtual circuit with Rackspace.</span>

<div>

### <span class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">Establishing a RackConnect Global </span><span class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">(RCG) </span><span class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">dedicated connection</span>

<span class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">Only use
this procedure if you are colocated in the sam</span><span
class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">e</span><span
class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z"> facility as
Rackspace. </span>

</div>

<span
class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z i">**NOTE:** If
you are part of the Equinix Cloud exchange or a Microsoft Azure customer
and need to establish a RackConnect Global connection with Rackspace,
please see below.</span>

1.  <span class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">You
    can order R</span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">ackConnect
    Globa</span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">l
    </span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">service
    </span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">using the
    dedicated connection method</span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z"> via
    </span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">our</span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z"> sales
    account team or </span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">appropriate
    Rackspace representative.</span>

2.  <span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo"><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">You are
    repsonsible for the physical cross-connection to Rackspace's RCG
    Edge devices. Rackspace </span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">generates
    and provides </span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">a Letter of
    Authority (</span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">LOA</span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">) which
    identifies the physical port and cage location for the RackConnect
    Global edge device.  </span></span>

3.  <span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo"><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z"><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">Customer
    submits </span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">the
    </span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">LOA and
    order</span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">s</span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo"> the
    cross connect </span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">via the
    colocation provider's portal</span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">.
    C</span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">urrently</span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">,
    the</span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z"> only
    supported colocation </span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">provider
    </span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">is
    </span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">Equini</span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">x.</span></span></span>

4.  <span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo"><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z"><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z"><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">The
    colocation provider makes the physical connection between customer
    and R</span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">ackConnect
    Global edge </span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">device</span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">(s).</span></span></span></span>

5.  <span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo"><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z"><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z"><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z"><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">R</span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">ackspace
    </span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">configures
    </span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">the
    R</span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">ackConnect
    Global</span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">
    </span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">edge
    device(s)  </span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">while
    </span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">customer
    configures their side to establish </span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">the
    Virtual Connection. </span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">The
    virtual circuit is establishe</span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">d.</span></span></span></span></span>


### <span class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">Establishing a RackConnect Global connection via Equinix Cloud Exchange</span>

<span class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">Use
this procedure if you are an Equinix Cloud </span><span
class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">E</span><span
class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">xchange
</span><span
class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">customer</span><span
class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">. </span>

<span
class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z i">**NOTE:** **
If you need to connect your on-premise infrastructure to Rackspace via a
dedicated connection or a</span><span
class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z i"> Microsoft
Azure customer needing to establish RackConnect Global connectivity with
Rackspace, please see the section above/below </span>

1.  <div id="magicdomid33">

    </div>

    <span class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">You
    can order RackConnect Global (RCG) </span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">service
    </span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">using
    </span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">a cloud
    exchange connection </span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">method
    via your sales account team or appropriate
    Rackspace representative.</span>

2.  <span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo"><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">R</span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">ackspace
    </span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">generates
    a </span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">S</span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">ervice
    </span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">K</span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">ey and
    provides </span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">it
    </span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">to
    the customer.</span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z"> The service
    key will be used when requesting a new VC. </span></span>

3.  <span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo"><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z"><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">C</span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">ustomer
    orders a VC via the Equinix Cloud Exchange portal and initiates the
    virtual circuit using the service key.</span></span></span>

4.  <span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo"><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z"><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo"><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">R</span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">ackspace
    </span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">completes
    the </span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">R</span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">ack</span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">C</span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">onnect
    </span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">G</span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">lobal</span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z"> Edge
    </span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">configuration</span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">.</span></span></span></span>
    <span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo"><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z"><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo"><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z"> </span></span></span></span>
5.  <span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo"><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z"><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo"><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z"><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">R</span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">ackspace
    </span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">accepts
    the virtual circuit </span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">request from
    the customer within the Cloud
    Exchange. </span></span></span></span></span>


### <span class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">Establishing a RackConnect Global connection</span><span class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z"> </span><span class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">if you use Microsoft Azure (via Microsoft ExpressRoute)</span>

<span class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">This
procedure applies if you are Microsoft Azure customer requiring a
private connection to your infrastructure at Rackspace.</span>

<span
class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z i">**NOTE:** If
you need to connect your on-premise infrastructure to Rackspace via a
dedicated connection or if</span><span
class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z i"> you need to
establish RackConnect Global connectivity with Rackspace via Equinix
Cloud Exchange, please see the relevant sections above</span>

1.  <div id="magicdomid56">

    </div>

    <span class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">You
    can order RackConnect Global service to connect to Microsoft Azure
    via your sales account team or appropriate Rackspace representative.
    If you are a fanatical Azure customer please contact your
    appropriate Rackspace support representative.</span>

2.  <span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo"><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">Customer
    </span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">configures
    Azure's dedicated virtual circuit and </span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">and
    provides </span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">the Azure
    Service Key </span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">to
    R</span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">ackspace</span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo"> for
    provisioning the V</span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">irtual
    Connection. </span></span>

3.  <span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo"><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z"><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">Rackspace
    orders a VC</span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z"> on behalf
    of the customer</span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo"> via the
    Equinix Cloud Exchange portal and initiates the virtual circuit
    </span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">provisioning
    </span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">using the
    service key.</span></span></span>

4.  <span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo"><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z"><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo"><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">Customer
    completes the configuration on the cloud to establish the VC and
    BGP connection.</span></span></span></span>

5.  <span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo"><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z"><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo"><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo"><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">Rackspace
    completes the configuration on the </span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">RCG Edges
    </span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">and
    backbone devices to establish the </span><span
    class="author-a-6z68z17wrz74zz86zz122zvz69zunz87zuz72z">VC
    </span><span
    class="author-a-z85zz86zz86zgz85zfz81zfz86z418z74ziz122zo">connection.</span></span></span></span></span>

<div id="magicdomid66">



</div>

<div id="magicdomid67">



</div>

