---
title: "globalModules Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 5170d993-1f79-49d2-8f4e-dca01d125d26
caps.latest.revision: 16
author: "shirhatti"
manager: "wpickett"
---
# globalModules Element
> [!NOTE]
>  For more information about the `globalModules` element, see the following topic on the Microsoft IIS.net Web site: [Global Modules \<globalModules>](http://www.iis.net/ConfigReference/system.webServer/globalModules).  
  
 Specifies configuration settings for global modules on a Web server.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a native module to the collection of global modules.|  
|`clear`|Optional element.<br /><br /> Removes all references to native modules from the global modules collection.|  
|`remove`|Optional element.<br /><br /> Removes a reference to a specific native module from the global modules collection.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the root element in ApplicationHost.config that is the top-level section group in which this element is defined.|  
  
## Remarks  
 For more information about the `globalModules` element, see the following topic on the Microsoft IIS.net Web site: [Global Modules \<globalModules>](http://www.iis.net/ConfigReference/system.webServer/globalModules).  
  
## Default Configuration  
 The following default `<globalModules>` element is configured in the root ApplicationHost.config file in [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)] when all the role services are installed. This configuration section inherits the default configuration settings unless you use the `<clear>` element.  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-globalmodules.md)   
 [\<clear>](../../reference/admin/clear-element-for-globalmodules.md)   
 [\<remove>](../../reference/admin/remove-element-for-globalmodules.md)