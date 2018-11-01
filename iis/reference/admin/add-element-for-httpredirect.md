---
title: "add Element for httpRedirect | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: f7a35ff3-575a-44df-a852-aaeec527f58c
caps.latest.revision: 16
author: "shirhatti"
manager: "wpickett"
---
# add Element for httpRedirect
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding HTTP Wildcard Redirects \<add>](http://www.iis.net/ConfigReference/system.webServer/httpRedirect/add).  
  
 Adds a wildcard redirection rule to the collection of redirection rules.  
  
> [!NOTE]
>  If you add wildcard redirection rules, you must remove the default destination value in the `httpRedirect` section in order for the wildcard rules to work.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`destination`|Required `string` attribute.<br /><br /> Specifies a location to which to redirect requests that match the related wildcard value.|  
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
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding HTTP Wildcard Redirects \<add>](http://www.iis.net/ConfigReference/system.webServer/httpRedirect/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|