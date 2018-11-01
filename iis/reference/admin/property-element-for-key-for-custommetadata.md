---
title: "property Element for key for customMetadata | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 69316e5f-b6b1-45c2-8361-44b0156159cb
caps.latest.revision: 19
author: "shirhatti"
manager: "wpickett"
---
# property Element for key for customMetadata
> [!NOTE]
>  For more information about the `property` element, see the following topic on the Microsoft IIS.net Web site: Custom [Metadata Key Property \<property>](http://www.iis.net/ConfigReference/system.applicationHost/customMetadata/key/property).  
  
 Adds a metabase property to the collection of metabase properties.  
  
> [!IMPORTANT]
>  This section of the configuration should not be modified.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`id`|Optional `integer` attribute.<br /><br /> Specifies the unique identifier of the metabase entry.|  
|`dataType`|Required `enum` attribute.<br /><br /> Specifies the type of data to retrieve.<br /><br /> The `dataType` attribute can be one of the following possible values.<br /><br /> `DWord`:<br /><br /> - An unsigned 32-bit number. The numeric value is 1.<br /><br /> `String`:<br /><br /> - A null-terminated ASCII string. The numeric value is 2.<br /><br /> `Binary`:<br /><br /> - Binary data in any form. The numeric value is 3.<br /><br /> `ExpandSZ`:<br /><br /> - A null-terminated string that contains unexpanded environment variables, such as %PATH%. The numeric value is 4.<br /><br /> `MultiSZ`:<br /><br /> - An array of null-terminated strings, terminated by two null characters. The numeric value is 5.|  
|`userType`|Optional `integer` attribute.<br /><br /> Specifies the user type of the data.<br /><br /> The default value is 1.|  
|`attributes`|Optional `enum` attribute.<br /><br /> Specifies the flags, contained in the [METADATA_RECORD](http://msdn.microsoft.com/en-us/276e983e-0714-46d5-b420-e7a0c9a56241) structure, that are used to get the data.<br /><br /> The `attributes` attribute can be one of the following possible values.<br /><br /> The default value is `Inherit`.<br /><br /> `None`:<br /><br /> - Specifies that no flags are set. The numeric value is 0.<br /><br /> `Inherit`:<br /><br /> - Specifies that the data can be inherited. The numeric value is 1.<br /><br /> `PartialPath`:<br /><br /> - Returns any inherited data even if the complete path is not available. This flag is only valid when the `Inherit` flag is also set. The numeric value is 2.<br /><br /> `Secure`:<br /><br /> - Specifies that the data is stored and transported in a secure manner. The numeric value is 4.<br /><br /> `Reference`:<br /><br /> - Specifies that the data was retrieved by reference. The numeric value is 8.<br /><br /> `Volatile`:<br /><br /> - Specifies that the data is not stored in long-term storage. The numeric value is 16.<br /><br /> `IsInherited`:<br /><br /> - Denotes that the data items were inherited. The numeric value is 32.<br /><br /> `InsertPath`:<br /><br /> - Replaces `MD_INSERT_PATH_STRINGW` with the path of the data item relative to the handle. The numeric value is 64.<br /><br /> `LocalMachineOnly`:<br /><br /> - Specifies that the data is not replicated during web cluster replication. The numeric value is 128.<br /><br /> `NonSecureOnly`:<br /><br /> - Specifies that secure properties should not be retrieved when calling `GetAll`. The numeric value is 256.|  
|`value`|Optional case-sensitive `string` attribute.<br /><br /> Specifies a custom value.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`customMetadata`|Contains settings that are used internally by the Admin Base Object (ABO) mapper component of [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`key`|Adds a custom metadata setting to the collection of custom metadata settings.|  
  
## Remarks  
 For more information about the `property` element, see the following topic on the Microsoft IIS.net Web site: Custom [Metadata Key Property \<property>](http://www.iis.net/ConfigReference/system.applicationHost/customMetadata/key/property).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<customMetadata>](../../reference/admin/custommetadata-element.md)   
 [\<key>](../../reference/admin/key-element-for-custommetadata.md)