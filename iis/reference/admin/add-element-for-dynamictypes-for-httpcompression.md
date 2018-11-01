---
title: "add Element for dynamicTypes for httpCompression | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 896dc56c-bc4f-4df3-9203-a427f0bb1081
caps.latest.revision: 28
author: "shirhatti"
manager: "wpickett"
---
# add Element for dynamicTypes for httpCompression
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Dynamic Types \<add>](http://www.iis.net/ConfigReference/system.webServer/httpCompression/dynamicTypes/add).  
  
 Adds a MIME type to the collection of dynamic MIME types.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`enabled`|Required `Boolean` attribute.<br /><br /> Specifies whether a new MIME type can use dynamic compression.<br /><br /> The default value is `true`.|  
|`mimeType`|Required `string` attribute.<br /><br /> Specifies the name of the MIME type—also called the content type—that uses dynamic compression.|  
  
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
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Dynamic Types \<add>](http://www.iis.net/ConfigReference/system.webServer/httpCompression/dynamicTypes/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<remove>](../../reference/admin/remove-element-for-dynamictypes-for-httpcompression.md)   
 [\<clear>](../../reference/admin/clear-element-for-dynamictypes-for-httpcompression.md)