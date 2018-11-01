---
title: "remove Element for traceAreas for add for traceFailedRequests for tracing | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 24e20ccf-e696-450f-9ed2-00c17f526a10
caps.latest.revision: 12
author: "shirhatti"
manager: "wpickett"
---
# remove Element for traceAreas for add for traceFailedRequests for tracing
> [!NOTE]
>  For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Trace Areas \<traceAreas>](http://www.iis.net/ConfigReference/system.webServer/tracing/traceFailedRequests/add/traceAreas).  
  
 Removes a reference to a trace area from the trace areas collection.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`provider`|Required `string` attribute.<br /><br /> Specifies which trace provider to use when tracing requests.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`tracing`|Configures request trace settings.|  
|`traceFailedRequests`|Contains settings for tracing failed requests on the Web server.|  
|`add`|Adds a path to the collection of path definitions.|  
|`traceAreas`|Configures what to trace for a given path.|  
  
## Remarks  
 For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Trace Areas \<traceAreas>](http://www.iis.net/ConfigReference/system.webServer/tracing/traceFailedRequests/add/traceAreas).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-traceareas-for-add-for-tracefailedrequests-for-tracing.md)   
 [\<clear>](../../reference/admin/clear-element-for-traceareas-for-add-for-tracefailedrequests-for-tracing.md)