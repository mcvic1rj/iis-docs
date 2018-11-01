---
title: "add Element for trustedProviders for management | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 0717f111-5738-4cac-98a1-a7ebdc9a695a
caps.latest.revision: 10
author: "shirhatti"
manager: "wpickett"
---
# add Element for trustedProviders for management
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Management Trusted Providers \<add>](http://www.iis.net/ConfigReference/system.webServer/management/trustedProviders/add).  
  
 Adds a provider to the collection of providers that are trusted to be run by [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] and the Management Service (WMSVC).  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`type`|Required `string` attribute.<br /><br /> Specifies the assembly-qualified type name for the provider.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in Administration.config) in which this element is defined.|  
|`trustedProviders`|Configures the providers that are trusted by [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] and the Management Service (WMSVC).|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Management Trusted Providers \<add>](http://www.iis.net/ConfigReference/system.webServer/management/trustedProviders/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Root Administration.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|