---
title: "fastCgi Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: f7a25acf-0a22-4569-bc41-fae9fa4d86e1
caps.latest.revision: 16
author: "shirhatti"
manager: "wpickett"
---
# fastCgi Element
> [!NOTE]
>  For more information about the `fastCgi` element, see the following topic on the Microsoft IIS.net Web site: [FastCGI \<fastCgi>](http://www.iis.net/ConfigReference/system.webServer/fastCgi).  
  
 Contains a collection of FastCGI process pool definitions.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`application`|Optional element.<br /><br /> Adds a FastCGI process pool definition to the collection of FastCGI process pool definitions.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
  
## Remarks  
 For more information about the `fastCgi` element, see the following topic on the Microsoft IIS.net Web site: [FastCGI \<fastCgi>](http://www.iis.net/ConfigReference/system.webServer/fastCgi).  
  
> [!NOTE]
>  In order to process requests by using FastCGI, you must first map the specific file name extensions and path to the FastCGI module and specify the target FastCGI process as the script processor.  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<application>](../../reference/admin/application-element-for-fastcgi.md)