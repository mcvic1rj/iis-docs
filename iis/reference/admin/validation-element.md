---
title: "validation Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: dde5c19f-e3f2-4488-84a7-151b927408d8
caps.latest.revision: 18
author: "shirhatti"
manager: "wpickett"
---
# validation Element
> [!NOTE]
>  For more information about the `validation` element, see the following topic on the Microsoft IIS.net Web site: [Validation \<validation>](http://www.iis.net/ConfigReference/system.webServer/validation).  
  
 Configures [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)] to detect whether an ASP.NET application that is set up to run in ISAPI mode needs to be changed in order to function correctly in Integrated mode.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`validateIntegratedModeConfiguration`|Optional `Boolean` attribute.<br /><br /> Specifies whether configuration validation is enabled when it runs in Integrated mode. The `<system.Web/httpHandlers>` and `<system.Web/httpModules>` sections as well as impersonation are checked during this process. For more information, see the Remarks section.<br /><br /> The default value is `true`.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
  
## Remarks  
 For more information about the `validation` element, see the following topic on the Microsoft IIS.net Web site: [Validation \<validation>](http://www.iis.net/ConfigReference/system.webServer/validation).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [ValidationSection Class](../../reference/admin/validationsection-class.md)