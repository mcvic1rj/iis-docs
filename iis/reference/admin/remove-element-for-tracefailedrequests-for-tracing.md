---
title: "remove Element for traceFailedRequests for tracing | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: f80b3025-164c-4a78-94c5-5482bec391b3
caps.latest.revision: 12
author: "shirhatti"
manager: "wpickett"
---
# remove Element for traceFailedRequests for tracing
> [!NOTE]
>  For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Trace Failed Requests \<traceFailedRequests>](http://www.iis.net/ConfigReference/system.webServer/tracing/traceFailedRequests).  
  
 Removes a reference to a path from the path definitions collection.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`path`|Optional `string` attribute.<br /><br /> Specifies the path for which you want to log trace events. The path is relative to the URL (virtual directory/directory). Sub paths cannot be used. In addition, the path must be local to the directory where the definition is set.|  
  
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
 For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Trace Failed Requests \<traceFailedRequests>](http://www.iis.net/ConfigReference/system.webServer/tracing/traceFailedRequests).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-tracefailedrequests-for-tracing.md)   
 [\<clear>](../../reference/admin/clear-element-for-tracefailedrequests-for-tracing.md)