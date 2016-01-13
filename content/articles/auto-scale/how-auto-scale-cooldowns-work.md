---
node_id: 3840
title: How Auto Scale Cooldowns Work
type: article
created_date: '2013-12-21 04:55:45'
created_by: maria.abrahms
last_modified_date: '2014-05-13 12:5408'
last_modified_by: kyle.laffoon
products: Auto Scale
body_format: tinymce
---

undefined&ndash;even if it is triggered by an event. A
policy cooldown controls how often a single, specific, policy can be
executed. For example, a scale-up policy cooldown restricts how often
the scale-up is executed despite being triggered by an event, which
allows scale-ups to fully deploy before another scale-up can occur.
Conversely, a scale-down policy cooldown can allow for the graceful
removal of servers by restricting the removal of too many servers at
once even if multiple scale-downs are rapidly triggered. Policy
cooldowns allow you to scale up fast and scale down slowly.

### Cooldowns Graph

The following graphs illustrates how cooldowns affect policy execution.

![](/knowledge_center/sites/default/files/field/image/Slide6.png)

 

![](/knowledge_center/sites/default/files/field/image/Slide7.png)

