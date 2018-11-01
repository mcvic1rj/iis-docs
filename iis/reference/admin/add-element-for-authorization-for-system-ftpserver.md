---
title: "add Element for authorization for system.ftpServer | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: ea640802-d436-478a-98ee-ba72612e4b16
caps.latest.revision: 9
author: "shirhatti"
manager: "wpickett"
---
# add Element for authorization for system.ftpServer
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Authorization \<add>](http://www.iis.net/ConfigReference/system.ftpServer/security/authorization/add).  
  
 Defines an authorization rule that will either allow or deny access to specified users, groups, anonymous users, or all users.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`accessType`|Required `enum` attribute.<br /><br /> The `accessType` attribute can be one of the following possible values.<br /><br /> `Allow`<br /><br /> - Specifies a rule that allows authorization.<br /><br /> - The numeric value is 0.<br /><br /> `Deny`<br /><br /> - Specifies a rule that denies authorization.<br /><br /> - The numeric value is 1.|  
|`roles`|Optional `string` attribute.<br /><br /> Specifies roles or groups for an authorization rule.|  
|`users`|Optional `string` attribute.<br /><br /> Specifies users for an authorization rule. Multiple users can be added in a comma-separated list. In addition, the following special identifiers have been defined.<br /><br /> `*`<br /><br /> - Specifies that the rule will apply to all users.<br /><br /> `?`<br /><br /> - Specifies that the rule will apply to anonymous users.|  
|`permissions`|Optional `flags` attribute.<br /><br /> Specifies the access permissions for the rule.<br /><br /> `Read`<br /><br /> - Specifies read access for the authorization rule.<br /><br /> - The numerical value is 1.<br /><br /> `Write`<br /><br /> - Specifies write access for the authorization rule.<br /><br /> - The numerical value is 2.<br /><br /> There is no default value.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.ftpServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies security settings for an FTP server.|  
|`authorization`|Specifies the resources that a user account can and cannot access on an FTP server.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Authorization \<add>](http://www.iis.net/ConfigReference/system.ftpServer/security/authorization/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<authorization>](../../reference/admin/authorization-element-for-system-ftpserver.md)