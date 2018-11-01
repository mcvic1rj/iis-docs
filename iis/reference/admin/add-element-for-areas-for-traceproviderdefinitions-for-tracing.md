---
title: "add Element for areas for traceProviderDefinitions for tracing | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: a2429d25-fe0f-49f1-85b2-eeb709c94a5c
caps.latest.revision: 15
author: "shirhatti"
manager: "wpickett"
---
# add Element for areas for traceProviderDefinitions for tracing
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Areas \<add>](http://www.iis.net/ConfigReference/system.webServer/tracing/traceProviderDefinitions/add/areas/add).  
  
 Adds a functional area to the collection of functional areas to trace.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`name`|Required `string` attribute.<br /><br /> Specifies the name of the functional area for the trace provider to trace.|  
|`value`|Required `int` attribute.<br /><br /> Specifies the value of the functional area for the trace provider to trace. For the "WWW Server", "ASP", "ISAPI Extension", and "ASPNET" providers, this value maps to the corresponding flag values in ETW Tracing.  Values increase in multiples of 2.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`tracing`|Configures request trace settings|  
|`traceProviderDefinitions`|Defines the trace providers that are used on the Web server.|  
|`add`|Adds a trace provider to the collection of trace providers.|  
|`areas`|Specifies the functional areas for the provider to trace.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Areas \<add>](http://www.iis.net/ConfigReference/system.webServer/tracing/traceProviderDefinitions/add/areas/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<remove>](../../reference/admin/remove-element-for-areas-for-traceproviderdefinitions-for-tracing.md)   
 [\<clear>](../../reference/admin/clear-element-for-areas-for-traceproviderdefinitions-for-tracing.md)