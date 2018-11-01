---
title: "section Element for SearchResult for configPaths | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 208612db-938e-4e74-997d-ae5dbe7621db
caps.latest.revision: 12
author: "shirhatti"
manager: "wpickett"
---
# section Element for SearchResult for configPaths
> [!NOTE]
>  For more information about the `section` element, see the following topic on the Microsoft IIS.net Web site: [Configuration Path Search Result Sections \<section>](http://www.iis.net/ConfigReference/configPaths/searchResult/section).  
  
 Contains a collection of section names returned by the configuration search, for example, "system.webServer/security/authentication/windowsAuthentication."  
  
> [!NOTE]
>  These settings are read-only and are not configurable by the end user.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`name`|Required `string` attribute.<br /><br /> Specifies the name of the section returned by the configuration search.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`configPaths`|Lists the locations where a configuration setting is set across the distributed configuration file system.|  
|`searchResult`|Contains a collection of configuration search results.|  
  
## Remarks  
 For more information about the `section` element, see the following topic on the Microsoft IIS.net Web site: [Configuration Path Search Result Sections \<section>](http://www.iis.net/ConfigReference/configPaths/searchResult/section).  
  
## Default Configuration  
 None.  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|None.|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|