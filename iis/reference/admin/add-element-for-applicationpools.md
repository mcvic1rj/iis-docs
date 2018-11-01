---
title: "add Element for applicationPools | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: efc4a211-8f4f-450c-8c5a-f19d0792dd07
caps.latest.revision: 26
author: "shirhatti"
manager: "wpickett"
---
# add Element for applicationPools
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Application Pools \<add>](http://www.iis.net/ConfigReference/system.applicationHost/applicationPools/add).  
  
 Configures an application pool in the server configuration.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`autoStart`|Optional `Boolean` attribute.<br /><br /> When `true`, indicates to the World Wide Web Publishing Service (W3SVC) that the application pool should be automatically started when it is created or when IIS is started.<br /><br /> The default value is `true`.|  
|`CLRConfigFile`|Optional string value.Specifies the .NET configuration file for the application pool.Note: This attribute was added in IIS 7.5.There is no default value.|  
|`enable32BitAppOnWin64`|Optional `Boolean` attribute.<br /><br /> When `true`, enables a 32-bit application to run on a computer that runs a 64-bit version of Windows.<br /><br /> The default value is `false`.|  
|`enableConfigurationOverride`|Optional Boolean attribute.When true, indicates that delegated settings in Web.config files will processed for applications within this application pool. When false, all settings in Web.config files will be ignored for this application pool.The default value is true.|  
|`managedPipelineMode`|Optional `enum` attribute.<br /><br /> Specifies the request-processing mode that is used to process requests for managed content.<br /><br /> The `managedPipelineMode` attribute can be one of the following possible values. The default is `Integrated`.<br /><br /> -   `Classic:`<br />     - Specifies that the application pool use separate IIS and ASP.NET request-processing pipelines, which works with ASP.NET 1.1 applications, and ASP.NET 2.0 applications that do not work in `Integrated` mode.<br />     - The numeric value is 1.<br /><br /> -   `Integrated:`<br />     - Specifies that the application pool use the integrated IIS and ASP.NET request-processing pipeline, which works with only ASP.NET 2.0 applications.<br />     - The numeric value is 0.|  
|`managedRuntimeVersion`|Optional `string` attribute.<br /><br /> Specifies the .NET Framework version to be used by the application pool.<br /><br /> The `managedRuntimeVersion` attribute can be one of the following possible values. The default value is `v2.0`.<br /><br /> -   `v1.1:`<br />     - Specifies that the application pool use the .NET Framework version 1.1.<br /><br /> -   `v2.0:`<br />     - Specifies that the application pool use the .NET Framework version 2.0.|  
|`name`|Required `string` attribute.<br /><br /> Specifies a unique name for an application pool on the server.|  
|`passAnonymousToken`|Optional Boolean attribute.If true, the Windows Process Activation Service (WAS) creates and passes a token for the built-in IUSR anonymous user account to the Anonymous authentication module. The Anonymous authentication module uses the token to impersonate the built-in account. When PassAnonymousToken is false, the token will not be passed.Note: The IUSR anonymous user account replaces the IIS_MachineName anonymous account. The IUSR account can be used by IIS or other applications. It does not have any privileges assigned to it during setup.The default value is true.|  
|`queueLength`|Optional `uint` attribute.<br /><br /> Indicates to HTTP.sys how many requests to queue for an application pool before rejecting future requests. The default value is 1000.<br /><br /> When the value set for this property is exceeded, IIS rejects subsequent requests with a 503 error. If the `loadBalancerCapabilities` setting is `true`, the connection is closed instead of rejecting requests with a 503.|  
|`startMode`|Optional enum value.Specifies the startup type for the application pool.Note: This attribute was added in IIS 7.5.The startMode attribute can be one of the following possible values.<br /><br /> -   **AlwaysRunning:**<br />     - Specifies that the Windows Process Activation Service (WAS) will always start the application pool. This behavior allows an application to load the operating environment before any serving any HTTP requests, which reduces the start-up processing for initial HTTP requests for the application.The numeric value is 1.<br /><br /> -   **OnDemand:**<br />     - Specifies that the Windows Process Activation Service (WAS) will start the application pool when an HTTP request is made for an application that is hosted in the application pool. This behavior resembles the WAS behavior in previous versions of IIS.The numeric value is 0.|  
  
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
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Application Pools \<add>](http://www.iis.net/ConfigReference/system.applicationHost/applicationPools/add).  
  
 The `applicationPools` element can be declared in ApplicationHost.config only. Any attempt to declare `applicationPools` in a configuration file at a different level in the hierarchy results in an error message.  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
|**IIS 7.5**|The \<add> element of the \<applicationPools> element was updated in IIS 7.5 to include attributes that allow you to preload applications.|  
  
## See Also  
 [\<cpu>](../../reference/admin/cpu-element-for-add-for-applicationpools.md)   
 [\<failure>](../../reference/admin/failure-element-for-add-for-applicationpools.md)   
 [\<processModel>](../../reference/admin/processmodel-element-for-add-for-applicationpools.md)   
 [\<recycling>](../../reference/admin/recycling-element-for-add-for-applicationpools.md)   
 [\<applicationPoolDefaults>](../../reference/admin/applicationpooldefaults-element-for-applicationpools.md)