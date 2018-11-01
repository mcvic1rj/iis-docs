---
title: "fileExtensions Element for requestFiltering for security for system.ftpServer | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: b033d511-06d9-4ef0-9fa1-9ed4532093d4
caps.latest.revision: 7
author: "shirhatti"
manager: "wpickett"
---
# fileExtensions Element for requestFiltering for security for system.ftpServer
> [!NOTE]
>  For more information about the `fileExtensions` element, see the following topic on the Microsoft IIS.net Web site: [FTP File Name Extensions \<fileExtensions>](http://www.iis.net/ConfigReference/system.ftpServer/security/requestFiltering/fileExtensions).  
  
 Contains a collection of file name extensions that IIS will either allow or deny, depending on how the settings of each element are defined.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`allowUnlisted`|Optional `Boolean` attribute.<br /><br /> Specifies whether the Web server should process files that have unlisted file name extensions. If you set this attribute to true, you must list all file name extensions that you want to deny. If you set this attribute to false, you must list all file name extensions that you want to allow.<br /><br /> The default value is `true`.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a file name extension to the collection of file name extensions.|  
|`remove`|Optional element.<br /><br /> Removes all references to file name extensions from the `fileExtensions` collection.|  
|`clear`|Optional element.<br /><br /> Removes a reference to a file name extension from the `fileExtensions` collection.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.ftpServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the root element for configuring FTP server settings.|  
|`requestFiltering`|Specifies configuration settings for request filtering.|  
  
## Remarks  
 For more information about the `fileExtensions` element, see the following topic on the Microsoft IIS.net Web site: [FTP File Name Extensions \<fileExtensions>](http://www.iis.net/ConfigReference/system.ftpServer/security/requestFiltering/fileExtensions).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-fileextensions-for-system-ftpserver.md)