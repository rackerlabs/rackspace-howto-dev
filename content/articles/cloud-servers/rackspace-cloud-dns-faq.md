---
node_id: 1239
title: Rackspace Cloud DNS - FAQ
type: article
created_date: '2011-10-25 16:30:48'
created_by: RackKCAdmin
last_modified_date: '2016-01-11 22:1210'
last_modified_by: rose.contreras
products: Cloud Servers
body_format: tinymce
---

undefined&rsquo;s for domains and records?

When a domain and/or record is created, and no TTL (Time To Live) is
specified, a default value of 3600 seconds is used. When the domain
and/or record TTL is supplied by the user via a create or update
operation, the specified TTL values must be 300 seconds or more.

#### How long does it take for DNS changes to be propagated globally?

Typical DNS propagation to Rackspace nameservers (globally) may take up
to one minute. This refers to the amount of time it takes after a change
(add/delete/update) is made to a customer's records via API, DNS
Manager, MyRackspace Customer Portal, Cloud Control, etc. before the
change is live on our nameservers. Large amount of changes made
simultaneously may take 2-3 minutes.

If a new domain is added or an existing domain is deleted, this may take
up to a few minutes to propagate to our Rackspace nameservers.

When changing nameservers for a domain, complete propagation will take
about 2 days for most domains. This is enforced by the registries.

#### Are there API rate limits?

All accounts, by default, have a preconfigured set of thresholds (or
limits) to manage capacity and prevent abuse of the system. The system
recognizes two kinds of limits: rate limits and absolute limits. Rate
limits are thresholds that are reset after a certain amount of time
passes. Absolute limits are fixed. See the [developers
guide](http://docs.rackspace.com/) for more information on rate limits.

#### How many Cloud DNS domains and records can I have?

By default, Cloud DNS users may have up to 500 domains (including
sub-domains) and 500 records per domain per Cloud account. When a user
submits a request to create new domains, records, and/or sub-domains,
the system will only accept the request if the total number of existing
plus requested domains, sub-domains and/or records is within the account
limits. If the total exceeds the account limit, the entire request will
be rejected and a '413 Request Entity Too Large' message will be
returned. See the [Cloud DNS Developer's
Guide](http://docs.rackspace.com/cdns/api/v1.0/cdns-devguide/content/overview.html)
for more information on absolute limits.

#### How can I create a Cloud DNS ticket?

You may submit Cloud DNS requests using the standard Support
ticket interface in the Control Panel.

