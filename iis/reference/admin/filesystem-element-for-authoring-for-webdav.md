---
title: "fileSystem Element for authoring for WebDAV | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 8f79f2a7-cbee-4057-864d-aa6118af772a
caps.latest.revision: 7
author: "shirhatti"
manager: "wpickett"
---
# fileSystem Element for authoring for WebDAV
> [!NOTE]
>  For more information about the `webdav` element, see the following topic on the Microsoft IIS.net Web site: [WebDAV File System \<webdav>](http://www.iis.net/ConfigReference/system.webServer/webdav/authoring/fileSystem).  
  
 Specifies how the WebDAV module interacts with the underlying file system.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`allowHiddenFiles`|Optional `Boolean` attribute.<br /><br /> `true` if WebDAV will display hidden files in the responses to property requests; otherwise, `false`. **Note:**  Even though files may be hidden from property requests, they can still be requested directly. For example, if you hid the Web.config file for your Web site, it would not be displayed in directory listings, but you could still open the file in a WebDAV-based editor if you knew that the path existed. <br /><br /> The default value is `false`.|  
|`useTransactionalIo`|Optional `Boolean` attribute.<br /><br /> The `useTransactionalIo` attribute specifies whether file operations should be transactional. For example, transactional processing helps to define what a server's behavior should be if a client sends a `MOVE` request for a series of files and the destination runs out of storage space before the entire operation has completed. With transactional processing enabled, the entire operation should fail. When transactional processing is disabled, the operation will only partially succeed and files will be distributed between the source and destination.<br /><br /> When set to `false`, the WebDAV module will not enforce any form of transactional processing. When set to `true`, the WebDAV module will enforce transactional processing by failing the operation if the base file system cannot transactions.<br /><br /> The default value is `false`.|  
|`hideChildVirtualDirectories`|Optional `Boolean` attribute.<br /><br /> `true` if virtual directories are hidden from WebDAV requests; otherwise, `false`. **Note:**  This attribute was added in WebDAV 7.5 and IIS 7.5. <br /><br /> The default value is `false`.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`webdav`|Configures Web Distributed Authoring and Versioning (WebDAV) for Internet Information Services (IIS) 7.|  
|`authoring`|Specifies the site-level settings for WebDAV.|  
  
## Remarks  
 For more information about the `webdav` element, see the following topic on the Microsoft IIS.net Web site: [WebDAV File System \<webdav>](http://www.iis.net/ConfigReference/system.webServer/webdav/authoring/fileSystem).  
  
## Element Information  
  
|||  
|-|-|  
|Configuration locations|ApplicationHost.config|  
|Requirements|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<authoring>](../../reference/admin/authoring-element-for-webdav.md)