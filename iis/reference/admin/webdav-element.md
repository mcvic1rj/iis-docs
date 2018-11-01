---
title: "WebDAV Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: cd69c8c1-8b62-4f49-ab85-0c5e9085e5f8
caps.latest.revision: 6
author: "shirhatti"
manager: "wpickett"
---
# WebDAV Element
> [!NOTE]
>  For more information about the webdav element, see the following topic on the Microsoft IIS.net Web site: [WebDAV \<webdav>](http://www.iis.net/ConfigReference/system.webServer/webdav).  
  
 Contains the settings that configure Web Distributed Authoring and Versioning (WebDAV) for Internet Information Services (IIS) 7. WebDAV is an Internet-based open standard that enables editing Web sites over HTTP and HTTPS connections. WebDAV yields several advantages over the File Transfer Protocol (FTP), the most notable advantages are more security options and the ability to use a single TCP port for all communication.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`authoring`|Optional element.<br /><br /> Specifies the configuration settings for WebDAV authoring.|  
|`authoringRules`|Optional element.<br /><br /> Specifies the authoring rules for WebDAV publishing. These rules specify the content types and authoring permissions for users or groups.|  
|`globalSettings`|Optional element.<br /><br /> Specifies the global settings for the WebDAV module.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
  
## Remarks  
 For more information about the webdav element, see the following topic on the Microsoft IIS.net Web site: [WebDAV \<webdav>](http://www.iis.net/ConfigReference/system.webServer/webdav).  
  
## Element Information  
  
|||  
|-|-|  
|Configuration locations|ApplicationHost.config|  
|Requirements|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<authoring>](../../reference/admin/authoring-element-for-webdav.md)   
 [\<authoringRules>](../../reference/admin/authoringrules-element-for-webdav.md)   
 [\<globalSettings>](../../reference/admin/globalsettings-element-for-webdav.md)