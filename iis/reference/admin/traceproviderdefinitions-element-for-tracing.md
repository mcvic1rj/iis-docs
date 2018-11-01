---
title: "traceProviderDefinitions Element for tracing | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: e131a9b0-5a89-4cc6-8589-3f1f6fbfdf65
caps.latest.revision: 15
author: "shirhatti"
manager: "wpickett"
---
# traceProviderDefinitions Element for tracing
> [!NOTE]
>  For more information about the `traceProviderDefinitions` element, see the following topic on the Microsoft IIS.net Web site: [Trace Provider Definitions \<traceProviderDefinitions>](http://www.iis.net/ConfigReference/system.webServer/tracing/traceProviderDefinitions).  
  
 Defines the trace providers that are available for use on the Web server.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a trace provider to the collection of trace providers.|  
|`remove`|Optional element.<br /><br /> Removes a reference to a trace provider from the trace provider collection.|  
|`clear`|Optional element.<br /><br /> Removes all references to trace providers from the trace provider collection.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`tracing`|Configures request trace settings.|  
  
## Remarks  
 For more information about the `traceProviderDefinitions` element, see the following topic on the Microsoft IIS.net Web site: [Trace Provider Definitions \<traceProviderDefinitions>](http://www.iis.net/ConfigReference/system.webServer/tracing/traceProviderDefinitions).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-traceproviderdefinitions-for-tracing.md)   
 [\<remove>](../../reference/admin/remove-element-for-traceproviderdefinitions-for-tracing.md)   
 [\<clear>](../../reference/admin/clear-element-for-traceproviderdefinitions-for-tracing.md)