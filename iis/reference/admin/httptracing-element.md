---
title: "httpTracing Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 417c3c26-d50a-4633-add5-7d5e65c8b79c
caps.latest.revision: 13
author: "shirhatti"
manager: "wpickett"
---
# httpTracing Element
> [!NOTE]
>  For more information about the `httpTracing` element, see the following topic on the Microsoft IIS.net Web site: [HTTP Tracing \<httpTracing>](http://www.iis.net/ConfigReference/system.webServer/httpTracing).  
  
 Specifies configuration settings for request-based Event Tracing for Windows (ETW) tracing.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`traceUrls`|Optional element.<br /><br /> Specifies the URL for which you want to enable request-based ETW tracing.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
  
## Remarks  
 For more information about the `httpTracing` element, see the following topic on the Microsoft IIS.net Web site: [HTTP Tracing \<httpTracing>](http://www.iis.net/ConfigReference/system.webServer/httpTracing).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<traceUrls>](../../reference/admin/traceurls-element-for-httptracing.md)