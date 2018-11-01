---
title: "clear Element for scheme for httpCompression | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: abaed76d-cc76-4d7c-bb61-f329c50c344f
caps.latest.revision: 11
author: "shirhatti"
manager: "wpickett"
---
# clear Element for scheme for httpCompression
> [!NOTE]
>  For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [Scheme \<scheme>](http://www.iis.net/ConfigReference/system.webServer/httpCompression/scheme).  
  
 Removes all references to HTTP compression schemes from the HTTP compression scheme collection.  
  
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
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`httpCompression`|Configures HTTP compression settings for a Web server.|  
|`scheme`|Configures the GNU zip (Gzip) and Deflate compression schemes.|  
  
## Remarks  
 For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [Scheme \<scheme>](http://www.iis.net/ConfigReference/system.webServer/httpCompression/scheme).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<remove>](../../reference/admin/remove-element-for-scheme-for-httpcompression.md)