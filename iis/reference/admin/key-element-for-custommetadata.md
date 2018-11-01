---
title: "key Element for customMetadata | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 6eccebfe-f7f6-4d6b-8cfb-b62d09a9e9d9
caps.latest.revision: 16
author: "shirhatti"
manager: "wpickett"
---
# key Element for customMetadata
> [!NOTE]
>  For more information about the `key` element, see the following topic on the Microsoft IIS.net Web site: [Custom Metadata Keys \<key>](http://www.iis.net/ConfigReference/system.applicationHost/customMetadata/key).  
  
 Adds a custom metadata setting to the collection of custom metadata settings.  
  
> [!IMPORTANT]
>  This section of the configuration should not be modified.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`path`|Optional `string` attribute.<br /><br /> Specifies the path of the metabase property.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`property`|Optional element.<br /><br /> Adds a metabase property to the collection of metabase properties.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`customMetabase`|Contains settings that are used internally by the Admin Base Object (ABO) mapper component of [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
  
## Remarks  
 For more information about the `key` element, see the following topic on the Microsoft IIS.net Web site: [Custom Metadata Keys \<key>](http://www.iis.net/ConfigReference/system.applicationHost/customMetadata/key).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<property>](../../reference/admin/property-element-for-key-for-custommetadata.md)