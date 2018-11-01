---
title: "environmentVariable Element for environmentVariables for application | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 7e1135a6-fe1c-4392-be40-46027327dd14
caps.latest.revision: 5
author: "shirhatti"
manager: "wpickett"
---
# environmentVariable Element for environmentVariables for application
> [!NOTE]
>  For more information about the `environmentVariable` element, see the following topic on the Microsoft IIS.net Web site: [Environment Variable \<environmentVariable>](http://www.iis.net/ConfigReference/system.webServer/fastCgi/application/environmentVariables/environmentVariable).  
  
 Adds a unique name/value pair of an environment variable that Internet Information Services (IIS) 7 will pass to a FastCGI process when it is launched.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`name`|Optional `string` attribute.<br /><br /> Specifies the name of the environment variable to pass to the FastCGI process.|  
|`Value`|Optional `string` attribute.<br /><br /> Specifies the value of the environment variable to pass to the FastCGI process.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`fastCgi`|Contains a collection of fastCgi application pool definitions.|  
|`application`|Adds a FastCGI process pool definition to the collection of FastCGI process pool definitions.|  
|`environmentVariable`|Specifies a collection of environment variables that IIS will pass to the FastCGI application.|  
  
## Remarks  
 For more information about the `environmentVariable` element, see the following topic on the Microsoft IIS.net Web site: [Environment Variable \<environmentVariable>](http://www.iis.net/ConfigReference/system.webServer/fastCgi/application/environmentVariables/environmentVariable).  
  
## Element Information  
  
|||  
|-|-|  
|`Configuration locations`|ApplicationHost.config|  
|`Requirements`|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<environmentVariables>](../../reference/admin/environmentvariables-element-for-application-for-fastcgi.md)