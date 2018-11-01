---
title: "add Element for credentials for authentication | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 7256d290-90e1-4756-87a9-6d69b7aa9fab
caps.latest.revision: 13
author: "shirhatti"
manager: "wpickett"
---
# add Element for credentials for authentication
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Management Authentication Credentials \<add>](http://www.iis.net/ConfigReference/system.webServer/management/authentication/credentials/add).  
  
 Adds an [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] user account to the collection of [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] users. [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] users can use [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] to connect to sites and applications for which they are authorized by a server administrator.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`name`|Required `string` attribute.<br /><br /> Specifies the user name of the [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] user account.|  
|`password`|Required `string` attribute.<br /><br /> Specifies the SHA256 hash of the user's password for the [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] user account. This attribute is case sensitive.<br /><br /> If you configure an [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] user account by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)], the password hash is computed automatically. If you want to calculate the hash of a password programmatically, you can use the `System.Security.Cryptography.SHA256`<br /><br /> `ComputeHash` method. For more information, see [SHA256 Class](http://go.microsoft.com/fwlink/?LinkId=96088) on MSDN.|  
|`enabled`|Optional `Boolean` attribute.<br /><br /> Specifies whether the [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] user is enabled (`true`) or disabled (`false`). When `true`, the [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] user can use [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] to connect to all sites and applications for which they have authorized by a server administrator on the Web server.<br /><br /> The default value is `true`.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in Administration.config) in which this element is defined.|  
|`management`|Configures a Web server for remote management by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
|`authentication`|Configures authentication settings for remote management of the Web server.|  
|`credentials`|Configures credentials for [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] user accounts.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Management Authentication Credentials \<add>](http://www.iis.net/ConfigReference/system.webServer/management/authentication/credentials/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Root Administration.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<authorization>](../../reference/admin/authorization-element-for-management.md)