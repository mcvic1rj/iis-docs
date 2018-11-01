---
title: "add Element for providers for authorization | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 99941fe2-9780-4f0a-b1ac-7ed10b2f3fe2
caps.latest.revision: 10
author: "shirhatti"
manager: "wpickett"
---
# add Element for providers for authorization
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Management Authorization Providers \<add>](http://www.iis.net/ConfigReference/system.webServer/management/authorization/providers/add).  
  
 Adds a provider to the collection of authorization providers. The default authorization provider, ConfigurationAuthorizationProvider, uses IIS configuration to store authorization rules for [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`name`|Required `string` attribute.<br /><br /> Specifies the name of the authorization provider.|  
|`type`|Required `string` attribute.<br /><br /> Specifies the authentication provider's managed type.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in Administration.config) in which this element is defined.|  
|`management`|Configures a Web server for remote management by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
|`authorization`|Configures authorization settings for remote management of the Web server.|  
|`providers`|Configures authorization providers that authorize [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] users and Windows users who connect remotely to sites and applications by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Management Authorization Providers \<add>](http://www.iis.net/ConfigReference/system.webServer/management/authorization/providers/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Root Administration.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|