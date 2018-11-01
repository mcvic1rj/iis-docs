---
title: "add Element for globalModules | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 507a579d-7bde-4c78-94ef-a0c819a82543
caps.latest.revision: 23
author: "shirhatti"
manager: "wpickett"
---
# add Element for globalModules
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Global Modules \<add>](http://www.iis.net/ConfigReference/system.webServer/globalModules/add).  
  
 Specifies a global module to be added to the Web server.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`image`|Required `string` attribute.<br /><br /> Specifies the physical path of the .dll file for the global module. The attribute value will be expanded when environment variables, such as %windir%, are used.|  
|`name`|Required `string` attribute.<br /><br /> Specifies the name of the global module.|  
|`preCondition`|Optional `string` attribute.<br /><br /> Specifies conditions under which the global module will run.<br /><br /> The `preCondition` attribute can be one or more of the following possible values. If you specify more than one value, separate the values with a comma (,).<br /><br /> -   `bitness32:`<br />     - Specify the `bitness32` value when the global module is a 32-bit .dll file, and IIS should load the global module only for worker processes that run in WOW64 mode (32-bit simulation) on a 64-bit operating system.<br /><br /> -   `bitness64:`<br />     - Specify the `bitness64` value when the global module is a 64-bit .dll file, and IIS should load the global module only for worker processes that run in 64-bit mode.<br /><br /> -   `integratedMode:`<br />     - Specify the `integratedMode` value when the global module should use the integrated request-processing pipeline to process requests for managed content.<br /><br /> -   `ISAPIMode:`<br />     - Specify the `ISAPIMode` value when the global module should use the ASP.NET ISAPI extension, aspnet_isapi.dll, to process requests for managed content.<br /><br /> -   `runtimeVersionv1.1:`<br />     - Specify the `runtimeVersionv1.1` value when the global module should load only for application pools that are configured to use .NET Framework version 1.1.<br /><br /> -   `runtimeVersionv2.0:`<br />     - Specify the `runtimeVersionv2.0` value when the global module should load only for application pools that are configured to use .NET Framework version 2.0.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the root element in ApplicationHost.config that is the top-level section group in which this element is defined.|  
|`globalModules`|Specifies configuration settings for global modules on a Web server.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Global Modules \<add>](http://www.iis.net/ConfigReference/system.webServer/globalModules/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|