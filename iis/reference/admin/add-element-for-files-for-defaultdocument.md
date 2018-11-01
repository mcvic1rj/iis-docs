---
title: "add Element for files for defaultDocument | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: c6e6ec07-6a57-4f57-a896-7119e04cd910
caps.latest.revision: 17
author: "shirhatti"
manager: "wpickett"
---
# add Element for files for defaultDocument
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Default Document Files \<add>](http://www.iis.net/ConfigReference/system.webServer/defaultDocument/files/add).  
  
 Adds a file name to the list of default documents in the `files` collection.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`name`|Optional `string` attribute.<br /><br /> Specifies a file name of Web content that can be used as a default document. The value must be unique in the `files` collection, and it can be a file name or a relative path.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the root element in ApplicationHost.config that is the top-level section group in which this element is defined.|  
|`files`|Specifies the file names that are configured as default documents.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Default Document Files \<add>](http://www.iis.net/ConfigReference/system.webServer/defaultDocument/files/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root level Web.config<br /><br /> Application level Web.config<br /><br /> Virtual or physical directory level Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|