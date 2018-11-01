---
title: "add Element for staticTypes for httpCompression | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 6f21a6a2-c56b-4702-a34b-5ef6dc522a8d
caps.latest.revision: 22
author: "shirhatti"
manager: "wpickett"
---
# add Element for staticTypes for httpCompression
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Static Types \<add>](http://www.iis.net/ConfigReference/system.webServer/httpCompression/staticTypes/add).  
  
 Adds a MIME type to the collection of static MIME types.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`enabled`|Required `Boolean` attribute.<br /><br /> Specifies whether a new MIME type can use static compression.<br /><br /> The default value is `True`.|  
|`mimeType`|Required `string` attribute.<br /><br /> Specifies the name of the MIME type—also called the content type—that uses static compression.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the root element in ApplicationHost.config that is the top-level section group in which this element is defined.|  
|`httpCompression`|Configures HTTP compression settings for a Web server.|  
|`staticTypes`|Specifies configuration settings for static compression.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Static Types \<add>](http://www.iis.net/ConfigReference/system.webServer/httpCompression/staticTypes/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<remove>](../../reference/admin/remove-element-for-statictypes-for-httpcompression.md)   
 [\<clear>](../../reference/admin/clear-element-for-statictypes-for-httpcompression.md)