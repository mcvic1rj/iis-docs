---
title: "authoring Element for WebDAV | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 874733b9-94e9-4c99-9a56-d5416a01b2dd
caps.latest.revision: 13
author: "shirhatti"
manager: "wpickett"
---
# authoring Element for WebDAV
> [!NOTE]
>  For more information about the authoring element, see the following topic on the Microsoft IIS.net Web site:                  [WebDAV Authoring \<authoring>](http://www.iis.net/ConfigReference/system.webServer/webdav/authoring).  
  
 Specifies the site-level settings for WebDAV.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`compatFlags`|Optional                                  `flags` attribute.<br /><br /> Specifies the compatibility options for WebDAV. There are several behaviors that were used in previous versions of the Microsoft WebDAV implementations, and the flags in this attribute specify which of those behaviors the new WebDAV module will implement.<br /><br /> The                                  `compatFlags` attribute can have one or more of the following possible values. If you specify more than one value, separate them with a comma (,). The default value is                                  `MsAuthorVia`,                                  `MultiProp`,                                  `CompactXml`,                                  `IsHidden`,                                  `IsCollection`.<br /><br /> `None`:<br /><br /> - No compatibility options should be used.<br /><br /> - The numeric value is 0.<br /><br /> `MsAuthorVia`:<br /><br /> - Specifies whether the WebDAV module should return the "MS-Author-Via" header to WebDAV clients.<br /><br /> - Note: Some WebDAV clients expect this header.<br /><br /> - The numeric value is 1.<br /><br /> `MultiProp`:<br /><br /> - Specifies whether multiple \<prop> statements should be allowed in WebDAV requests.<br /><br /> - Note: This violates RFC 4918, but some earlier WebDAV implementations supported this syntax.<br /><br /> - The numeric value is 2.<br /><br /> `CompactXml`:<br /><br /> - Specifies whether the XML that is returned by the WebDAV module should be formatted hierarchically.<br /><br /> - Note: Normally the WebDAV module will simply return XML responses with no CRLF characters and no indentation. This cuts down on the size of the data that is transmitted over the wire, but it’s very difficult to read without an XML parser.<br /><br /> - The numeric value is 4.<br /><br /> `IsHidden`:<br /><br /> - Specifies that the                                                  `IsHidden` pseudo-live property should be supported.<br /><br /> - Note: This property is an informal standard that is not defined in RFC 4918.<br /><br /> - The numeric value is 8.|  
|`enabled`|Optional                                  `Boolean` attribute.<br /><br /> `true` if WebDAV authoring is enabled; otherwise,                                  `false`.<br /><br /> The default value is                                  `false`.|  
|`maxAllowedXmlRequestLength`|Optional                                  `uint` attribute.<br /><br /> Specifies the maximum length, in bytes, of the request XML body for WebDAV requests.<br /><br /> Note:<br /><br /> This attribute was added in WebDAV 7.5 and IIS 7.5.<br /><br /> The default value is 1000000.|  
|`requireSsl`|Optional                                  `Boolean` attribute.<br /><br /> `true` if SSL is required for WebDAV authoring; otherwise,                                  `false`. Requiring SSL for WebDAV authoring adds an additional layer of security, but adds to the processing overhead for each request.<br /><br /> The default value is                                  `false`.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`fileSystem`|Optional element.<br /><br /> Specifies how the WebDAV module interacts with the underlying file system.|  
|`locks`|Optional element.<br /><br /> Specifies the WebDAV locking settings.|  
|`properties`|Optional element<br /><br /> Specifies the WebDAV property settings.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by                                  [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`webdav`|Configures Web Distributed Authoring and Versioning (WebDAV) for Internet Information Services (IIS) 7.|  
  
## Remarks  
 For more information about the authoring element, see the following topic on the Microsoft IIS.net Web site:                  [WebDAV Authoring \<authoring>](http://www.iis.net/ConfigReference/system.webServer/webdav/authoring).  
  
## Element Information  
  
|||  
|-|-|  
|Configuration locations|ApplicationHost.config|  
|Requirements|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<fileSystem>](../../reference/admin/filesystem-element-for-authoring-for-webdav.md)   
 [\<locks>](../../reference/admin/llock-element-for-authoring-for-webdav.md)   
 [\<properties>](../../reference/admin/properties-element-for-authoring-for-webdav.md)