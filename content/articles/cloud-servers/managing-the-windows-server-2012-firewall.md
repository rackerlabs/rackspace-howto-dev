---
node_id: 3429
title: Managing the Windows Server 2012 Firewall
type: article
created_date: '2013-04-23 20:59:31'
created_by: evan.nabors
last_modified_date: '2013-04-30 18:3604'
last_modified_by: evan.nabors
product: Cloud Servers
body_format: tinymce
---

 Description
------------

This article will detail how to perform the most common tasks with the
windows firewall on Windows Server 2012. This includes managing the
firewall settings and creating custom inbound and outbound firewall
rules.

Contents
--------

-   [Managing Firewall Settings](#manage)
-   [Applying Custom Rules](#custom)

Managing Firewall Settings
--------------------------

The Windows Firewall with Advanced Security is a host-based firewall
that runs on Windows Server 2012 and is turned on by default. Firewall
settings within Windows Server 2012 are managed from within the Windows
Firewall MMC (Microsoft Management Console). To review and set Firewall
settings perform the following:
1. Open the **Server Manager** from the task bar.
2. Click the **Tools menu** and select **Windows Firewall with Advanced
Security**.

![](/knowledge_center/sites/default/files/field/image/firewall.png)
3. First review the current configuration settings by selecting
**Windows Firewall Properties** from the MMC landing page. This **allows
access to modify the settings** for each of the three firewall profiles,
**Domain, Private, and Public** as well as IPSec settings.

![](/knowledge_center/sites/default/files/field/image/firewall_properties.png)

Applying Custom Rules {style="line-height: 20px;"}
---------------------

Custom Rules allow the finest level of control over inbound and outbound
traffic to your Windows Server 2012.
1. If you have not done so already load the Windows Firewall MMC by
opening the **Server Manager** from the task bar, clicking the **Tools
menu**, and selecting **Windows Firewall with Advanced Security**.
2. Select either **Inbound Rules** or **Outbound Rules** under
**Windows Firewall with Advanced Security** on the left side of the
management console. 

*Note: This will provide a listing on each of the currently configured
firewall rules. Rules that are currently enabled are denoted by green
checkbox icon, while disabled rules display a grey checkbox icon.
Rightclicking a rule will allow you toggle enable/disable.\
\
*

*![](/knowledge_center/sites/default/files/field/image/enable_disable.png)*
3. From the right side of either the **Inbound Rules** or **Outbound
Rules **tab click**New Rule**.

![](/knowledge_center/sites/default/files/field/image/new_rule.png)
4. Select **Custom** from the Rule Type radial button and click
**Next**.

![](/knowledge_center/sites/default/files/field/image/rule_type.png)
5. **Select the Program association** for the Custom Firewall Rule
either All programs or the path to a program and click **Next**.

![](/knowledge_center/sites/default/files/field/image/rule_program.png)
6. From the Protocol type field **select the protocol type** and click
**Next**.

*Note: This walkthrough uses TCP on port 80 (HTTP) for example
purposes.*

![](/knowledge_center/sites/default/files/field/image/rule_protocol.png)
7. **Select an IP address association** for both local and remote
addresses and click **Next**.

![](/knowledge_center/sites/default/files/field/image/rule_scope.png)
8. Select an action to take on matching traffic and click **Next**.

![](/knowledge_center/sites/default/files/field/image/rule_action.png)
9. Select the profiles associated with the custom rule and click
**Next**.

![](/knowledge_center/sites/default/files/field/image/rule_profile.png)
10. Provide a name for your Firewall rule and an optional description
and click **Finish**.

![](/knowledge_center/sites/default/files/field/image/rule_name.png)

11. Once created the rule will be enabled. The firewall rule can be
found on the corresponding Rule tab, either inbound or outbound
depending on the type created. To disable or delete the rule find the
rule in the MMC, right-click it, and select either Disable Rule or
Delete.

![](/knowledge_center/sites/default/files/field/image/custom_disable.png) {style="line-height: 20px;"}
-------------------------------------------------------------------------

