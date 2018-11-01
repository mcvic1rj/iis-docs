---
title: "remove Element for httpRedirect | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 18ca893b-dd58-4daa-b959-6dcbc5bd0d7a
caps.latest.revision: 17
author: "shirhatti"
manager: "wpickett"
---
# remove Element for httpRedirect
> [!NOTE]
>  For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [HTTP Redirects \<httpRedirect>](http://www.iis.net/ConfigReference/system.webServer/httpRedirect).  
  
 Removes a wildcard redirection rule from the collection of redirection rules.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`wildcard`|Required `string` attribute.<br /><br /> Specifies a unique wildcard value to which requests are compared. A request is then redirected to the specified destination if the request matches the wildcard value.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`httpRedirect`|Configures settings for redirecting client requests to a new location.|  
  
## Remarks  
 For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [HTTP Redirects \<httpRedirect>](http://www.iis.net/ConfigReference/system.webServer/httpRedirect).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|