---
title: "dynamicTypes Element for httpCompression | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: a4bc5515-7cc7-4ec3-b430-a9695c61613d
caps.latest.revision: 21
author: "shirhatti"
manager: "wpickett"
---
# dynamicTypes Element for httpCompression
> [!NOTE]
>  For more information about the `dynamicTypes` element, see the following topic on the Microsoft IIS.net Web site: [Dynamic Types \<dynamicTypes>](http://www.iis.net/ConfigReference/system.webServer/httpCompression/dynamicTypes).  
  
 Specifies configuration settings for dynamic compression.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a MIME type to the collection of dynamic MIME types.|  
|`remove`|Optional element.<br /><br /> Removes a reference to a MIME type from the dynamic MIME type collection.|  
|`clear`|Optional element.<br /><br /> Removes all references to MIME types from the dynamic MIME type collection.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the root element in ApplicationHost.config that is the top-level section group in which this element is defined.|  
|`httpCompression`|Configures HTTP compression settings for a Web server.|  
  
## Remarks  
 For more information about the `dynamicTypes` element, see the following topic on the Microsoft IIS.net Web site: [Dynamic Types \<dynamicTypes>](http://www.iis.net/ConfigReference/system.webServer/httpCompression/dynamicTypes).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root level Web.config<br /><br /> Application level Web.config<br /><br /> Virtual or physical directory level Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-dynamictypes-for-httpcompression.md)   
 [\<remove>](../../reference/admin/remove-element-for-dynamictypes-for-httpcompression.md)   
 [\<clear>](../../reference/admin/clear-element-for-dynamictypes-for-httpcompression.md)