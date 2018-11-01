---
title: "remove Element for httpErrors | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: d3d88cc7-fdcf-4eb1-bb64-10a1955a95f6
caps.latest.revision: 14
author: "shirhatti"
manager: "wpickett"
---
# remove Element for httpErrors
> [!NOTE]
>  For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [HTTP Errors \<httpErrors>](http://www.iis.net/ConfigReference/system.webServer/httpErrors).  
  
 Removes a reference to an HTTP error from the HTTP error collection.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`statusCode`|Required `integer` attribute.<br /><br /> Specifies the number of the HTTP status code for which you want to create a custom error message.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`httpErrors`|Configures HTTP error messages for a Web server.|  
  
## Remarks  
 For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [HTTP Errors \<httpErrors>](http://www.iis.net/ConfigReference/system.webServer/httpErrors).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [IIS 7.0 Beta: error Element for httpErrors (IIS Settings Schema)](http://msdn.microsoft.com/en-us/2d5fd268-4845-4da6-98a9-594ed7d79dc5)   
 [\<clear>](../../reference/admin/clear-element-for-httperrors.md)