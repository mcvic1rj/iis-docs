---
title: "providers Element for authorization | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 4e9269eb-2fd1-4bcb-a2ea-42eafa0dfddd
caps.latest.revision: 11
author: "shirhatti"
manager: "wpickett"
---
# providers Element for authorization
> [!NOTE]
>  For more information about the `providers` element, see the following topic on the Microsoft IIS.net Web site: [Management Authorization Providers \<providers>](http://www.iis.net/ConfigReference/system.webServer/management/authorization/providers).  
  
 Configures authorization providers that authorize [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] users and Windows users who connect remotely to sites and applications by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)]. The default authorization provider, ConfigurationAuthorizationProvider, uses IIS configuration to store authorization rules for [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a provider to the collection of authorization providers.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in Administration.config) in which this element is defined.|  
|`management`|Configures a Web server for remote management by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
|`authorization`|Configures authorization settings for remote management of the Web server.|  
  
## Remarks  
 For more information about the `providers` element, see the following topic on the Microsoft IIS.net Web site: [Management Authorization Providers \<providers>](http://www.iis.net/ConfigReference/system.webServer/management/authorization/providers).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Root Administration.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-providers-for-authorization.md)