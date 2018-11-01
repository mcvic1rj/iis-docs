---
title: "customMetadata Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 17067176-a48d-4ea5-b8a9-fe06d26f2ae7
caps.latest.revision: 18
author: "shirhatti"
manager: "wpickett"
---
# customMetadata Element
> [!NOTE]
>  For more information about the `customMetadata` element, see the following topic on the Microsoft IIS.net Web site: [Custom Metadata \<customMetadata>](http://www.iis.net/ConfigReference/system.applicationHost/customMetadata).  
  
 Contains settings that are used internally by the Admin Base Object (ABO) mapper component of [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].  
  
> [!IMPORTANT]
>  This section of the configuration should not be modified.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`key`|Optional element.<br /><br /> Adds a custom metadata setting to the collection of custom metadata settings.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
  
## Remarks  
 For more information about the `customMetadata` element, see the following topic on the Microsoft IIS.net Web site: [Custom Metadata \<customMetadata>](http://www.iis.net/ConfigReference/system.applicationHost/customMetadata).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<key>](../../reference/admin/key-element-for-custommetadata.md)