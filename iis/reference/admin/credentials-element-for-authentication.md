---
title: "credentials Element for authentication | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 94c5604f-d9ee-44e0-a613-75c105e62132
caps.latest.revision: 12
author: "shirhatti"
manager: "wpickett"
---
# credentials Element for authentication
> [!NOTE]
>  For more information about the `credentials` element, see the following topic on the Microsoft IIS.net Web site: [Management Authentication Credentials \<credentials>](http://www.iis.net/ConfigReference/system.webServer/management/authentication/credentials).  
  
 Configures credentials for [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] user accounts. [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] users can use [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] to connect to sites and applications for which they are authorized by a server administrator.  
  
> [!NOTE]
>  This configuration only applies when you use the default ConfigurationAuthenticationProvider as your authentication provider.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds an [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] user account to the collection of [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] users.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in Administration.config) in which this element is defined.|  
|`management`|Configures a Web server for remote management by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
|`authentication`|Configures authentication settings for remote management of the Web server.|  
  
## Remarks  
 For more information about the `credentials` element, see the following topic on the Microsoft IIS.net Web site: [Management Authentication Credentials \<credentials>](http://www.iis.net/ConfigReference/system.webServer/management/authentication/credentials).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Root Administration.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-credentials-for-authentication.md)   
 [\<authorization>](../../reference/admin/authorization-element-for-management.md)