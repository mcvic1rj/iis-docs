---
title: "failureDefinitions Element for add for traceFailedRequests for tracing | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 3722c3f5-ce7b-40f7-9f9b-816664853a42
caps.latest.revision: 20
author: "shirhatti"
manager: "wpickett"
---
# failureDefinitions Element for add for traceFailedRequests for tracing
> [!NOTE]
>  For more information about the `failureDefinitions` element, see the following topic on the Microsoft IIS.net Web site: [Failure Definitions \<failureDefinitions>](http://www.iis.net/ConfigReference/system.webServer/tracing/traceFailedRequests/add/failureDefinitions).  
  
 Defines the conditions in which to trace requests.  
  
> [!NOTE]
>  The first condition that is met will generate a failed request trace log file for the request.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`statusCodes`|Optional `string` attribute.<br /><br /> Specifies the status code(s) you want to trace. You can enter multiple status codes in this list by using commas to separate each code. You can also refine your status codes using sub status codes, such as "404.2, 500" or a range of sub status codes such as "400-599". If you do not specify substatus codes, all substatus codes for the given status code will be traced. Status codes must be from 100 to 999, and substatus codes must be from 1 to 999.|  
|`timeTaken`|Optional `timeSpan` attribute.<br /><br /> Specifies the maximum time that a request may spend in processing before it is marked as failed and then traced.<br /><br /> The default value is 00:00:00.|  
|`verbosity`|Optional `enum` attribute.<br /><br /> Specifies the minimum amount of information and the type of information that is saved to the trace log. If the verbosity is set to `Error,` a failed request trace log file for the request will be created when the first trace event whose verbosity is either `Error` or `CriticalError` is received.<br /><br /> The `verbosity` attribute can be one of the following possible values.<br /><br /> The default value is `Ignore.`<br /><br /> `Ignore`:<br /><br /> - Provides no information about the request activity. The numeric value is 0.<br /><br /> `CriticalError`:<br /><br /> - Provides information about actions that can cause a process to exit or that are about to cause a process to exit. The numeric value is 1.<br /><br /> `Error`:<br /><br /> - Provides information about components that experience an error and cannot continue to process requests. These errors usually indicate a server-side problem. The numeric value is 2.<br /><br /> `Warning`:<br /><br /> - Provides information about components that experience an error but that can continue to process the request. The numeric value is 3.|  
  
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
  
## Remarks  
 For more information about the `failureDefinitions` element, see the following topic on the Microsoft IIS.net Web site: [Failure Definitions \<failureDefinitions>](http://www.iis.net/ConfigReference/system.webServer/tracing/traceFailedRequests/add/failureDefinitions).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<traceFailedRequests>](../../reference/admin/tracefailedrequests-element-for-tracing.md)   
 [TraceFailedRequestsSection Class](../../reference/admin/tracefailedrequestssection-class.md)