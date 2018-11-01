---
title: "properties Element for authoring for WebDAV | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 035b0f75-2874-48dc-a1a2-743fab915d60
caps.latest.revision: 6
author: "shirhatti"
manager: "wpickett"
---
# properties Element for authoring for WebDAV
> [!NOTE]
>  For more information about the `properties` element, see the following topic on the Microsoft IIS.net Web site: [WebDAV Properties \<properties>](http://www.iis.net/ConfigReference/system.webServer/webdav/authoring/properties).  
  
 Configures locking behavior properties for the WebDAV module.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`allowAnonymousPropfind`|Optional `Boolean` attribute.<br /><br /> `true` if anonymous WebDAV property requests are allowed; otherwise, `false`. **Important:**  Most WebDAV verbs require authentication; however, anonymous WebDAV property requests may be allowed for backwards-compatibility for some WebDAV clients. Unless there is a specific requirement for your environment, anonymous WebDAV property requests should always be disabled because they introduce the chance of information disclosure for a Web site. For example, an anonymous WebDAV client can retrieve a list of files in your application. <br /><br /> The default value is `false`.|  
|`allowInfinitePropfindDepth`|Optional `Boolean` attribute.<br /><br /> `true` if infinite-depth WebDAV property requests are allowed; otherwise, `false`. **Note:**  Allowing infinite-depth WebDAV property requests is strongly discouraged due to the amount of CPU time that may be required to fullfill an infinite-depth WebDAV property request. This could even lead to a denial of service for your application. Unless there is a specific requirement for your environment, infinite-depth WebDAV property requests should always be disabled. <br /><br /> The default value is `false`.|  
|`allowCustomProperties`|Optional `Boolean` attribute.<br /><br /> `true` if custom WebDAV properties are allowed; otherwise, `false`. **Note:**  Custom WebDAV properties are also known as "dead" properties. **Note:**  If `allowCustomProperties` is set to `true` but no property stores are defined or there are no XML namespace to property store mappings, no custom properties can be stored. <br /><br /> The default value is `true`.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a mapping for an XML namespace to a property provider.|  
|`clear`|Optional element.<br /><br /> Clears all the existing namespace mappings.|  
|`remove`|Optional element.<br /><br /> Removes a mapping from the list of XML namespaces to property providers.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`webdav`|Configures Web Distributed Authoring and Versioning (WebDAV) for Internet Information Services (IIS) 7.|  
  
## Remarks  
 For more information about the `properties` element, see the following topic on the Microsoft IIS.net Web site: [WebDAV Properties \<properties>](http://www.iis.net/ConfigReference/system.webServer/webdav/authoring/properties).  
  
## Element Information  
  
|||  
|-|-|  
|Configuration locations|ApplicationHost.config|  
|Requirements|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-properties-for-authoring.md)