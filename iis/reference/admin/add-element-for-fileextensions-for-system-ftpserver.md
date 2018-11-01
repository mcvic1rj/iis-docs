---
title: "add Element for fileExtensions for system.ftpServer | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: fe2b1129-a43f-4172-8042-410bdd8ef699
caps.latest.revision: 7
author: "shirhatti"
manager: "wpickett"
---
# add Element for fileExtensions for system.ftpServer
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding FTP File Name Extensions \<add>](http://www.iis.net/ConfigReference/system.ftpServer/security/requestFiltering/fileExtensions/add).  
  
 Specifies a unique file name extension to add to the collection of file name extensions for FTP 7.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`allowed`|Required `Boolean` attribute.<br /><br /> Specifies whether the file name extension is allowed or denied. Setting this attribute to true allows the Web server to process requests associated with this type of file; setting this attribute to false prevents the Web server from processing requests.<br /><br /> The default value is `true`.|  
|`fileExtension`|Required `string` attribute.<br /><br /> Specifies the name of the file name extension to allow or deny.<br /><br /> There is no default value.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.ftpServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies security settings for an FTP server.|  
|`requestFiltering`|Specifies the root element for configuring Web process settings.|  
|`fileExtensions`|Contains a collection of file name extensions that IIS will either allow or deny, depending on how the settings of each element are defined.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding FTP File Name Extensions \<add>](http://www.iis.net/ConfigReference/system.ftpServer/security/requestFiltering/fileExtensions/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<fileExtensions>](../../reference/admin/fileextensions-element-for-requestfiltering-for-security-for-system-ftpserver.md)