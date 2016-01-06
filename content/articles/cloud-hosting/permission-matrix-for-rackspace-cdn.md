---
node_id: 4635
title: Permission Matrix for Rackspace CDN
permalink: article/permission-matrix-for-rackspace-cdn
type: article
created_date: '2015-04-07 20:40:34'
created_by: catherine.richardson
last_modified_date: '2015-04-07 20:4119'
last_modified_by: kyle.laffoon
products: Cloud Hosting
body_format: tinymce
---

The following permissions matrix displays specific permissions for the
roles in Rackspace CDN. The matrix displays the method names and the
roles that are supported.

Rackspace CDN RBAC
------------------

  Endpoint                                   RBAC-Creator                                                                     RBAC-Observer                                                                    RBAC-Admin                                                                       RBAC-Operator
  ------------------------------------------ -------------------------------------------------------------------------------- -------------------------------------------------------------------------------- -------------------------------------------------------------------------------- --------------------------------------------------------------------------------
  GET /                                      ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)   ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)   ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)   ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)
  GET /ping                                  ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)   ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)   ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)   ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)
  GET /health                                ![](/knowledge_center/sites/default/files/field/image/red%20X.png)               ![](/knowledge_center/sites/default/files/field/image/red%20X.png)               ![](/knowledge_center/sites/default/files/field/image/red%20X.png)               ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)
  GET /health/{subsystem}                    ![](/knowledge_center/sites/default/files/field/image/red%20X.png)               ![](/knowledge_center/sites/default/files/field/image/red%20X.png)               ![](/knowledge_center/sites/default/files/field/image/red%20X.png)               ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)
  POST /services                             ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)   ![](/knowledge_center/sites/default/files/field/image/red%20X.png)               ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)   ![](/knowledge_center/sites/default/files/field/image/red%20X.png)
  GET /services                              ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)   ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)   ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)   ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)
  GET /services/\\{service\_id\\}            ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)   ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)   ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)   ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)
  PATCH /services/\\{service\_id\\}          ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)   ![](/knowledge_center/sites/default/files/field/image/red%20X.png)               ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)   ![](/knowledge_center/sites/default/files/field/image/red%20X.png)
  DELETE /services/\\{service\_id\\}         ![](/knowledge_center/sites/default/files/field/image/red%20X.png)               ![](/knowledge_center/sites/default/files/field/image/red%20X.png)               ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)   ![](/knowledge_center/sites/default/files/field/image/red%20X.png)
  DELETE /service/\\{service\_id\\}/assets   ![](/knowledge_center/sites/default/files/field/image/red%20X.png)               ![](/knowledge_center/sites/default/files/field/image/red%20X.png)               ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)   ![](/knowledge_center/sites/default/files/field/image/red%20X.png)
  GET /flavors                               ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)   ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)   ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)   ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)
  GET /flavors/\\{flavor\_id\\}              ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)   ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)   ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)   ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)
  POST /flavors                              ![](/knowledge_center/sites/default/files/field/image/red%20X.png)               ![](/knowledge_center/sites/default/files/field/image/red%20X.png)               ![](/knowledge_center/sites/default/files/field/image/red%20X.png)               ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)
  DELETE /flavors/\\{flavor\_id\\}           ![](/knowledge_center/sites/default/files/field/image/red%20X.png)               ![](/knowledge_center/sites/default/files/field/image/red%20X.png)               ![](/knowledge_center/sites/default/files/field/image/red%20X.png)               ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png)

###  

[\< Permission Matrices for RBAC](http://www.rackspace.com/knowledge_center/article/permissions-matrix-for-role-based-access-control-rbac)
------------------------------------------------------------------------------------------------------------------------------------------

 

