---
title: "authoringRules Element for WebDAV | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 3f6d9469-4c36-4b39-9f55-c904632aa165
caps.latest.revision: 8
author: "shirhatti"
manager: "wpickett"
---
# authoringRules Element for WebDAV
> [!NOTE]
>  For more information about the `authoringRules` element, see the following topic on the Microsoft IIS.net Web site: [WebDAV Authoring Rules \<authoringRules>](http://www.iis.net/ConfigReference/system.webServer/webdav/authoringRules).  
  
 Specifies the WebDAV authoring permissions for a URI space. This element is can be defined per-URI within a Web site. The permissions in this element are inherited, so child URIs will have the same permissions as a parent URI, provided that the child URI does not have unique permissions defined.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`defaultAccess`|Optional `flags` attribute.<br /><br /> Specifies the default access settings for WebDAV authoring. These values combined with a logical `OR` operation, so "`None`, `Read`" = "`Read`."<br /><br /> Source access allows a WebDAV client to request the contents of a script-mapped file, such as an ASP.NET or PHP file, as opposed to the processed output of the file.<br /><br /> The default value is `None`.<br /><br /> `None`:<br /><br /> - No authoring is allowed.<br /><br /> - The numeric value is 0.<br /><br /> `Read`:<br /><br /> - Read access is allowed.<br /><br /> - The numeric value is 1.<br /><br /> `Write`:<br /><br /> - Write access is allowed.<br /><br /> - The numeric value is 2.<br /><br /> `Source`:<br /><br /> - Access to source code is allowed.<br /><br /> - The numeric value is 16.|  
|`allowNonMimeMapFiles`|Optional `Boolean` attribute.<br /><br /> `true` if WebDAV requests should be allowed for files that are not defined in the MIME map; otherwise, `false`.<br /><br /> For example, files that are script-mapped are not defined in the MIME map, but Web authors may still need to edit these files, which are not allowed in IIS requests by default. When set to true, the WebDAV module will accept requests for files that are not included in the MIME map. When set to false, the module will require that all files are found in the MIME map and return a "404.3 – MIME map policy prevents this request" error for any request that does not match the MIME list.<br /><br /> The default value is `false`.|  
|`defaultMimeType`|Optional `string` attribute.<br /><br /> Specifies the default MIME type for files that do not have an explicit MIME type defined.<br /><br /> The default value is application/octet-stream.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds an authoring rule to the collection of authoring rules.|  
|`clear`|Optional element.<br /><br /> Clears the collection of authoring rules.|  
|`remove`|Optional element.<br /><br /> Removes an authoring rule from the collection of authoring rules.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`webdav`|Configures Web Distributed Authoring and Versioning (WebDAV) for Internet Information Services (IIS) 7.|  
  
## Remarks  
 For more information about the `authoringRules` element, see the following topic on the Microsoft IIS.net Web site: [WebDAV Authoring Rules \<authoringRules>](http://www.iis.net/ConfigReference/system.webServer/webdav/authoringRules).  
  
## Element Information  
  
|||  
|-|-|  
|Configuration locations|ApplicationHost.config|  
|Requirements|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-authoringrules-for-webdav.md)