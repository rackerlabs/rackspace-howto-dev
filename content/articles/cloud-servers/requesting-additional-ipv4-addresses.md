---
node_id: 1179
title: Requesting additional IPv4 addresses for Cloud Servers
type: article
created_date: '2011-08-08 17:28:23'
created_by: RackKCAdmin
last_modified_date: '2016-01-13 14:1831'
last_modified_by: rose.contreras
products: Cloud Servers
body_format: markdown_w_tinymce
---

Rackspace offers the ability to add IPv4 addresses to cloud servers for a fee. If you want to obtain an additional IPv4 address for your server, you must open a ticket through the Support section of the Cloud Control Panel to get policy information and approval. Before opening a ticket, read this article for necessary information and alternatives.

- [Conditions](#conditions)
- [Pricing](#pricing)  |
- [Information needed for additional IPv4 addresses](#info)
- [Alternatives to obtaining additional IPv4 addresses](#alt)

<a name="conditions"> </a>

## Conditions

Because of the global shortage of IPv4 address space, Rackspace currently offers additional IPv4 addresses only for the following purposes:

- SSL on cloud servers
- NAT (Network Address Translation) on a Brocade Vyatta vRouter

**Note:** No more than four additional IPv4 addresses can be allocated to a single cloud server or Brocade Vyatta vRouter. Thus each cloud server or Brocade Vyatta vRouter has a maximum capacity of five IPv4 addresses, including the originally assigned public IPv4 address.

<a name="pricing"> </a>
## Pricing

The rates for additional IPv4 addresses vary by region. Discuss rates for your region with the Support team during your setup.

<a name="info"> </a>
## Information needed for additional IPv4 addresses

After you are approved for an additional IPv4 address, you will be asked to provide the following information.

### Cloud servers

For an additional IPv4 address on a cloud server, you must provide the following information:

- The name of the server for which you want to add the IP address.
- The SSL certificate. The certificate must have been signed by a valid Certificate Authority; self-signed certificates are not accepted.

### Brocade Vyatta vRouters

For an additional IPv4 address on a Brocade Vyatta vRouter, you must confirm that you intend to use the additional IPv4 address for the purpose of NAT.

<a name="alt"> </a>
## Alternatives to obtaining additional IPv4 addresses

Because there is a finite number of IPv4 addresses, Rackspace limits the number that it distributes. We recommend that you use one of the following options instead of obtaining additional IPv4 addresses:

- Subject Alternate Name (SAN) certificates
- Server Name Indication (SNI) certificates

### SAN certificates

SAN certificates make it possible to protect multiple domain names with one certificate. When you use a SAN certificate for a domain, you can then add more SAN values and have that same certificate protect that single domain.

### SNI certificates

An SNI certificate allows you to have multiple hostnames consolidated onto fewer IP addresses.
However, you should not use an SNI certificate if your website has a high rate of usage by the following applications:

- Internet Explorer 8 and Android 2.3
- Python 2.7.8 and Java 1.6 (and earlier), or any similar client
