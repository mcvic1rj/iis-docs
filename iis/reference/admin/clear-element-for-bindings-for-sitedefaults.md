---
title: "clear Element for bindings for siteDefaults | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: ab03f8dd-03ce-41de-9f41-f6a739d58dc8
caps.latest.revision: 13
author: "shirhatti"
manager: "wpickett"
---
# clear Element for bindings for siteDefaults
> [!NOTE]
>  For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [Default Bindings \<bindings>](http://www.iis.net/ConfigReference/system.applicationHost/sites/siteDefaults/bindings/binding).  
  
 Clears references to default settings that are inherited from the parent level of the configuration.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`sites`|Specifies configuration settings for all sites on the server, and includes settings for applications and virtual directories in those sites.|  
|`siteDefaults`|Specifies default settings for all sites on the server.|  
|`bindings`|Specifies the default bindings to access all sites on the server.|  
  
## Remarks  
 For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [Default Bindings \<bindings>](http://www.iis.net/ConfigReference/system.applicationHost/sites/siteDefaults/bindings/binding).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|