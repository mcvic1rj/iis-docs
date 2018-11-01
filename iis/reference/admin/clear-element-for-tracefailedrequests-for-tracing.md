---
title: "clear Element for traceFailedRequests for tracing | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 4b4cfdd2-324e-4084-aed4-160e5356aa2d
caps.latest.revision: 12
author: "shirhatti"
manager: "wpickett"
---
# clear Element for traceFailedRequests for tracing
> [!NOTE]
>  For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [Trace Failed Requests \<traceFailedRequests>](http://www.iis.net/ConfigReference/system.webServer/tracing/traceFailedRequests).  
  
 Removes all references to paths from the path definitions collection.  
  
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
|`tracing`|Configures request trace settings.|  
|`traceFailedRequests`|Contains settings for tracing failed requests on the Web server.|  
  
## Remarks  
 For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [Trace Failed Requests \<traceFailedRequests>](http://www.iis.net/ConfigReference/system.webServer/tracing/traceFailedRequests).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-tracefailedrequests-for-tracing.md)   
 [\<remove>](../../reference/admin/remove-element-for-tracefailedrequests-for-tracing.md)