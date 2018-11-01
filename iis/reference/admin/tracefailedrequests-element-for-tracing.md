---
title: "traceFailedRequests Element for tracing | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 18af8ea8-dabf-4c8e-a762-9a18b17ebb4b
caps.latest.revision: 16
author: "shirhatti"
manager: "wpickett"
---
# traceFailedRequests Element for tracing
> [!NOTE]
>  For more information about the `traceFailedRequests` element, see the following topic on the Microsoft IIS.net Web site: [Trace Failed Requests \<traceFailedRequests>](http://www.iis.net/ConfigReference/system.webServer/tracing/traceFailedRequests).  
  
 Contains settings for tracing failed requests on the Web server.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a path to the collection of path definitions.|  
|`remove`|Optional element.<br /><br /> Removes a reference to a path from the path definitions collection.|  
|`clear`|Optional element.<br /><br /> Removes all references to paths from the path definitions collection.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`tracing`|Configures request trace settings.|  
  
## Remarks  
 For more information about the `traceFailedRequests` element, see the following topic on the Microsoft IIS.net Web site: [Trace Failed Requests \<traceFailedRequests>](http://www.iis.net/ConfigReference/system.webServer/tracing/traceFailedRequests).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-tracefailedrequests-for-tracing.md)   
 [\<remove>](../../reference/admin/remove-element-for-tracefailedrequests-for-tracing.md)   
 [\<clear>](../../reference/admin/clear-element-for-tracefailedrequests-for-tracing.md)