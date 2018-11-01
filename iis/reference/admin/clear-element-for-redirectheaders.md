---
title: "clear Element for redirectHeaders | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 59f8e36e-febd-413d-96ff-ed45755d6a0a
caps.latest.revision: 17
author: "shirhatti"
manager: "wpickett"
---
# clear Element for redirectHeaders
> [!NOTE]
>  For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [Redirect Headers \<redirectHeaders>](http://www.iis.net/ConfigReference/system.webServer/httpProtocol/redirectHeaders).  
  
 Clears inherited settings for response headers in the `redirectHeaders` collection.  
  
## Syntax  
  
```  
<clear />  
```  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`redirectHeaders`|Configures response headers that are returned in responses only when the server redirects requests.|  
  
## Remarks  
 For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [Redirect Headers \<redirectHeaders>](http://www.iis.net/ConfigReference/system.webServer/httpProtocol/redirectHeaders).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|