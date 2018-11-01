---
title: "remove Element for files | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: fa0ef92c-c04b-441e-8523-bd21bba7a6df
caps.latest.revision: 18
author: "shirhatti"
manager: "wpickett"
---
# remove Element for files
> [!NOTE]
>  For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Default Document Files \<files>](http://www.iis.net/ConfigReference/system.webServer/defaultDocument/files/add).  
  
 Removes a file name from the list of default documents in the `files` collection.  
  
 IIS 7.0: configuration Element (IIS Settings Schema)  
IIS 7.0: system.webServer Section Group (IIS Settings Schema)  
IIS 7.0: defaultDocument Element (IIS Settings Schema)  
IIS 7.0: files Element for defaultDocument (IIS Settings Schema)  
IIS 7.0: remove Element for files (IIS Settings Schema)  
  
## Syntax  
  
```  
<remove   
   name="name of file"  
/>  
```  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`name`|Optional `string` attribute.<br /><br /> Specifies the file name to be removed from the collection.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the root element in ApplicationHost.config that is the top-level section group in which this element is defined.|  
|`files`|Specifies the file names that are configured as default documents.|  
  
## Remarks  
 For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Default Document Files \<files>](http://www.iis.net/ConfigReference/system.webServer/defaultDocument/files/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root level Web.config<br /><br /> Application level Web.config<br /><br /> Virtual or physical directory level Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|