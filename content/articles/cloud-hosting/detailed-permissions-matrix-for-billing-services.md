---
node_id: 3693
title: Detailed Permissions Matrix for Billing Services
type: article
created_date: '2013-09-19 16:51:13'
created_by: renee.rendon
last_modified_date: '2016-01-05 17:0722'
last_modified_by: Mike Asthalter
product: Cloud Hosting
body_format: tinymce
---

The following permissions matrix displays specific capabilities for the
roles in Billing and Payment Services. 

### **[Related Knowledge Center Articles](http://www.rackspace.com/knowledge_center/article/billing-services-overview)**

### **As of April 8, 2014**

CAPABILITY

ROLE

DESCRIPTION

 

Observer

Admin

 

### BILLING SERVICES

List Account Balance

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

Returns the balance for the current account. 

List Billing Summary 

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

Returns the billing summary for the current account. 

List Account Currency 

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png) 

Returns the currency for the current account.

List Account Billing Cycle 

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png) 

Returns the billing cycle for the current account.

List Current Invoice 

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

Returns the invoice for the current account. Returns response in PDF
format.

List Invoice by ID 

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

 

Returns a specific invoice. Returns response in PDF format.  

List Invoice Payments

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

Returns a list of payments related to an invoice. 

List Account Payment by ID

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

Lists a specific payment. 

List Payment Invoices

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

Returns a list of invoices related to a payment. 

List Refund by ID

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

Lists a specific refund

List Account VAT

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

Returns the Value Added Tax (VAT) code for the current account.

List Billing Periods

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

Returns a list of billing periods. 

List Estimated Charges

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png) 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png) 

Returns list of summarized estimated charge for a specific billing
period.

List Subscriptions

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png) 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png) 

Returns a list of Subscriptions for the account.

List Contract Entity

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png) 

Retrieves a Rackspace Contract Entity for a billing account.  

Create Payment

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png) 

Submits a payment for the balance owed by an account.

Update Account VAT

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png) 

Updates the Value Added Tax (VAT) code for the account. 

Create Account VAT

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png) 

Creates a Value Added Tax (VAT) code for the current account.

Delete Account VAT

 

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png) 

Deletes the Value Added Tax (VAT) code for a current account. 

### PAYMENT SERVICES

Get Payment Method

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

Returns the payment method for the current account.

Get Payment Methods

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

Returns a list of payment methods for the current account. 

Get Default Payment Method

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png) 

Returns the default payment method for the current account. 

Create Payment Method

 

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

Creates a payment method for the current account. 

Set Default Payment Method

 

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

Sets the default payment method for the current account. 

Delete Default Payment Method

 

 

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

Deletes the default payment method for the current account.  

Get Supported Methods

 ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

![](/knowledge_center/sites/default/files/field/image/green%20checkmark_5.png)

Lists the supported method of payments. 

**Note:** RBAC is enabled for Billing Services Level (BSL) and Payment
Services Level only through the Cloud Control Panel. API access for BSL
and PSL is not provided at this time.

[\< Permission Matrices for RBAC](http://www.rackspace.com/knowledge_center/article/permissions-matrix-for-role-based-access-control-rbac)
------------------------------------------------------------------------------------------------------------------------------------------

 

