---
node_id: 4231
title: Getting Started with the RackConnect v3.0 API
type: article
created_date: '2014-09-10 13:34:52'
created_by: juan.perez
last_modified_date: '2015-09-14 19:0944'
last_modified_by: kelly.holcomb
products: RackConnect
body_format: tinymce
---

undefined&mdash;so you use the *--include* option
with the request. A 204 response code signifies that the public IP
address was successfully removed from the cloud server.

### ****Example 204 response to the remove a public IP address from a cloud server API request

    HTTP/1.1 204 No Content
    Server: Apache-Coyote/1.1
    cache-control: no-cache
    via: 1.1 Repose (Repose/3.0.1)
    expires: -1
    date: Thu, 13 Sep 2014 14:48:58 GMT
    pragma: no-cache

Examples with sample data
-------------------------

The preceding sections explained how to use the RackConnect v3.0 API
to list, add, and remove cloud server public IP addresses. To help
clarify the information that has been covered, this section provides a
final example that uses sample data instead of placeholders in the *list
public IP address* operation.

### ****List public IP address for a cloud server API request with sample data

    curl --include \ 
    --request GET \
    --header "X-Auth-Token: NNNaaNNaNNaaaaNNaNaNNNNaaNaNaaaa" \
    --header "Content-Type: application/json" \
    https://iad.rackconnect.api.rackspacecloud.com/v3/NNNNNNN/public_ips?cloud_server_id=aaaNNNNNa-aaaa-NNNN-aNaN-aNNaaNaNaNaa

### ****Sample data entries for this example are as follows:

-   Authentication Token ID = NNNaaNNaNNaaaaNNaNaNNNNaaNaNaaaa
-   Region = iad
-   Tenant ID = NNNNNNN
-   Cloud Server UUID = aaaNNNNNa-aaaa-NNNN-aNaN-aNNaaNaNaNaa

For information about the many other API calls available with the
RackConnect v3.0 API, visit
[http://docs.rcv3.apiary.io/](http://docs.rcv3.apiary.io/).

If you have any questions, reach out to us. Contact information is
available on the [Contact
Us](http://www.rackspace.com/knowledge_center/support) page.

