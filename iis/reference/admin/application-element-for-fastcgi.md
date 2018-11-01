---
title: "application Element for fastCgi | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 282e807b-2f6d-4841-acc3-7f133a447963
caps.latest.revision: 20
author: "shirhatti"
manager: "wpickett"
---
# application Element for fastCgi
> [!NOTE]
>  For more information about the `application` element, see the following topic on the Microsoft IIS.net Web site: [FastCGI Application \<application>](http://www.iis.net/ConfigReference/system.webServer/fastCgi/application/environmentVariables/environmentVariable).  
  
 Adds a FastCGI process pool definition to the collection of FastCGI process pool definitions.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`activityTimeout`|Optional `int` attribute.<br /><br /> Specifies the maximum time, in seconds, that a FastCGI process can take to process. Acceptable values are from 10 through 3600.<br /><br /> The default value is 30.|  
|`arguments`|Optional `string` attribute.<br /><br /> Specifies the command-line arguments for the FastCGI process.|  
|`flushNamedPipe`|Optional `Boolean` attribute.<br /><br /> Specifies whether named pipes are flushed at the end of each request. This property applies only when the named-pipe protocol is used.<br /><br /> The default value is `false`.|  
|`fullPath`|Required `string` attribute.<br /><br /> Specifies the full path of the FastCGI process.|  
|`idleTimeout`|Optional `int` attribute.<br /><br /> Specifies the maximum amount of time, in seconds, that a FastCGI process can be idle before the process is shut down. Acceptable values are from 10 through 604800.<br /><br /> The default value is 300.|  
|`instanceMaxRequests`|Optional `int` attribute.<br /><br /> Specifies the maximum number of requests that can be processed by each FastCGI worker process before it is recycled. Acceptable values are from 1 through 10000000.<br /><br /> The default value is 200.|  
|`maxInstances`|Optional `int` attribute.<br /><br /> Specifies the maximum number of FastCGI worker processes that can be started in an application pool. Acceptable values are from 1 through 10000.<br /><br /> The default value is 4.|  
|`protocol`|Optional `enum` attribute.<br /><br /> Specifies the transport mechanism used to communicate with the FastCGI process.<br /><br /> The `protocol` attribute can be one of the following possible values.<br /><br /> The default value is `NamedPipe`.<br /><br /> `NamedPipe`:<br /><br /> - The named-pipe protocol will be used to communicate with the FastCGI worker process.<br /><br /> `Tcp`:<br /><br /> - The TCP protocol will be used to communicate with the FastCGI worker process.|  
|`queueLength`|Optional `int` attribute.<br /><br /> Specifies the maximum number of requests that can be queued for a FastCGI process pool. Acceptable values are from 1 through 10000000.<br /><br /> The default value is 1000.|  
|`requestTimeout`|Optional `int` attribute.<br /><br /> Specifies the maximum time, in seconds, that a FastCGI process request can take. Acceptable values are from 10 through 604800.<br /><br /> The default value is 90.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`environmentVariables`|Optional element.<br /><br /> Specifies a collection of environment variables that IIS will pass to the FastCGI application.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`fastCgi`|Contains a collection of fastCgi application pool definitions.|  
  
## Remarks  
 For more information about the `application` element, see the following topic on the Microsoft IIS.net Web site: [FastCGI Application \<application>](http://www.iis.net/ConfigReference/system.webServer/fastCgi/application/environmentVariables/environmentVariable).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<environmentVariables>](../../reference/admin/environmentvariables-element-for-application-for-fastcgi.md)   
 [\<fastCgi>](../../reference/admin/fastcgi-element.md)   
 [FastCgiApplicationElement Class](../../reference/admin/fastcgiapplicationelement-class.md)   
 [FastCgiSection Class](../../reference/admin/fastcgisection-class.md)