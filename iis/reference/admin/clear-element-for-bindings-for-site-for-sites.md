---
title: "clear Element for bindings for site for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: f4c3f20e-3419-490e-9342-afa597bd2e1a
caps.latest.revision: 24
author: "shirhatti"
manager: "wpickett"
---
# clear Element for bindings for site for sites
> [!NOTE]
>  For more information about the `bindings` element, see the following topic on the Microsoft IIS.net Web site: [Bindings \<bindings>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/bindings).  
  
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
|`site`|Specifies configuration settings for a site.|  
|`bindings`|Specifies bindings to access the site.|  
  
## Remarks  
 For more information about the `bindings` element, see the following topic on the Microsoft IIS.net Web site: [Bindings \<bindings>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/bindings).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|