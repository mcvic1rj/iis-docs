---
title: "remove Element for modules for system.webServer | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: c2b4e12e-2665-428a-89b9-aa86c73b42e0
caps.latest.revision: 20
author: "shirhatti"
manager: "wpickett"
---
# remove Element for modules for system.webServer
> [!NOTE]
>  For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Modules \<modules>](http://www.iis.net/ConfigReference/system.webServer/modules).  
  
 Specifies a native or managed module to be removed from the `modules` collection.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`name`|Required `string` attribute.<br /><br /> Specifies the unique name of a native or managed module on the Web server.|  
|`preCondition`|Optional `string` attribute.<br /><br /> Specifies conditions under which the module will run.<br /><br /> The `preCondition` attribute can be one or more of the following possible values. If you specify more than one value, separate the values with a comma (,).<br /><br /> `bitness32`:<br /><br /> - Specify the `bitness32` value when the module is a 32-bit .dll file and IIS should load the handler only for worker processes that run in WOW64 mode (32-bit simulation) on a 64-bit operating system.<br /><br /> `bitness64`:<br /><br /> - Specify the `bitness64` value when the module is a 64-bit .dll file and IIS should load the handler only for worker processes that run in 64-bit mode.<br /><br /> `integratedMode`:<br /><br /> - Specify the `integratedMode` value when the module should respond only to requests in application pools that are configured to use the integrated request-processing pipeline.<br /><br /> `ISAPIMode`:<br /><br /> - Specify the `ISAPIMode` value when the module should respond only to requests in application pools that are configured to use **Classic** mode.<br /><br /> `managedHandler`:<br /><br /> - Specify the `managedHandler` value when the module should process requests only for managed resources, such as .aspx files, and should not respond to requests for non-managed resources, such as .html files.<br /><br /> `runtimeVersionv1.1`:<br /><br /> - Specify the `runtimeVersionv1.1` value when the module should respond only to requests in application pools that are configured to use .NET Framework version 1.1.<br /><br /> `runtimeVersionv2.0`:<br /><br /> - Specify the `runtimeVersionv2.0` value when the module should respond only to requests in application pools that are configured to use .NET Framework version 2.0.|  
|`type`|Optional `string` attribute.<br /><br /> Specifies the managed type of a managed module. The `type` attribute does not apply to native modules.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`modules`|Specifies configuration settings for modules on a Web server.|  
  
## Remarks  
 For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Modules \<modules>](http://www.iis.net/ConfigReference/system.webServer/modules).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|