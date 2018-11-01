---
title: "httpLogging Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: d03966d9-7217-49b0-9978-282dd9986e4b
caps.latest.revision: 23
author: "shirhatti"
manager: "wpickett"
---
# httpLogging Element
> [!NOTE]
>  For more information about the `httpLogging` element, see the following topic on the Microsoft IIS.net Web site: [HTTP Logging \<httpLogging>](http://www.iis.net/ConfigReference/system.webServer/httpLogging).  
  
 Specifies configuration settings for HTTP.sys logging.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`dontLog`|Optional `Boolean` attribute.<br /><br /> Specifies whether HTTP logging is enabled for successful requests. A request is considered successful if its status code is less than 400.<br /><br /> The default value is `false`.|  
|`selectiveLogging`|Optional `enum` attribute.<br /><br /> Specifies which type of requests to log.<br /><br /> The `selectiveLogging` attribute can be one of the following possible values.<br /><br /> The default value is `LogAll`.<br /><br /> `LogAll`:<br /><br /> - Logs all requests. The numeric value is 0.<br /><br /> `LogSuccessful`:<br /><br /> - Logs only successful requests. The HTTP status code range for successful requests is 100-399. The numeric value is 1.<br /><br /> `LogError`:<br /><br /> - Logs only unsuccessful requests. The HTTP status code range for unsuccessful requests is 400-999. The numeric value is 2.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
  
## Remarks  
 For more information about the `httpLogging` element, see the following topic on the Microsoft IIS.net Web site: [HTTP Logging \<httpLogging>](http://www.iis.net/ConfigReference/system.webServer/httpLogging).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [HttpLoggingSection Class](../../reference/admin/httploggingsection-class1.md)