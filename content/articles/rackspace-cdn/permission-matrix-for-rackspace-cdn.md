---
node_id: 4635
title: Permission Matrix for Rackspace CDN
type: article
created_date: '2015-04-07'
created_by: Catherine Richardson
last_modified_date: '2016-01-11'
last_modified_by: Rose Contreras
product: Rackspace CDN
body_format: tinymce
---

The following permissions matrix displays specific permissions for the
roles in Rackspace CDN. The matrix displays the method names and the
roles that are supported.

Rackspace CDN RBAC
------------------

| Endpoint                                 | RBAC-Creator                                                                                           | RBAC-Observer                                                                                          | RBAC-Admin                                                                                             | RBAC-Operator                                                                                          |
|------------------------------------------|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| GET /                                    | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} |
| GET /ping                                | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} |
| GET /health                              | ![](/knowledge_center/sites/default/files/field/image/red%20X.png){width="37" height="41"}             | ![](/knowledge_center/sites/default/files/field/image/red%20X.png){width="37" height="41"}             | ![](/knowledge_center/sites/default/files/field/image/red%20X.png){width="37" height="41"}             | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} |
| GET /health/{subsystem}                  | ![](/knowledge_center/sites/default/files/field/image/red%20X.png){width="37" height="41"}             | ![](/knowledge_center/sites/default/files/field/image/red%20X.png){width="37" height="41"}             | ![](/knowledge_center/sites/default/files/field/image/red%20X.png){width="37" height="41"}             | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} |
| POST /services                           | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} | ![](/knowledge_center/sites/default/files/field/image/red%20X.png){width="37" height="41"}             | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} | ![](/knowledge_center/sites/default/files/field/image/red%20X.png){width="37" height="41"}             |
| GET /services                            | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} |
| GET /services/\\{service\_id\\}          | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} |
| PATCH /services/\\{service\_id\\}        | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} | ![](/knowledge_center/sites/default/files/field/image/red%20X.png){width="37" height="41"}             | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} | ![](/knowledge_center/sites/default/files/field/image/red%20X.png){width="37" height="41"}             |
| DELETE /services/\\{service\_id\\}       | ![](/knowledge_center/sites/default/files/field/image/red%20X.png){width="37" height="41"}             | ![](/knowledge_center/sites/default/files/field/image/red%20X.png){width="37" height="41"}             | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} | ![](/knowledge_center/sites/default/files/field/image/red%20X.png){width="37" height="41"}             |
| DELETE /service/\\{service\_id\\}/assets | ![](/knowledge_center/sites/default/files/field/image/red%20X.png){width="37" height="41"}             | ![](/knowledge_center/sites/default/files/field/image/red%20X.png){width="37" height="41"}             | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} | ![](/knowledge_center/sites/default/files/field/image/red%20X.png){width="37" height="41"}             |
| GET /flavors                             | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} |
| GET /flavors/\\{flavor\_id\\}            | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} |
| POST /flavors                            | ![](/knowledge_center/sites/default/files/field/image/red%20X.png){width="37" height="41"}             | ![](/knowledge_center/sites/default/files/field/image/red%20X.png){width="37" height="41"}             | ![](/knowledge_center/sites/default/files/field/image/red%20X.png){width="37" height="41"}             | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} |
| DELETE /flavors/\\{flavor\_id\\}         | ![](/knowledge_center/sites/default/files/field/image/red%20X.png){width="37" height="41"}             | ![](/knowledge_center/sites/default/files/field/image/red%20X.png){width="37" height="41"}             | ![](/knowledge_center/sites/default/files/field/image/red%20X.png){width="37" height="41"}             | ![](/knowledge_center/sites/default/files/field/image/green%20checkmark_4.png){width="41" height="39"} |

### <span> </span>

[&lt; Permission Matrices for RBAC](/howto/permissions-matrix-for-role-based-access-control-rbac)
--------------------------------------------------------------------------------------------------------------------------------------------



