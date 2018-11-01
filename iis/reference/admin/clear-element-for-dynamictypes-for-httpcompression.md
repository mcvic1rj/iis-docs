---
title: "clear Element for dynamicTypes for httpCompression | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 2f229bf1-78b5-42ec-8659-1c7aa0251c96
caps.latest.revision: 21
author: "shirhatti"
manager: "wpickett"
---
# clear Element for dynamicTypes for httpCompression
> [!NOTE]
>  For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [Dynamic Types \<dynamicTypes>](http://www.iis.net/ConfigReference/system.webServer/httpCompression/dynamicTypes).  
  
 Removes all references to MIME types from the dynamic MIME type collection.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the root element in ApplicationHost.config that is the top-level section group in which this element is defined.|  
|`httpCompression`|Configures HTTP compression settings for a Web server.|  
|`dynamicTypes`|Specifies configuration settings for dynamic compression.|  
  
## Remarks  
 For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [Dynamic Types \<dynamicTypes>](http://www.iis.net/ConfigReference/system.webServer/httpCompression/dynamicTypes).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-dynamictypes-for-httpcompression.md)   
 [\<remove>](../../reference/admin/remove-element-for-dynamictypes-for-httpcompression.md)