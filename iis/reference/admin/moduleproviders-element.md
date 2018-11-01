---
title: "moduleProviders Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: e11f2e1e-db5f-4193-83a7-d4a4aeec00ab
caps.latest.revision: 15
author: "shirhatti"
manager: "wpickett"
---
# moduleProviders Element
> [!NOTE]
>  For more information about the `moduleProviders` element, see the following topic on the Microsoft IIS.net Web site: [Module Providers \<moduleProviders>](http://www.iis.net/ConfigReference/moduleProviders).  
  
 Configures module providers for [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)]. A module provider contains the registration information for a module and determines whether a module can run in [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a module to the collection of module providers for [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
|`clear`|Optional element.<br /><br /> Removes all references to modules from the module providers collection.|  
|`remove`|Optional element.<br /><br /> Removes a reference to a module from the collection of module providers for [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
  
## Remarks  
 For more information about the `moduleProviders` element, see the following topic on the Microsoft IIS.net Web site: [Module Providers \<moduleProviders>](http://www.iis.net/ConfigReference/moduleProviders).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Root Administration.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-moduleproviders.md)   
 [\<clear>](../../reference/admin/clear-element-for-moduleproviders.md)   
 [\<remove>](../../reference/admin/remove-element-for-moduleproviders.md)