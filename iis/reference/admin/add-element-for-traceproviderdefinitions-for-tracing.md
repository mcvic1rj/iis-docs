---
title: "add Element for traceProviderDefinitions for tracing | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 903b9c41-65dc-44ce-b1aa-7d274905bf3a
caps.latest.revision: 18
author: "shirhatti"
manager: "wpickett"
---
# add Element for traceProviderDefinitions for tracing
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Trace Provider Definitions \<add>](http://www.iis.net/ConfigReference/system.webServer/tracing/traceProviderDefinitions/add).  
  
 Adds a trace provider to the collection of trace providers.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`guid`|Required `string` attribute.<br /><br /> Specifies the GUID of the trace provider. This GUID is used in Event Tracing for Windows (ETW). **Note:**  You can display the value of this attribute by running `logman query providers` at a command prompt.|  
|`name`|Required `string` attribute.<br /><br /> Specifies the name of the trace provider.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`areas`|Required element.<br /><br /> Specifies the functional areas for the provider to trace.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`tracing`|Configures request trace settings.|  
|`traceProviderDefinitions`|Defines the trace providers that are used on the Web server.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Trace Provider Definitions \<add>](http://www.iis.net/ConfigReference/system.webServer/tracing/traceProviderDefinitions/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<remove>](../../reference/admin/remove-element-for-traceproviderdefinitions-for-tracing.md)   
 [\<clear>](../../reference/admin/clear-element-for-traceproviderdefinitions-for-tracing.md)   
 [\<areas>](../../reference/admin/areas-element-for-add-element-for-traceproviderdefinitions-for-tracing.md)