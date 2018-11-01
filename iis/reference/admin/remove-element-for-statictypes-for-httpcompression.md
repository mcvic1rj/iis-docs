---
title: "remove Element for staticTypes for httpCompression | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: aa3090cf-f57f-4834-85c0-a8fdb64c3fc6
caps.latest.revision: 16
author: "shirhatti"
manager: "wpickett"
---
# remove Element for staticTypes for httpCompression
> [!NOTE]
>  For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Static Types \<staticTypes>](http://www.iis.net/ConfigReference/system.webServer/httpCompression/staticTypes).  
  
 Removes a reference to a MIME type from the static MIME type collection.  
  
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
|`staticTypes`|Specifies configuration settings for static compression.|  
  
## Remarks  
 For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Static Types \<staticTypes>](http://www.iis.net/ConfigReference/system.webServer/httpCompression/staticTypes).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-statictypes-for-httpcompression.md)   
 [\<clear>](../../reference/admin/clear-element-for-statictypes-for-httpcompression.md)