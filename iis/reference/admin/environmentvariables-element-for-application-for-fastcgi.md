---
title: "environmentVariables Element for application for fastCgi | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 21dee112-23ae-4c77-984e-ecabe8099e18
caps.latest.revision: 5
author: "shirhatti"
manager: "wpickett"
---
# environmentVariables Element for application for fastCgi
> [!NOTE]
>  For more information about the `environmentVariables` element, see the following topic on the Microsoft IIS.net Web site: [Environment Variables \<environmentVariables>](http://www.iis.net/ConfigReference/system.webServer/fastCgi/application/environmentVariables).  
  
 Specifies a list of environment variables that Internet Information Services (IIS) 7 will pass to a FastCGI process when it is launched.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`environmentVariable`|Optional element.<br /><br /> Adds an environment variable to the collection of environment variables.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`fastCgi`|Contains a collection of fastCgi application pool definitions.|  
|`application`|Adds a FastCGI process pool definition to the collection of FastCGI process pool definitions.|  
  
## Remarks  
 For more information about the `environmentVariables` element, see the following topic on the Microsoft IIS.net Web site: [Environment Variables \<environmentVariables>](http://www.iis.net/ConfigReference/system.webServer/fastCgi/application/environmentVariables).  
  
## Element Information  
  
|||  
|-|-|  
|`Configuration locations`|ApplicationHost.config|  
|`Requirements`|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<environmentVariable>](../../reference/admin/environmentvariable-element-for-environmentvariables-for-application.md)