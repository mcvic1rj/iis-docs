---
title: "remove Element for dynamicTypes for httpCompression | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: d364e9f4-c930-4119-a622-543f20d4d626
caps.latest.revision: 22
author: "shirhatti"
manager: "wpickett"
---
# remove Element for dynamicTypes for httpCompression
> [!NOTE]
>  For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Dynamic Types \<dynamicTypes>](http://www.iis.net/ConfigReference/system.webServer/httpCompression/dynamicTypes).  
  
 Removes a reference to a MIME type from the dynamic MIME type collection.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`mimeType`|Required `string` attribute.<br /><br /> Specifies the name of the MIME type—also called the content type—that uses static compression.|  
  
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
 For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Dynamic Types \<dynamicTypes>](http://www.iis.net/ConfigReference/system.webServer/httpCompression/dynamicTypes).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-dynamictypes-for-httpcompression.md)   
 [\<clear>](../../reference/admin/clear-element-for-dynamictypes-for-httpcompression.md)