---
title: "traceAreas Element for add for traceFailedRequests for tracing | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 143defaa-0ae7-4ace-b185-1536ae1981f0
caps.latest.revision: 13
author: "shirhatti"
manager: "wpickett"
---
# traceAreas Element for add for traceFailedRequests for tracing
> [!NOTE]
>  For more information about the `traceAreas` element, see the following topic on the Microsoft IIS.net Web site: [Trace Areas \<traceAreas>](http://www.iis.net/ConfigReference/system.webServer/tracing/traceFailedRequests/add/traceAreas).  
  
 Configures what to trace for a given path by specifying the providers, provider areas, and verbosity for each provider.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a trace area to the collection of trace areas.|  
|`remove`|Optional element.<br /><br /> Removes a reference to a trace area from the trace areas collection.|  
|`clear`|Optional element.<br /><br /> Removes all references to trace areas from the trace areas collection.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`tracing`|Configures request trace settings.|  
|`traceFailedRequests`|Contains settings for tracing failed requests on the Web server.|  
|`add`|Adds a path to the collection of path definitions.|  
  
## Remarks  
 For more information about the `traceAreas` element, see the following topic on the Microsoft IIS.net Web site: [Trace Areas \<traceAreas>](http://www.iis.net/ConfigReference/system.webServer/tracing/traceFailedRequests/add/traceAreas).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-traceareas-for-add-for-tracefailedrequests-for-tracing.md)   
 [\<remove>](../../reference/admin/remove-element-for-traceareas-for-add-for-tracefailedrequests-for-tracing.md)   
 [\<clear>](../../reference/admin/clear-element-for-traceareas-for-add-for-tracefailedrequests-for-tracing.md)