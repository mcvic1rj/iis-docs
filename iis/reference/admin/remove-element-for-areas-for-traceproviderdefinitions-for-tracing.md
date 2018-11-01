---
title: "remove Element for areas for traceProviderDefinitions for tracing | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: e4c82904-b913-4e15-87df-6d57056fbe88
caps.latest.revision: 12
author: "shirhatti"
manager: "wpickett"
---
# remove Element for areas for traceProviderDefinitions for tracing
> [!NOTE]
>  For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Areas \<areas>](http://www.iis.net/ConfigReference/system.webServer/tracing/traceProviderDefinitions/add/areas).  
  
 Removes a reference to a functional area from the functional areas to trace collection.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`name`|Required `string` attribute.<br /><br /> Specifies the name of the functional area for the trace provider to trace.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`tracing`|Configures request trace settings.|  
|`traceProviderDefinitions`|Defines the trace providers that are used on the Web server.|  
|`add`|Adds a trace provider to the collection of trace providers.|  
|`areas`|Specifies the functional areas for the provider to trace.|  
  
## Remarks  
 For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Areas \<areas>](http://www.iis.net/ConfigReference/system.webServer/tracing/traceProviderDefinitions/add/areas).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-areas-for-traceproviderdefinitions-for-tracing.md)   
 [\<clear>](../../reference/admin/clear-element-for-areas-for-traceproviderdefinitions-for-tracing.md)