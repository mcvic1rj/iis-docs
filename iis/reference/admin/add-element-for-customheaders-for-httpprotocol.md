---
title: "add Element for customHeaders for httpProtocol | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 8a932ef8-593b-446d-bdc6-8017e557c2c8
caps.latest.revision: 24
author: "shirhatti"
manager: "wpickett"
---
# add Element for customHeaders for httpProtocol
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Custom Headers \<add>](http://www.iis.net/ConfigReference/system.webServer/httpProtocol/customHeaders/add).  
  
 Configures a custom response header to be returned in responses from the Web server.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`name`|Required`string` attribute.<br /><br /> Specifies a field name for the custom response header. In a response, a field name precedes the related field value.|  
|`value`|Optional `string` attribute.<br /><br /> Specifies a field value for the custom response header. In a response, a field value follows the related field name.|  
  
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
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Custom Headers \<add>](http://www.iis.net/ConfigReference/system.webServer/httpProtocol/customHeaders/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|