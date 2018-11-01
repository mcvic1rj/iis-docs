---
title: "trustedProviders Element for management | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 49294b04-fd12-4697-9430-c9a72f0d320d
caps.latest.revision: 11
author: "shirhatti"
manager: "wpickett"
---
# trustedProviders Element for management
> [!NOTE]
>  For more information about the `trustedProviders` element, see the following topic on the Microsoft IIS.net Web site: [Management Trusted Providers \<trustedProviders>](http://www.iis.net/ConfigReference/system.webServer/management/trustedProviders).  
  
 Configures the providers that are trusted by [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] and the Management Service (WMSVC).  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`allowUntrustedProviders`|Optional `Boolean` attribute.<br /><br /> Specifies whether untrusted providers can run. **Important:**  For security reasons, it is not recommended to change this value to `true`, because it will allow untrusted code to run on your server. Instead, you should always test a provider and add it to the trusted providers collection only when it is safe. <br /><br /> The default value is `false`.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a provider to the collection of providers that are trusted to be run by [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] and the Management Service (WMSVC).|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in Administration.config) in which this element is defined.|  
|`management`|Configures a Web server for remote management by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
  
## Remarks  
 For more information about the `trustedProviders` element, see the following topic on the Microsoft IIS.net Web site: [Management Trusted Providers \<trustedProviders>](http://www.iis.net/ConfigReference/system.webServer/management/trustedProviders).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Root Administration.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-trustedproviders-for-management.md)