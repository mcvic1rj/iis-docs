---
title: "clear Element for customHeaders for httpProtocol | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 9b4a8f41-59ea-42f6-b9a2-c6d05ae827f3
caps.latest.revision: 20
author: "shirhatti"
manager: "wpickett"
---
# clear Element for customHeaders for httpProtocol
> [!NOTE]
>  For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [Custom Headers \<customHeaders>](http://www.iis.net/ConfigReference/system.webServer/httpProtocol/customHeaders).  
  
 Clears all references to custom headers in the `customHeaders` collection.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
 None.  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`httpProtocol`|Specifies configuration settings for the HTTP protocol on a Web server.|  
|`customHeaders`|Configures custom response headers that are returned in responses from the Web server.|  
  
## Remarks  
 For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [Custom Headers \<customHeaders>](http://www.iis.net/ConfigReference/system.webServer/httpProtocol/customHeaders).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|