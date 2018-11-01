---
title: "globalSettings Element for WebDAV | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 2e6213d7-2c2f-45b0-961e-b4e92970a25e
caps.latest.revision: 6
author: "shirhatti"
manager: "wpickett"
---
# globalSettings Element for WebDAV
> [!NOTE]
>  For more information about the `globalSettings` element, see the following topic on the Microsoft IIS.net Web site: [WebDAV Global Settings \<globalSettings>](http://www.iis.net/ConfigReference/system.webServer/webdav/globalSettings).  
  
 Specifies the global WebDAV configuration settings for property and lock provider definitions.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`propertyStores`|Optional element.<br /><br /> Specifies the collection of property store providers.|  
|`lockStores`|Optional element.<br /><br /> Specifies the collection of lock store providers.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`webdav`|Configures Web Distributed Authoring and Versioning (WebDAV) for Internet Information Services (IIS) 7.|  
  
## Remarks  
 For more information about the `globalSettings` element, see the following topic on the Microsoft IIS.net Web site: [WebDAV Global Settings \<globalSettings>](http://www.iis.net/ConfigReference/system.webServer/webdav/globalSettings).  
  
## Element Information  
  
|||  
|-|-|  
|Configuration locations|ApplicationHost.config|  
|Requirements|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<fileSystem>](../../reference/admin/filesystem-element-for-authoring-for-webdav.md)   
 [\<propertyStore>](../../reference/admin/propertystore-element-for-globalsettings-for-webdav.md)