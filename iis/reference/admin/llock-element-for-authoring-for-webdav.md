---
title: "llock Element for authoring for WebDAV | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 9c2824ce-a59e-49ab-8702-de744387bc7a
caps.latest.revision: 7
author: "shirhatti"
manager: "wpickett"
---
# llock Element for authoring for WebDAV
> [!NOTE]
>  For more information about the `lock` element, see the following topic on the Microsoft IIS.net Web site: [WebDAV Locks \<lock>](http://www.iis.net/ConfigReference/system.webServer/webdav/authoring/locks).  
  
 Defines the locking behavior for the WebDAV module.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`enabled`|Optional `Boolean` attribute.<br /><br /> `true` if WebDAV locking is enabled; otherwise, `false`.<br /><br /> The default value is `false`.|  
|`lockStore`|Optional `string` attribute.<br /><br /> Specifies the name of the provider to use for WebDAV locking. This name must be defined in the `lockStores`<br /><br /> collection. For information on the `lockStore` element, see [\<lockStore>](../../reference/admin/lockstore-element-for-globalsettings-for-webdav.md).<br /><br /> This attribute has no default value.|  
|`requireLockForWriting`|Optional `Boolean` attribute.<br /><br /> `true` if locks are required for WebDAV authoring; otherwise, `false`. Requiring locks for WebDAV authoring helps to prevent collisions in a multi-source authoring environment.<br /><br /> The default value is `false`.|  
  
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
 For more information about the `lock` element, see the following topic on the Microsoft IIS.net Web site: [WebDAV Locks \<lock>](http://www.iis.net/ConfigReference/system.webServer/webdav/authoring/locks).  
  
## Element Information  
  
|||  
|-|-|  
|Configuration locations|ApplicationHost.config|  
|Requirements|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<authoring>](../../reference/admin/authoring-element-for-webdav.md)