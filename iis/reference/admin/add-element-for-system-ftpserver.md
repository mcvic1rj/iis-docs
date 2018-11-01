---
title: "add Element for system.ftpServer | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 6f06a96b-14bc-47d8-82c2-b49ab2f4de78
caps.latest.revision: 7
author: "shirhatti"
manager: "wpickett"
---
# add Element for system.ftpServer
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding FTP Provider Activation Data \<add>](http://www.iis.net/ConfigReference/system.ftpServer/providerDefinitions/activation/providerData/add).  
  
 Specifies a unique key/value pair, which defines a custom parameter that an FTP custom provider requires.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`key`|Required `string` attribute.<br /><br /> Specifies the unique name of the key for the key/value pair.<br /><br /> There is no default value.|  
|`value`|Optional `string` attribute.<br /><br /> Specifies the unencrypted value for the key/value pair. **Note:**  If the `value` attribute is used, do not use the `encryptedValue` attribute. <br /><br /> There is no default value.|  
|`encryptedValue`|Optional `string` attribute.<br /><br /> Specifies the unencrypted value for the key/value pair. **Note:**  If the `encryptedValue` attribute is used, do not use the `value` attribute. <br /><br /> There is no default value.|  
  
### Child Elements  
 None  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.ftpServer`|Specifies the top-level section group in which this element is defined.|  
|`providerDefinitions`|Specifies a collection of custom FTP providers.|  
|`activation`|Specifies a collection of custom name/value pairs that specify any parameters that a custom FTP provider requires.|  
|`providerData`|Specifies the collection of key/value pairs that contain the data for a custom provider.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding FTP Provider Activation Data \<add>](http://www.iis.net/ConfigReference/system.ftpServer/providerDefinitions/activation/providerData/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<providerData>](../../reference/admin/providerdata-element-for-system-ftpserver.md)