---
title: "add Element for traceUrls for httpTracing | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 24109edf-3a86-4373-883d-68aacc07c6b6
caps.latest.revision: 18
author: "shirhatti"
manager: "wpickett"
---
# add Element for traceUrls for httpTracing
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Trace URLs \<add>](http://www.iis.net/ConfigReference/system.webServer/httpTracing/traceUrls/add).  
  
 Adds a trace URL to the collection of trace URLs.  
  
## Syntax  
  
```  
<add value="URL" />  
```  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`value`|Required `string` attribute.<br /><br /> Specifies the URL to trace.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`httpTracing`|Specifies configuration settings for request-based Event Tracing for Windows (ETW).|  
|`traceUrls`|Specifies the URL for which you want to enable HTTP tracing for ETW tracing.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Trace URLs \<add>](http://www.iis.net/ConfigReference/system.webServer/httpTracing/traceUrls/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<remove>](../../reference/admin/remove-element-for-traceurls-for-httptracing.md)   
 [\<clear>](../../reference/admin/clear-element-for-traceurls-for-httptracing.md)