---
title: "providerData Element for system.ftpServer | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: c9314c59-a2cf-493c-8707-6256c0c0208e
caps.latest.revision: 7
author: "shirhatti"
manager: "wpickett"
---
# providerData Element for system.ftpServer
> [!NOTE]
>  For more information about the `providerData` element, see the following topic on the Microsoft IIS.net Web site: [Provider Activation Data \<providerData>](http://www.iis.net/ConfigReference/system.ftpServer/providerDefinitions/activation/providerData).  
  
 Specifies the collection of key/value pairs that contain the data for a custom provider.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`name`|Required `string` attribute.<br /><br /> Specifies the friendly name of the custom provider. **Note:**  This name must match the name of a provider that is specified by a `providerDefinitions`.`add` element. <br /><br /> There is no default value.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a data entry for a custom provider.|  
|`clear`|Optional element.<br /><br /> Clears the data for a custom provider.|  
|`remove`|Optional element.<br /><br /> Removes a data entry for a custom provider.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.ftpServer`|Specifies the top-level section group in which this element is defined.|  
|`providerDefinitions`|Specifies a collection of custom FTP providers.|  
|`activation`|Specifies a collection of custom name/value pairs that specify any parameters that a custom FTP provider requires.|  
  
## Remarks  
 For more information about the `providerData` element, see the following topic on the Microsoft IIS.net Web site: [Provider Activation Data \<providerData>](http://www.iis.net/ConfigReference/system.ftpServer/providerDefinitions/activation/providerData).  
  
## Element Information  
  
|||  
|-|-|  
|Configuration locations|ApplicationHost.config|  
|Requirements|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-system-ftpserver.md)