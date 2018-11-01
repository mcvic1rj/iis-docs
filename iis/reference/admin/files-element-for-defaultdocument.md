---
title: "files Element for defaultDocument | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 8c7bceb0-f649-4378-87d6-9efb9eb1300a
caps.latest.revision: 18
author: "shirhatti"
manager: "wpickett"
---
# files Element for defaultDocument
> [!NOTE]
>  For more information about the `files` element, see the following topic on the Microsoft IIS.net Web site: [Default Document Files \<files>](http://www.iis.net/ConfigReference/system.webServer/defaultDocument/files).  
  
 Specifies the file names that are configured as default documents.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a file name to the collection of files.|  
|`remove`|Optional element.<br /><br /> Removes a reference to a file name from the files collection.|  
|`clear`|Optional element.<br /><br /> Removes all references to file names from the files collection.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the root element in ApplicationHost.config that is the top-level section group in which this element is defined.|  
|`defaultDocument`|Configures settings for returning a default document to a client browser when the client does not specify a file name in a request.|  
  
## Remarks  
 For more information about the `files` element, see the following topic on the Microsoft IIS.net Web site: [Default Document Files \<files>](http://www.iis.net/ConfigReference/system.webServer/defaultDocument/files).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root level Web.config<br /><br /> Application level Web.config<br /><br /> Virtual or physical directory level Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-files-for-defaultdocument.md)   
 [\<clear>](../../reference/admin/clear-element-for-files.md)   
 [\<remove>](../../reference/admin/remove-element-for-files.md)