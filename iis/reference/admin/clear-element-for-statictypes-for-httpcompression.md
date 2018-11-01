---
title: "clear Element for staticTypes for httpCompression | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 4a93a21b-9839-439f-8733-8d763e3cd204
caps.latest.revision: 15
author: "shirhatti"
manager: "wpickett"
---
# clear Element for staticTypes for httpCompression
> [!NOTE]
>  For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [Static Types \<staticTypes>](http://www.iis.net/ConfigReference/system.webServer/httpCompression/staticTypes).  
  
 Removes all references to MIME types from the static MIME type collection.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
 None  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the root element in ApplicationHost.config that is the top-level section group in which this element is defined.|  
|`httpCompression`|Configures HTTP compression settings for a Web server.|  
|`staticTypes`|Specifies configuration settings for static compression.|  
  
## Remarks  
 For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [Static Types \<staticTypes>](http://www.iis.net/ConfigReference/system.webServer/httpCompression/staticTypes).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-statictypes-for-httpcompression.md)   
 [\<remove>](../../reference/admin/remove-element-for-statictypes-for-httpcompression.md)