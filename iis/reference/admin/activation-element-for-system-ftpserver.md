---
title: "activation Element for system.ftpServer | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: ee727997-9165-4a9c-8a2f-3259f5838b1c
caps.latest.revision: 6
author: "shirhatti"
manager: "wpickett"
---
# activation Element for system.ftpServer
> [!NOTE]
>  For more information about the `activation` element, see the following topic on the Microsoft IIS.net Web site: [FTP Provider Activation \<activation>](http://www.iis.net/ConfigReference/system.ftpServer/providerDefinitions/activation).  
  
 Specifies a collection of custom name/value pairs that specify any parameters that a custom FTP provider requires.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`providerData`|Optional element.<br /><br /> Specifies the collection of key/value pairs that contain the data for a custom provider.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.ftpServer`|Specifies the top-level section group in which this element is defined.|  
|`providerDefinitions`|Specifies the root element for configuring a collection of custom FTP providers.|  
  
## Remarks  
 For more information about the `activation` element, see the following topic on the Microsoft IIS.net Web site: [FTP Provider Activation \<activation>](http://www.iis.net/ConfigReference/system.ftpServer/providerDefinitions/activation).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration Locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<providerData>](../../reference/admin/providerdata-element-for-system-ftpserver.md)