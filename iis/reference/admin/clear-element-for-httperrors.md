---
title: "clear Element for httpErrors | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 59b05e9f-6bee-4a24-b804-a1b962d20ab0
caps.latest.revision: 12
author: "shirhatti"
manager: "wpickett"
---
# clear Element for httpErrors
> [!NOTE]
>  For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [HTTP Errors \<httpErrors>](http://www.iis.net/ConfigReference/system.webServer/httpErrors).  
  
 Removes all references to HTTP errors from the HTTP error collection.  
  
## Syntax  
  
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
|`httpErrors`|Configures HTTP error messages for a Web server.|  
  
## Remarks  
 For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [HTTP Errors \<httpErrors>](http://www.iis.net/ConfigReference/system.webServer/httpErrors).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [IIS 7.0 Beta: error Element for httpErrors (IIS Settings Schema)](http://msdn.microsoft.com/en-us/2d5fd268-4845-4da6-98a9-594ed7d79dc5)   
 [\<remove>](../../reference/admin/remove-element-for-httperrors.md)