---
title: "modules Element for system.webServer | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: e55e85ab-da96-4bf6-9b09-1347cbfe97f8
caps.latest.revision: 15
author: "shirhatti"
manager: "wpickett"
---
# modules Element for system.webServer
> [!NOTE]
>  For more information about the `modules` element, see the following topic on the Microsoft IIS.net Web site: [Modules \<modules>](http://www.iis.net/ConfigReference/system.webServer/modules).  
  
 Specifies configuration settings for modules on a Web server.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a module to the collection of modules.|  
|`clear`|Optional element.<br /><br /> Removes all references to modules from the modules collection.|  
|`remove`|Optional element.<br /><br /> Removes a reference to a module from the modules collection.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
  
## Remarks  
 For more information about the `modules` element, see the following topic on the Microsoft IIS.net Web site: [Modules \<modules>](http://www.iis.net/ConfigReference/system.webServer/modules).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-modules-for-system-webserver.md)   
 [\<remove>](../../reference/admin/remove-element-for-modules-for-system-webserver.md)   
 [\<clear>](../../reference/admin/clear-element-for-modules-for-system-webserver.md)