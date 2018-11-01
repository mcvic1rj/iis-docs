---
title: "clear Element for traceAreas for add for traceFailedRequests for tracing | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: f69613fb-ed62-4432-9395-b8e36345ad11
caps.latest.revision: 11
author: "shirhatti"
manager: "wpickett"
---
# clear Element for traceAreas for add for traceFailedRequests for tracing
> [!NOTE]
>  For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [Trace Areas \<traceAreas>](http://www.iis.net/ConfigReference/system.webServer/tracing/traceFailedRequests/add/traceAreas).  
  
 Removes all references to trace areas from the trace areas collection.  
  
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
|`Tracing`|Configures request trace settings.|  
|`traceFailedRequests`|Contains settings for tracing failed requests on the Web server.|  
|`add`|Adds a path to the collection of path definitions.|  
|`traceAreas`|Configures what to trace for a given path.|  
  
## Remarks  
 For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [Trace Areas \<traceAreas>](http://www.iis.net/ConfigReference/system.webServer/tracing/traceFailedRequests/add/traceAreas).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-traceareas-for-add-for-tracefailedrequests-for-tracing.md)   
 [\<remove>](../../reference/admin/remove-element-for-traceareas-for-add-for-tracefailedrequests-for-tracing.md)