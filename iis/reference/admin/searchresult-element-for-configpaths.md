---
title: "searchResult Element for configPaths | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 6237c5ee-4611-4c77-8696-14a7384713cd
caps.latest.revision: 13
author: "shirhatti"
manager: "wpickett"
---
# searchResult Element for configPaths
> [!NOTE]
>  For more information about the `searchResult` element, see the following topic on the Microsoft IIS.net Web site: [Configuration Path Search Results \<searchResult>](http://www.iis.net/ConfigReference/configPaths/searchResult).  
  
 Contains a collection of configuration search results.  
  
> [!NOTE]
>  These settings are read-only and are not configurable by the end user.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`path`|Required `string` attribute.<br /><br /> Indicates the absolute virtual path of the configuration file.|  
|`locationPath`|Required `string` attribute.<br /><br /> Indicates the relative path for the location tag inside the configuration file.|  
|`status`|Required `int` attribute.<br /><br /> Specifies a status code that indicates whether the search for `path` and `locationPath` was successful.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`section`|Contains a collection of section names returned by the configuration search, for example, "system.webServer/security/authentication/windowsAuthentication."|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`configPaths`|Lists the locations where a configuration setting is set across the distributed configuration file system.|  
  
## Remarks  
 For more information about the `searchResult` element, see the following topic on the Microsoft IIS.net Web site: [Configuration Path Search Results \<searchResult>](http://www.iis.net/ConfigReference/configPaths/searchResult).  
  
## Default Configuration  
 None.  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|None.|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<section>](../../reference/admin/section-element-for-searchresult-for-configpaths.md)