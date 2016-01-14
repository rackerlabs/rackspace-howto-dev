---
node_id: 770
title: Transferring your DNS hosting to Rackspace
type: article
created_date: '2011-11-16 01:09:51'
created_by: Rae D. Cabello
last_modified_date: '2016-01-12 19:3554'
last_modified_by: stephanie.fillmon
product: Cloud Hosting
body_format: tinymce
---

undefined2. Next, you will then need to contact your Domain Registrar and ask
them to change your **Name Servers** and point them to the following: If
you're unsure of who your domain registrar is, you can check your
domain's registration info at the website: who.is

  ---------------- ------------------------
  **Primary**:     DNS1.NAME-SERVICES.COM
  **Secondary**:   DNS2.NAME-SERVICES.COM
  **Secondary**:   DNS3.NAME-SERVICES.COM
  **Secondary**:   DNS4.NAME-SERVICES.COM
  **Secondary**:   DNS5.NAME-SERVICES.COM
  ---------------- ------------------------

*Note:* *DNS changes can take up to 48 hours to resolve. We recommend
that you make this switch during non-business hours or when email
activity is light. No email will be lost during this transition, but do
not cancel your current DNS hosting service until the transfer is
complete.*

