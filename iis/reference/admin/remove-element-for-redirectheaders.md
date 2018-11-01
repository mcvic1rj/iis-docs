---
title: "remove Element for redirectHeaders | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 7f0d6ec2-0316-47d6-9631-66f79bef9687
caps.latest.revision: 24
author: "shirhatti"
manager: "wpickett"
---
# remove Element for redirectHeaders
> [!NOTE]
>  For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Redirect Headers \<redirectHeaders>](http://www.iis.net/ConfigReference/system.webServer/httpProtocol/redirectHeaders).  
  
 Removes a response header from the `redirectHeaders` collection. Headers that are removed from the `redirectHeaders` collection are not returned in responses when the server redirects requests.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`name`|Required`string` attribute.<br /><br /> Specifies a field name for the response header. In a response, a field name comes before the related field value.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`redirectHeaders`|Configures response headers that are returned in responses. These responses are returned only when the server redirects requests.|  
  
## Remarks  
 For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Redirect Headers \<redirectHeaders>](http://www.iis.net/ConfigReference/system.webServer/httpProtocol/redirectHeaders).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|