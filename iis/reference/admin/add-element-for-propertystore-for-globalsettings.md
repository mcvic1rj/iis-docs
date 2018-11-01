---
title: "add Element for propertyStore for globalSettings | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 27f19afb-a0bc-4894-85ef-451fb808702d
caps.latest.revision: 6
author: "shirhatti"
manager: "wpickett"
---
# add Element for propertyStore for globalSettings
> [!NOTE]
>  For more information about the add element, see the following topic on the Microsoft IIS.net Web site: [Adding WebDAV Property Stores \<add>](http://www.iis.net/ConfigReference/system.webServer/webdav/globalSettings/propertyStores/add).  
  
 Specifies the settings for a property store provider.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`name`|Required attribute.<br /><br /> Specifies the name for a property store provider.|  
|`image`|Required attribute.<br /><br /> Specifies the file system path for a property store provider. **Note:**  On a 64-bit system this will be the 64-bit path, whereas on a 32-bit system this will contain the path to the 32-bit provider and the `image32` attribute will be ignored.|  
|`image32`|Optional attribute.<br /><br /> Specifies the 32-bit path for a property provider on a 64-bit system. **Note:**  This attribute was added in WebDAV 7.5 and IIS 7.5.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`webdav`|Configures Web Distributed Authoring and Versioning (WebDAV) for Internet Information Services (IIS) 7.|  
|`propertyStore`|Specifies settings for a collection of property store providers.|  
  
## Remarks  
 For more information about the add element, see the following topic on the Microsoft IIS.net Web site: [Adding WebDAV Property Stores \<add>](http://www.iis.net/ConfigReference/system.webServer/webdav/globalSettings/propertyStores/add).  
  
## Element Information  
  
|||  
|-|-|  
|Configuration locations|ApplicationHost.config|  
|Requirements|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<propertyStore>](../../reference/admin/propertystore-element-for-globalsettings-for-webdav.md)