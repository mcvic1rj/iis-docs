---
title: "propertyStore Element for globalSettings for WebDAV | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 161099ef-bf1b-4c63-b63e-18f7ad1625a5
caps.latest.revision: 6
author: "shirhatti"
manager: "wpickett"
---
# propertyStore Element for globalSettings for WebDAV
> [!NOTE]
>  For more information about the propertyStores element, see the following topic on the Microsoft IIS.net Web site: [WebDAV Property Store Definitions \<propertyStores>](http://www.iis.net/ConfigReference/system.webServer/webdav/globalSettings/propertyStores).  
  
 Specifies settings for a collection of property store providers, which are defined in the webdav/globalSettings/propertyStores collection.  
  
> [!NOTE]
>  Currently the only property store provider is webdav_simple_prop, which stores WebDAV properties in files that are named Propeties.dav in each content directory.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Specifies the settings for a property store provider.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`webdav`|Configures Web Distributed Authoring and Versioning (WebDAV) for Internet Information Services (IIS) 7.|  
  
## Remarks  
 For more information about the propertyStores element, see the following topic on the Microsoft IIS.net Web site: [WebDAV Property Store Definitions \<propertyStores>](http://www.iis.net/ConfigReference/system.webServer/webdav/globalSettings/propertyStores).  
  
## Element Information  
  
|||  
|-|-|  
|Configuration locations|ApplicationHost.config|  
|Requirements|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-propertystore-for-globalsettings.md)