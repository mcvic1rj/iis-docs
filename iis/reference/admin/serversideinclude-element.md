---
title: "serverSideInclude Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 9a6400ec-abd9-4d55-808d-4fd7e4632245
caps.latest.revision: 13
author: "shirhatti"
manager: "wpickett"
---
# serverSideInclude Element
> [!NOTE]
>  For more information about the `serverSideInclude` element, see the following topic on the Microsoft IIS.net Web site: [Server Side Include \<serverSideInclude>](http://www.iis.net/ConfigReference/system.webServer/serverSideInclude).  
  
 Specifies whether server-side includes (SSI) `#exec` directives are disabled.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`ssiExecDisable`|Optional `Boolean` attribute.<br /><br /> Specifies whether the SSI `#exec` directive is enabled (`false`) or disabled (`true`). When disabled, the directive cannot execute a program, script, or shell command on the server.<br /><br /> The default value is `false`.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
  
## Remarks  
 For more information about the `serverSideInclude` element, see the following topic on the Microsoft IIS.net Web site: [Server Side Include \<serverSideInclude>](http://www.iis.net/ConfigReference/system.webServer/serverSideInclude).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|