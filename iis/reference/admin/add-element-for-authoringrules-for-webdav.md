---
title: "add Element for authoringRules for WebDAV | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 6f7f760c-c8d3-4997-b69d-18d33b3e8b72
caps.latest.revision: 9
author: "shirhatti"
manager: "wpickett"
---
# add Element for authoringRules for WebDAV
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding WebDAV Authoring Rules \<add>](http://www.iis.net/ConfigReference/system.webServer/webdav/authoringRules/add).  
  
 Specifies the access permissions for users or groups for specific content types for a unique authoring rule.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`access`|Optional `flags` attribute.<br /><br /> Specifies the access settings for the authoring rule. These values combined with a logical OR operation, so "None, Read" = "Read."<br /><br /> Note:<br /><br /> Source access allows a WebDAV client to request the contents of a script-mapped file, such as an ASP.NET or PHP file, as opposed to the processed output of the file.<br /><br /> `None`<br /><br /> - No authoring is allowed.<br /><br /> - The numeric value is 0.<br /><br /> `Read`<br /><br /> - Read access is allowed.<br /><br /> - The numeric value is 1.<br /><br /> `Write`<br /><br /> - Write access is allowed.<br /><br /> - The numeric value is 2.<br /><br /> `Source`<br /><br /> - Access to source code is allowed.<br /><br /> - The numeric value is 16.<br /><br /> The default value is `None`.|  
|`path`|Optional `string` attribute.<br /><br /> Specifies the file name or the file name extension for which the authoring rule applies. For example, "*.aspx", "\*.php", etc. In addition, the following special identifiers have been defined.<br /><br /> \*<br /><br /> - Specifies that the rule will apply to all content.<br /><br /> There is no default value.|  
|`roles`|Optional `string` attribute.<br /><br /> Specifies roles or groups for an authorization rule. Multiple roles can be added in a comma-separated list.<br /><br /> There is no default value.|  
|`users`|Optional `string` attribute.<br /><br /> Specifies users for an authorization rule. Multiple users can be added in a comma-separated list. In addition, the following special identifiers have been defined.<br /><br /> *<br /><br /> - Specifies that the rule will apply to all users.<br /><br /> ?<br /><br /> - Specifies that the rule will apply to anonymous users.<br /><br /> There is no default value.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`webdav`|Configures Web Distributed Authoring and Versioning (WebDAV) for Internet Information Services (IIS) 7.|  
|`authoringRules`|Specifies the access permissions for users or groups for specific content types for a unique authoring rule.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding WebDAV Authoring Rules \<add>](http://www.iis.net/ConfigReference/system.webServer/webdav/authoringRules/add).  
  
## Element Information  
  
|||  
|-|-|  
|Configuration locations|ApplicationHost.config|  
|Requirements|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<authoringRules>](../../reference/admin/authoringrules-element-for-webdav.md)