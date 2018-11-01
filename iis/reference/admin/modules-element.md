---
title: "modules Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 886ca982-d724-4b2c-94b8-38776eb5dc7b
caps.latest.revision: 15
author: "shirhatti"
manager: "wpickett"
---
# modules Element
> [!NOTE]
>  For more information about the `modules` element, see the following topic on the Microsoft IIS.net Web site: [Modules \<modules>](http://www.iis.net/ConfigReference/modules).  
  
 Configures modules for [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)]. The `modules` element specifies the features that are available in [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] when a user is connected to a site or an application.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a module to the collection of modules for [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
|`clear`|Optional element.<br /><br /> Removes all references to modules from the parent modules collection.|  
|`remove`|Optional element.<br /><br /> Removes a reference to a module from the collection of modules for [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
  
## Remarks  
 For more information about the `modules` element, see the following topic on the Microsoft IIS.net Web site: [Modules \<modules>](http://www.iis.net/ConfigReference/modules).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Root Administration.config<br /><br /> Site level Administration.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-modules.md)   
 [\<clear>](../../reference/admin/clear-element-for-modules.md)   
 [\<remove>](../../reference/admin/remove-element-for-modules.md)