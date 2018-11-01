---
title: "authorization Element for management | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 9171be0a-de34-4b60-ae42-c4a062d8bc76
caps.latest.revision: 12
author: "shirhatti"
manager: "wpickett"
---
# authorization Element for management
> [!NOTE]
>  For more information about the `authorization` element, see the following topic on the Microsoft IIS.net Web site: [Management Authorization \<authorization>](http://www.iis.net/ConfigReference/system.webServer/management/authorization).  
  
 Configures authorization settings for remote management of the Web server.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`defaultProvider`|Optional `string` attribute.<br /><br /> Specifies the default provider that authorizes [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] users and Windows users who connect remotely to the Web server by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].<br /><br /> If you change the default provider, you must restart the Management Service (WMSVC) for changes to take effect. If you have [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] open, you must also reopen [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`authorizationRules`|Optional element.<br /><br /> Configures the [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] users and Windows users who are authorized to connect to a site or an application by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
|`providers`|Optional element.<br /><br /> Configures authorization providers that authorize [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] users and Windows users who connect remotely to sites and applications by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in Administration.config) in which this element is defined.|  
|`management`|Configures a Web server for remote management by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
  
## Remarks  
 For more information about the `authorization` element, see the following topic on the Microsoft IIS.net Web site: [Management Authorization \<authorization>](http://www.iis.net/ConfigReference/system.webServer/management/authorization).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Root Administration.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<authorizationRules>](../../reference/admin/authorizationrules-element-for-authorization.md)   
 [\<providers>](../../reference/admin/providers-element-for-authorization.md)