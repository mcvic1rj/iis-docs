---
title: "add Element for traceAreas for add for traceFailedRequests for tracing | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: dc5c3c27-ee24-4a9a-ade3-4513a7d0ee97
caps.latest.revision: 21
author: "shirhatti"
manager: "wpickett"
---
# add Element for traceAreas for add for traceFailedRequests for tracing
> [!NOTE]
>  For more information about the add element, see the following topic on the Microsoft IIS.net Web site: [Adding Trace Areas \<add>](http://www.iis.net/ConfigReference/system.webServer/tracing/traceFailedRequests/add/traceAreas/add).  
  
 Adds a trace area to the collection of trace areas for tracing failed requests.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`areas`|Optional `string` attribute.<br /><br /> Specifies a comma-delimited list, without spaces, that contains what content areas to trace for a given provider. When the `provider` attribute is set to "ASPNET," the possible values are "Infrastructure", "Module", "Page", and "AppServices". When the `provider` attribute is set to "WWW server", the possible values are "Authentication", "Security", "Filter", "StaticFile", "CGI", "Compression", "Cache", "RequestNotifications", and "All".|  
|`provider`|Required `string` attribute.<br /><br /> Specifies which trace provider to use when tracing requests by name.|  
|`verbosity`|Optional `enum` attribute.<br /><br /> Specifies the amount and type of information that is saved to the trace log.<br /><br /> The `verbosity` attribute can be one of the following possible values. The default is `Verbose`.<br /><br /> `General`:<br /><br /> - Returns information that provides context for the request activity, for example, a `GENERAL_REQUEST_START` event that logs the URL and the verb for the request. The numeric value is 0.<br /><br /> `CriticalError`:<br /><br /> - Provides information about actions that can cause a process to exit. The numeric value is 1.<br /><br /> `Error`:<br /><br /> - Provides information about components that experience an error and cannot continue to process requests. These errors usually indicate a server-side problem. The numeric value is 2.<br /><br /> `Warning`:<br /><br /> - Provides information about components that experience an error but that can continue to process the request. The numeric value is 3.<br /><br /> `Information`:<br /><br /> - Provides general information about requests. The numeric value is 4.<br /><br /> `Verbose`:<br /><br /> - Provides detailed information about requests. The numeric value is 5.|  
  
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
 For more information about the add element, see the following topic on the Microsoft IIS.net Web site: [Adding Trace Areas \<add>](http://www.iis.net/ConfigReference/system.webServer/tracing/traceFailedRequests/add/traceAreas/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<remove>](../../reference/admin/remove-element-for-traceareas-for-add-for-tracefailedrequests-for-tracing.md)   
 [\<clear>](../../reference/admin/clear-element-for-traceareas-for-add-for-tracefailedrequests-for-tracing.md)