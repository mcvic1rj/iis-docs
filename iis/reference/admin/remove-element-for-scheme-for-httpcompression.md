---
title: "remove Element for scheme for httpCompression | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 3c5d07a0-8257-4a99-b28f-dfba043051ec
caps.latest.revision: 11
author: "shirhatti"
manager: "wpickett"
---
# remove Element for scheme for httpCompression
> [!NOTE]
>  For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Scheme \<scheme>](http://www.iis.net/ConfigReference/system.webServer/httpCompression/scheme).  
  
 Removes a reference to an HTTP compression scheme from the HTTP compression scheme collection.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`name`|Required `string` attribute.<br /><br /> Specifies the name of the HTTP compression scheme to remove.|  
  
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
 For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Scheme \<scheme>](http://www.iis.net/ConfigReference/system.webServer/httpCompression/scheme).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<clear>](../../reference/admin/clear-element-for-scheme-for-httpcompression.md)