---
title: "add Element for properties for authoring | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: f883ed9b-48a9-40f1-ab80-7f026278e6c3
caps.latest.revision: 6
author: "shirhatti"
manager: "wpickett"
---
# add Element for properties for authoring
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding XML Namespace to Property Provider Mappings \<add>](http://www.iis.net/ConfigReference/system.webServer/webdav/authoring/properties/add).  
  
 Defines a mapping for an XML namespace to a property store provider.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|xmlNamespace|Required `string` attribute.<br /><br /> Specifies the XML namespace for the mapping. **Note:**  The wildcard "*" character is used to define the default namespace mapping, and any namespace that does not have a unique mapping will use the wildcard mapping. If a WebDAV client uses an XML namespace for which there is no specific namespace mapping and a wildcard mapping does not exist, the properties cannot be stored. <br /><br /> The default value is `false`.|  
|propertyStore|Required `string` attribute.<br /><br /> Specifies the property store for the mapping. **Note:**  The name of the property store must be defined in the `propertyStores` collection. <br /><br /> The default value is `false`.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`webdav`|Configures Web Distributed Authoring and Versioning (WebDAV) for Internet Information Services (IIS) 7.|  
|`authoring`|Specifies the site-level settings for WebDAV.|  
|`properties`|Configures locking behavior properties for the WebDAV module.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding XML Namespace to Property Provider Mappings \<add>](http://www.iis.net/ConfigReference/system.webServer/webdav/authoring/properties/add).  
  
## Element Information  
  
|||  
|-|-|  
|Configuration locations|ApplicationHost.config|  
|Requirements|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<properties>](../../reference/admin/properties-element-for-authoring-for-webdav.md)