---
title: "comPlus Element for asp | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: b8d332dc-6f08-424c-ae74-a634ba0de8d4
caps.latest.revision: 29
author: "shirhatti"
manager: "wpickett"
---
# comPlus Element for asp
> [!NOTE]
>  For more information about the `comPlus` element, see the following topic on the Microsoft IIS.net Web site: [ASP COM Plus \<comPlus>](http://www.iis.net/ConfigReference/system.webServer/asp/comPlus).  
  
 Configures COM+ settings.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`appServiceFlags`|Optional `enum` attribute.<br /><br /> Contains the flags that must be set to enable COM+ services on your IIS applications.<br /><br /> The `appServiceFlags` attribute can be one of the following possible values. The default is `None`.<br /><br /> `None`: Specifies that no flags are set. The numeric value is 0.<br /><br /> `EnableTracker`: A value of `true` enables COM+ tracker, which allows administrators or developers to debug ASP applications. The numeric value is 1.<br /><br /> `EnableSxS`: A value of `true` enables COM+ side-by-side assemblies, which allow ASP applications to specify which version of a system DLL or classic COM component to use, such as WinHTTP 5.1, Shell Common Controls version 6.0 (Comctl32.dll), GDI Plus version 1.0 (GDIplus.dll), and Visual C++ Run-time Libraries version 6.0. If this value is set to `true`, you must also specify a value for the `sxsName` attribute.  The numeric value is 2.<br /><br /> `UsePartition`: A value of `true` enables COM+ partitioning, which can be used to isolate Web applications into their own COM+ partitions. COM+ partitions can hold different versions of your own custom COM components.  If this value is set to `true`, you must also specify a value for the `partitionId` attribute. The numeric value is 4.|  
|`executeInMta`|Optional `Boolean` attribute.<br /><br /> Specifies whether ASP runs in a multithreaded environment.<br /><br /> The default value is `false`.|  
|`partitionId`|Optional `string` attribute.<br /><br /> Specifies the Globally Unique Identifier (GUID) of the COM+ partition.<br /><br /> Note:<br /><br /> This attribute is required when the `appServiceFlags` attribute is set to `UsePartition`<br /><br /> The default value is "00000000-0000-0000-0000-000000000000".|  
|`sxsName`|Optional `string` attribute.<br /><br /> Note:<br /><br /> This property is required when the `appServiceFlags` attribute is set to `EnableSxS`.<br /><br /> Specifies the name of the COM+ application.|  
|`trackThreadingModel`|Optional `Boolean` attribute.<br /><br /> Specifies whether thread model checking is enabled. A value of `true` means that IIS honors the threading model of the components that an application creates.<br /><br /> The default value is `false`.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`asp`|Configures settings for ASP applications.|  
  
## Remarks  
 For more information about the `comPlus` element, see the following topic on the Microsoft IIS.net Web site: [ASP COM Plus \<comPlus>](http://www.iis.net/ConfigReference/system.webServer/asp/comPlus).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<cache>](../../reference/admin/cache-element-for-asp.md)   
 [\<limits>](../../reference/admin/limits-element-for-asp.md)   
 [\<session>](../../reference/admin/session-element-for-asp.md)