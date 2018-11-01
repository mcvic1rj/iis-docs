---
title: "clear Element for traceUrls for httpTracing | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 6629578e-afde-45de-a0ff-6b05d3ceeced
caps.latest.revision: 14
author: "shirhatti"
manager: "wpickett"
---
# clear Element for traceUrls for httpTracing
> [!NOTE]
>  For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [Trace URLs \<traceUrls>](http://www.iis.net/ConfigReference/system.webServer/httpTracing/traceUrls).  
  
 Removes all references to trace URLs from the trace URL collection.  
  
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
|`httpTracing`|Specifies configuration settings for request-based ETW tracing.|  
|`traceUrls`|Specifies the URL for which you want to enable request-based ETW tracing.|  
  
## Remarks  
 For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [Trace URLs \<traceUrls>](http://www.iis.net/ConfigReference/system.webServer/httpTracing/traceUrls).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-traceurls-for-httptracing.md)   
 [\<remove>](../../reference/admin/remove-element-for-traceurls-for-httptracing.md)