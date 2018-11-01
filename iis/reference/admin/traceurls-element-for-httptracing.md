---
title: "traceUrls Element for httpTracing | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: fd51784c-76b7-488b-abc3-63eaac7cfd2a
caps.latest.revision: 15
author: "shirhatti"
manager: "wpickett"
---
# traceUrls Element for httpTracing
> [!NOTE]
>  For more information about the `traceUrls` element, see the following topic on the Microsoft IIS.net Web site: [Trace URLs \<traceUrls>](http://www.iis.net/ConfigReference/system.webServer/httpTracing/traceUrls).  
  
 Specifies the URL for which you want to enable request-based ETW tracing.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a trace URL to the collection of trace URLs.|  
|`remove`|Optional element.<br /><br /> Removes a reference to a trace URL from the trace URL collection.|  
|`clear`|Optional element.<br /><br /> Removes all references to trace URLs from the trace URL collection.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`httpTracing`|Specifies configuration settings for request-based ETW tracing.|  
  
## Remarks  
 For more information about the `traceUrls` element, see the following topic on the Microsoft IIS.net Web site: [Trace URLs \<traceUrls>](http://www.iis.net/ConfigReference/system.webServer/httpTracing/traceUrls).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-traceurls-for-httptracing.md)   
 [\<remove>](../../reference/admin/remove-element-for-traceurls-for-httptracing.md)   
 [\<clear>](../../reference/admin/clear-element-for-traceurls-for-httptracing.md)