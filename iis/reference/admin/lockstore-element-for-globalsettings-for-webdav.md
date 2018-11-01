---
title: "lockStore Element for globalSettings for WebDAV | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: e90e3b73-7037-40f5-898f-17cadb0e8de0
caps.latest.revision: 6
author: "shirhatti"
manager: "wpickett"
---
# lockStore Element for globalSettings for WebDAV
> [!NOTE]
>  For more information about the lockStores element, see the following topic on the Microsoft IIS.net Web site: [WebDAV Lock Store Defintions \<lockStores>](http://www.iis.net/ConfigReference/system.webServer/webdav/globalSettings/lockStores).  
  
 Specifies the configuration settings for the collection of lock store providers, which are defined in the webdav/globalSettings/lockStores collection.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Specifies the settings for a lock store provider.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`webdav`|Configures Web Distributed Authoring and Versioning (WebDAV) for Internet Information Services (IIS) 7.|  
|`globalSettings`|Specifies the global WebDAV configuration settings for property and lock provider definitions.|  
  
## Remarks  
 For more information about the lockStores element, see the following topic on the Microsoft IIS.net Web site: [WebDAV Lock Store Defintions \<lockStores>](http://www.iis.net/ConfigReference/system.webServer/webdav/globalSettings/lockStores).  
  
## Element Information  
  
|||  
|-|-|  
|Configuration locations|ApplicationHost.config|  
|Requirements|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-lockstore-for-globalsettings.md)