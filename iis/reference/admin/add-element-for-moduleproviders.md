---
title: "add Element for moduleProviders | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 2cda6415-d117-41f0-b4a8-9b70e19220de
caps.latest.revision: 15
author: "shirhatti"
manager: "wpickett"
---
# add Element for moduleProviders
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Module Providers \<add>](http://www.iis.net/ConfigReference/moduleProviders/add).  
  
 Adds a module to the list of module providers for [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|||  
|-|-|  
|Attribute|Description|  
|`name`|Required `string` attribute.<br /><br /> Specifies the unique name of a managed module on the Web server.|  
|`type`|Required `string` attribute.<br /><br /> Specifies the managed type of a managed module.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|||  
|-|-|  
|Element|Description|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`moduleProviders`|Configures module providers for [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Module Providers \<add>](http://www.iis.net/ConfigReference/moduleProviders/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Root Administration.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<modules>](../../reference/admin/modules-element.md)