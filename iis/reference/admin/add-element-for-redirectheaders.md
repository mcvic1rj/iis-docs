---
title: "add element for redirectHeaders | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: c80afa6f-4e6f-4fc8-906c-96a3d050aed5
caps.latest.revision: 24
author: "shirhatti"
manager: "wpickett"
---
# add element for redirectHeaders
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Redirect Headers \<add>](http://www.iis.net/ConfigReference/system.webServer/httpProtocol/redirectHeaders/add).  
  
 Adds a response header to the `redirectHeaders` collection.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`name`|Required`string` attribute.<br /><br /> Specifies a field name for the redirect header. In a response, a field name precedes the related field value.|  
|`value`|Optional `string` attribute.<br /><br /> Specifies a field value for the redirect header. In a response, a field value follows the related field name.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`redirectHeaders`|Configures response headers that are returned in responses only when the server redirects requests.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Redirect Headers \<add>](http://www.iis.net/ConfigReference/system.webServer/httpProtocol/redirectHeaders/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|