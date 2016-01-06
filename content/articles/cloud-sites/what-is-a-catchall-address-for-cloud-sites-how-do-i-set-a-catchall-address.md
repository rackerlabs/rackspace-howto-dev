---
node_id: 717
title: What is a catchall address for Cloud Sites? How do I set a catchall address?
permalink: article/what-is-a-catchall-address-for-cloud-sites-how-do-i-set-a-catchall-address
type: article
created_date: '2011-03-16 21:57:40'
created_by: RackKCAdmin
last_modified_date: '2015-06-30 16:4750'
last_modified_by: kelly.holcomb
products: Cloud Sites
body_format: tinymce
---

##### NOTE: *This documentation refers to a feature that is no longer available for Cloud Sites.  This article is here for the purpose of legacy support only.* {.p1}

 

A catchall address is a designated mailbox where any email sent to a
non-existent email address will be delivered. To better help explain
catchalls, review the example below:

You have the following mailboxes setup on your account:

-   john@yourdomain.com
-   bill@yourdomain.com
-   catchall@yourdomain.com (**Which is set as the catch-all**)

Now in this example, any email sent to john@yourdomain.com would be
delivered to that corresponding mailbox.

The same would hold true for any email sent to bill@yourdomain.com.
However, what would happen if an email was sent to
"frank@yourdomain.com"?

Because the mailbox frank@yourdomain.com has not been setup in the
system, normally the email would be rejected with a "user unknown"
message and would be returned to the sender. However, if you have a
catchall setup, like in the example above, the email would be delivered
to the catch-all mailbox. This would hold true for email sent to any
other addresses which have not been setup as mailboxes on the system.

To set up a catchall email account for a particular domain:

1.  Log in to your [control
    panel.](https://manage.rackspacecloud.com "https://manage.rackspacecloud.com")
2.  Select the "**Hosting**" link in the left navigation bar. Then
    select "**Cloud Sites**"
3.  Select the domain for which you wish to add a catch-all account from
    the "Websites" list.
4.  Click the "**Email Accounts**" tab in the bar at the top of the
    page.
5.  Add the email account that you want to use for the catch-all (i.e.
    catchall@yourdomain.com).
6.  Under "**Mail Preferences**" at the bottom of the page, select "Send
    them to this account (catchall)" and select the account you want to
    use from the pull-down menu.


