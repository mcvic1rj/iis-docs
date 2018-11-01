---
title: "remove Element for profiles for caching | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: ea783e41-a8cb-47b6-b8e6-fbe0cbcc6ce7
caps.latest.revision: 20
author: "shirhatti"
manager: "wpickett"
---
# remove Element for profiles for caching
> [!NOTE]
>  For more information about the `profiles` element, see the following topic on the Microsoft IIS.net Web site: [Caching Profiles \<profiles>](http://www.iis.net/ConfigReference/system.webServer/caching/profiles/add).  
  
 Removes a reference to an output caching profile from the output caching profile collection.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`extension`|Required `string` attribute.<br /><br /> Specifies the file type extension for the files you want to cache.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`caching`|Configures output cache settings.|  
|`profiles`|Configures the profile to use for output caching.|  
  
## Remarks  
 For more information about the `profiles` element, see the following topic on the Microsoft IIS.net Web site: [Caching Profiles \<profiles>](http://www.iis.net/ConfigReference/system.webServer/caching/profiles/add).  
  
## Example  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-profiles-for-caching.md)   
 [\<clear>](../../reference/admin/clear-element-for-profiles-for-caching.md)