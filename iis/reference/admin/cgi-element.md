---
title: "cgi Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 89b8445e-9299-4448-bdd7-acb48803fd19
caps.latest.revision: 20
author: "shirhatti"
manager: "wpickett"
---
# cgi Element
> [!NOTE]
>  For more information about the `cgi` element, see the following topic on the Microsoft IIS.net Web site: [CGI \<cgi>](http://www.iis.net/ConfigReference/system.webServer/cgi).  
  
 Configures default settings for Common Gateway Interface (CGI) applications.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`createCGIWithNewConsole`|Optional `Boolean` attribute.<br /><br /> Specifies whether a CGI application runs in its own console. **Note:**  If the value is set to `true`, each CGI application creates a new console when the application is started. A value of `false` indicates that CGI applications should run without a console. <br /><br /> The default value is `false`.|  
|`createProcessAsUser`|Optional `Boolean` attribute.<br /><br /> Specifies whether a CGI process is created in the system context or in the context of the requesting user.<br /><br /> The default value is `true`.|  
|`timeout`|Optional `timeSpan` attribute.<br /><br /> Specifies the time-out for a CGI application.<br /><br /> The default value is 00:15:00 (15 minutes).|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
  
## Remarks  
 For more information about the `cgi` element, see the following topic on the Microsoft IIS.net Web site: [CGI \<cgi>](http://www.iis.net/ConfigReference/system.webServer/cgi).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<application>](../../reference/admin/application-element-for-fastcgi.md)   
 [\<fastCgi>](../../reference/admin/fastcgi-element.md)   
 [\<isapiCgiRestriction>](../../reference/admin/isapicgirestriction-element.md)