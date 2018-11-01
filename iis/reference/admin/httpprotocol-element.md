---
title: "httpProtocol Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: ad772ea8-b67b-4002-a1ba-ae2f9ba8d6fe
caps.latest.revision: 23
author: "shirhatti"
manager: "wpickett"
---
# httpProtocol Element
> [!NOTE]
>  For more information about the `httpProtocol` element, see the following topic on the Microsoft IIS.net Web site: [HTTP Protocol Settings \<httpProtocol>](http://www.iis.net/ConfigReference/system.webServer/httpProtocol).  
  
 Configures custom and redirect response headers to be sent from the server to the client.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`allowKeepAlive`|Optional `Boolean` attribute.<br /><br /> Specifies whether keep-alive processing is permitted (`true`) or not (`false`).<br /><br /> The default value is `true`.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`customHeaders`|Configures custom response headers that are returned in responses from the Web server.|  
|`redirectHeaders`|Configures response headers that are returned in responses only when the Web server redirects requests.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
  
## Remarks  
 For more information about the `httpProtocol` element, see the following topic on the Microsoft IIS.net Web site: [HTTP Protocol Settings \<httpProtocol>](http://www.iis.net/ConfigReference/system.webServer/httpProtocol).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<customHeaders>](../../reference/admin/customheaders-element-for-httpprotocol.md)   
 [\<redirectHeaders>](../../reference/admin/redirectheaders-element.md)