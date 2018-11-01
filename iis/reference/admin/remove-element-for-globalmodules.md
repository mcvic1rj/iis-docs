---
title: "remove Element for globalModules | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: de8c84ee-3239-4144-95fb-112136011722
caps.latest.revision: 16
author: "shirhatti"
manager: "wpickett"
---
# remove Element for globalModules
> [!NOTE]
>  For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Global Modules \<globalModules>](http://www.iis.net/ConfigReference/system.webServer/globalModules/add).  
  
 Specifies a global module to be removed from the Web server.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`name`|Required `string` attribute.<br /><br /> Specifies the name of the global module.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the root element in ApplicationHost.config that is the top-level section group in which this element is defined.|  
|`globalModules`|Specifies configuration settings for global modules on a Web server.|  
  
## Remarks  
 For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Global Modules \<globalModules>](http://www.iis.net/ConfigReference/system.webServer/globalModules/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|