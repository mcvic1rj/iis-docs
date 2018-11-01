---
title: "filter Element for isapiFilters | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 8241bb22-9613-4836-9d0a-72419fb1a1d6
caps.latest.revision: 24
author: "shirhatti"
manager: "wpickett"
---
# filter Element for isapiFilters
> [!NOTE]
>  For more information about the `filter` element, see the following topic on the Microsoft IIS.net Web site: [Filter \<filter>](http://www.iis.net/ConfigReference/system.webServer/isapiFilters/filter).  
  
 Configures an ISAPI filter to process client request data or server response data.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attributes|Description|  
|----------------|-----------------|  
|`enableCache`|Optional `Boolean` attribute.<br /><br /> Specifies whether HTTP.sys caching is enabled (`true`) or disabled (`false`) for filtered server responses.<br /><br /> The default `value` is false.|  
|`enabled`|Optional `Boolean` attribute.<br /><br /> Specifies whether the installed filter is enabled (`true`) or disabled (`false`).<br /><br /> The default value is `true`.|  
|`name`|Required `string` attribute.<br /><br /> Specifies the unique name of the ISAPI filter.|  
|`path`|Required `string` attribute.<br /><br /> Specifies the full physical path of the ISAPI filter .dll file.|  
|`preCondition`|Optional `string` attribute.<br /><br /> Specifies conditions under which the ISAPI filter will run.<br /><br /> The `preCondition` attribute can be one or more of the following possible values. If you specify more than one value, separate the values with a comma (,).<br /><br /> `bitness32`:<br /><br /> - Specify the `bitness32` value when the ISAPI filter is a 32-bit .dll file and IIS should load the filter only for worker processes that run in WOW64 mode (32-bit simulation) on a 64-bit operating system.<br /><br /> `bitness64`:<br /><br /> - Specify the `bitness64` value when the ISAPI filter is a 64-bit .dll file and IIS should load the filter only for worker processes that run in 64-bit mode.<br /><br /> `integratedMode`:<br /><br /> - Specify the `integratedMode` value when the ISAPI filter should use the integrated request-processing pipeline to process requests for managed content.<br /><br /> `ISAPIMode`:<br /><br /> - Specify the `ISAPIMode` value when the ISAPI filter should use the ASP.NET ISAPI extension, aspnet_isapi.dll, to process requests for managed content.<br /><br /> `runtimeVersionv1.1`:<br /><br /> - Specify the `runtimeVersionv1.1` value when the ISAPI filter should load only for application pools that are configured to use .NET Framework version 1.1.<br /><br /> `runtimeVersionv2.0`:<br /><br /> - Specify the `runtimeVersionv2.0` value when the ISAPI filter should load only for application pools that are configured to use .NET Framework version 2.0.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`isapiFilters`|Specifies configuration settings for ISAPI filters on a Web server.|  
  
## Remarks  
 For more information about the `filter` element, see the following topic on the Microsoft IIS.net Web site: [Filter \<filter>](http://www.iis.net/ConfigReference/system.webServer/isapiFilters/filter).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<isapiFilters>](../../reference/admin/isapifilters-element.md)