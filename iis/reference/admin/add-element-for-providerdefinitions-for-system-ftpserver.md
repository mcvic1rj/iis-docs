---
title: "add Element for providerDefinitions for system.ftpServer | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 50cecd8c-1c23-4b89-8f2f-66a9005e4a02
caps.latest.revision: 7
author: "shirhatti"
manager: "wpickett"
---
# add Element for providerDefinitions for system.ftpServer
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding FTP Provider Definitions \<add>](http://www.iis.net/ConfigReference/system.ftpServer/providerDefinitions/add).  
  
 Specifies the registration information for a managed-code or native-code (COM) provider.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`Name`|Required `string` attribute.<br /><br /> Specifies the friendly name for a custom provider.<br /><br /> There is no default value.|  
|`type`|Optional `string` attribute.<br /><br /> Specifies the type for a managed-code provider.<br /><br /> There is no default value.|  
|`clsid`|Optional `string` attribute.<br /><br /> Specifies the COM class ID for a native-code provider.<br /><br /> There is no default value.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.ftpServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`providerDefinitions`|Specifies the collection of custom FTP providers.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding FTP Provider Definitions \<add>](http://www.iis.net/ConfigReference/system.ftpServer/providerDefinitions/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<providerDefinitiions>](../../reference/admin/providerdefinitions-element-for-system-ftpserver.md)