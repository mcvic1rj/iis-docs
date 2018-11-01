---
title: "applicationPoolDefaults Element for applicationPools | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 26205684-1822-4673-8944-865af86a3fa3
caps.latest.revision: 32
author: "shirhatti"
manager: "wpickett"
---
# applicationPoolDefaults Element for applicationPools
> [!NOTE]
>  For more information about the `applicationPoolDefaults` element, see the following topic on the Microsoft IIS.net Web site: [Application Pool Defaults \<applicationPoolDefaults>](http://www.iis.net/ConfigReference/system.applicationHost/applicationPools/applicationPoolDefaults).  
  
 Configures default values for all application pools on a Web server. Individual application pool settings can override these defaults.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`autoStart`|Optional `Boolean` attribute.<br /><br /> When `true`, indicates to the World Wide Web Publishing Service (W3SVC) that the application pool should be automatically started when it is created or when IIS is started.<br /><br /> The default value is `true`.|  
|`CLRConfigFile`|Optional string value.Specifies the .NET configuration file for the application pool.Note: This attribute was added in IIS 7.5.There is no default value.|  
|`enable32BitAppOnWin64`|Optional `Boolean` attribute.<br /><br /> When `true`, enables a 32-bit application to run on a computer that runs a 64-bit version of Windows.<br /><br /> The default value is `false`.|  
|`managedPipelineMode`|Optional `enum` attribute.<br /><br /> Specifies the request-processing mode that is used to process requests for managed content.<br /><br /> The `managedPipelineMode` attribute can be one of the following possible values. The default is `Integrated`.<br /><br /> `Classic`<br /><br /> - Specifies that the application pool use separate IIS and ASP.NET request-processing pipelines, which works with ASP.NET 1.1 applications, and ASP.NET 2.0 applications that do not work in `Integrated` mode.<br /><br /> - The numeric value is 1.<br /><br /> `Integrated`<br /><br /> - Specifies that the application pool use the integrated IIS and ASP.NET request-processing pipeline, which works with only ASP.NET 2.0 applications.<br /><br /> - The numeric value is 0.|  
|`ManagedRuntimeLoader`|Optional string attribute.Specifies the managed loader to use for pre-loading the the application pool.Note: This attribute was added in IIS 7.5.The default value is webengine4.dll.|  
|`managedRuntimeVersion`|Optional `string` attribute.<br /><br /> Specifies the .NET Framework version that is used by the application pool.<br /><br /> The `managedRuntimeVersion` attribute can be one of the following values. The default is `v2.0`.<br /><br /> `v1.1`<br /><br /> - Specifies that the application pool uses .NET Framework version 1.1.<br /><br /> `v2.0`<br /><br /> - Specifies that the application pool uses .NET Framework version 2.0.|  
|`name`|Required `string` attribute.<br /><br /> Specifies the default name for application pools on the server.|  
|`queueLength`|Optional `uint` attribute.<br /><br /> Indicates to HTTP.sys how many requests to queue for an application pool before rejecting future requests. The default value is 1000.<br /><br /> When the value set for this property is exceeded, IIS rejects subsequent requests with a 503 error. If the `loadBalancerCapabilities` setting is `true`, the connection is closed instead of rejecting requests with a 503.|  
|`startMode`|Optional enum value.Specifies the startup type for the application pool.Note: This attribute was added in IIS 7.5.The startMode attribute can be one of the following possible values; the default value is OnDemand.<br /><br /> `AlwaysRunning`<br /><br /> - Specifies that the Windows Process Activation Service (WAS) will always start the application pool. This behavior allows an application to load the operating environment before any serving any HTTP requests, which reduces the start-up processing for initial HTTP requests for the application.The numeric value is 1.<br /><br /> `OnDemand`<br /><br /> - Specifies that the Windows Process Activation Service (WAS) will start the application pool when an HTTP request is made for an application that is hosted in the application pool. This behavior resembles the WAS behavior in previous versions of IIS.The numeric value is 0.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`cpu`|Configures CPU affinity and CPU actions.|  
|`failure`|Configures actions to take when an application pool fails.|  
|`processModel`|Configures process management attributes for an application pool.|  
|`recycling`|Configures application pool recycling.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`applicationPools`|Specifies configuration settings for all application pools.|  
  
## Remarks  
 For more information about the `applicationPoolDefaults` element, see the following topic on the Microsoft IIS.net Web site: [Application Pool Defaults \<applicationPoolDefaults>](http://www.iis.net/ConfigReference/system.applicationHost/applicationPools/applicationPoolDefaults).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<cpu>](../../reference/admin/cpu-element-for-applicationpooldefaults-for-applicationpools.md)   
 [\<failure>](../../reference/admin/failure-element-for-applicationpooldefaults-for-applicationpools.md)   
 [\<processModel>](../../reference/admin/processmodel-element-for-applicationpooldefaults-for-applicationpools.md)   
 [\<recycling>](../../reference/admin/recycling-element-for-applicationpooldefaults-for-applicationpools.md)   
 [\<add>](../../reference/admin/add-element-for-applicationpools.md)