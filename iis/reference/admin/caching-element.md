---
title: "caching Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 5fd4632c-9085-40dd-b41d-b78498810dc2
caps.latest.revision: 23
author: "shirhatti"
manager: "wpickett"
---
# caching Element
> [!NOTE]
>  For more information about the `cache` element, see the following topic on the Microsoft IIS.net Web site: [Cache \<cache>](http://www.iis.net/ConfigReference/system.webServer/caching).  
  
 Configures output cache settings.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`enabled`|Optional `Boolean` attribute.<br /><br /> Specifies whether page output caching is enabled.<br /><br /> The default value is `true`.|  
|`enableKernelCache`|Optional `Boolean` attribute.<br /><br /> Specifies whether kernel caching is enabled.<br /><br /> The default value is `true`.|  
|`maxCacheSize`|Optional `integer` attribute.<br /><br /> Specifies the maximum size of the output cache.<br /><br /> The default value is 0. **Note:**  This setting is effective only at the level of the ApplicationHost.config file. If you set this property at a lower level, it will have no effect.|  
|`maxResponseSize`|Optional `integer` attribute.<br /><br /> Specifies the maximum response size that can be cached.<br /><br /> The default value is 262144. **Note:**  This setting is effective only at the level of the ApplicationHost.config file. If you set this property at a lower level, it will have no effect.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`profiles`|Optional element.<br /><br /> Contains a group of output cache settings that can be applied to ASP.NET pages.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
  
## Remarks  
 For more information about the `cache` element, see the following topic on the Microsoft IIS.net Web site: [Cache \<cache>](http://www.iis.net/ConfigReference/system.webServer/caching).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<profiles>](../../reference/admin/profiles-element-for-caching.md)