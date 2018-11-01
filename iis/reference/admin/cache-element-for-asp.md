---
title: "cache Element for asp | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: fba10d80-a2b1-4bc8-97d2-3e7e989c4d29
caps.latest.revision: 27
author: "shirhatti"
manager: "wpickett"
---
# cache Element for asp
> [!NOTE]
>  For more information about the `cache` element, see the following topic on the Microsoft IIS.net Web site: [ASP Cache \<cache>](http://www.iis.net/ConfigReference/system.webServer/asp/cache).  
  
 Configures Active Server Pages (ASP) cache settings.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`diskTemplateCacheDirectory`|Optional `string` attribute.<br /><br /> Specifies the name of the directory where ASP stores compiled ASP templates when the in-memory cache overflows.<br /><br /> The default value is "%*systemdrive*%\inetpub\temp\ASP Compiled Templates".|  
|`enableTypelibCache`|Optional `Boolean` attribute.<br /><br /> Specifies whether type libraries are cached.<br /><br /> The default value is `true` .|  
|`maxDiskTemplateCacheFiles`|Optional `integer` attribute.<br /><br /> Specifies the maximum number of compiled ASP templates that can be stored. This value is an integer range from 0 to 2147483647.<br /><br /> The default value is 2000.|  
|`scriptEngineCacheMax`|Optional `integer` attribute.<br /><br /> Specifies the maximum number of scripting engines that ASP pages will keep cached in memory. This value is an integer range from 0 to 2147483647.<br /><br /> The default value is 250.|  
|`scriptFileCacheSize`|Optional `integer` attribute.<br /><br /> Specifies the number of precompiled script files to cache. If set to 0, no script files are cached. If set to 4294967295, all script files requested are cached. This property is used to tune performance, depending on the amount of available memory and the amount of script file traffic.<br /><br /> The default value is 500.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`asp`|Configures settings for ASP applications.|  
  
## Remarks  
 For more information about the `cache` element, see the following topic on the Microsoft IIS.net Web site: [ASP Cache \<cache>](http://www.iis.net/ConfigReference/system.webServer/asp/cache).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<comPlus>](../../reference/admin/complus-element-for-asp.md)   
 [\<limits>](../../reference/admin/limits-element-for-asp.md)   
 [\<session>](../../reference/admin/session-element-for-asp.md)