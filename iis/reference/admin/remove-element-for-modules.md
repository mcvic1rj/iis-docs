---
title: "remove Element for modules | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 7eebd6fe-8add-4909-84eb-daa4d468f6d3
caps.latest.revision: 12
author: "shirhatti"
manager: "wpickett"
---
# remove Element for modules
> [!NOTE]
>  For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Modules \<modules>](http://www.iis.net/ConfigReference/modules/add).  
  
 Removes a reference to a module from the collection of modules for [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`name`|Required `string` attribute.<br /><br /> Specifies the unique name of a managed module on the Web server.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`modules`|Configures modules for [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
  
## Remarks  
 For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Modules \<modules>](http://www.iis.net/ConfigReference/modules/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Root Administration.config<br /><br /> Site level Administration.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|