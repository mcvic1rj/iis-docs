---
title: "redirectHeaders Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 7e38b58c-6933-4e1c-ad55-68b7b810cc8d
caps.latest.revision: 20
author: "shirhatti"
manager: "wpickett"
---
# redirectHeaders Element
> [!NOTE]
>  For more information about the `redirectHeaders` element, see the following topic on the Microsoft IIS.net Web site: [Redirect Headers \<redirectHeaders>](http://www.iis.net/ConfigReference/system.webServer/httpProtocol/redirectHeaders).  
  
 Configures response headers that are returned in responses only when the server redirects requests.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a response header to the redirectHeaders collection.|  
|`clear`|Optional element.<br /><br /> Removes all references to response headers from the redirectHeaders collection.|  
|`remove`|Optional element.<br /><br /> Removes a reference to a response header from the redirectHeaders collection.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
  
## Remarks  
 For more information about the `redirectHeaders` element, see the following topic on the Microsoft IIS.net Web site: [Redirect Headers \<redirectHeaders>](http://www.iis.net/ConfigReference/system.webServer/httpProtocol/redirectHeaders).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-redirectheaders.md)   
 [\<remove>](../../reference/admin/remove-element-for-redirectheaders.md)   
 [\<clear>](../../reference/admin/clear-element-for-redirectheaders.md)