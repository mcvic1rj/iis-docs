---
title: "remove Element for traceUrls for httpTracing | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 14d76e2d-c7ac-4efc-b491-696ab564506d
caps.latest.revision: 15
author: "shirhatti"
manager: "wpickett"
---
# remove Element for traceUrls for httpTracing
> [!NOTE]
>  For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Trace URLs \<traceUrls>](http://www.iis.net/ConfigReference/system.webServer/httpTracing/traceUrls).  
  
 Removes a reference to a trace URL from the trace URL collection.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`value`|Required `string` attribute.<br /><br /> Specifies the URL for which tracing should be disabled.|  
  
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
 For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Trace URLs \<traceUrls>](http://www.iis.net/ConfigReference/system.webServer/httpTracing/traceUrls).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-traceurls-for-httptracing.md)   
 [\<clear>](../../reference/admin/clear-element-for-traceurls-for-httptracing.md)