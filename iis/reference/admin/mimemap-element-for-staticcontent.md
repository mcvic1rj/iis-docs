---
title: "mimeMap Element for staticContent | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 419c2ecd-9739-478e-bd23-dde77f88419d
caps.latest.revision: 16
author: "shirhatti"
manager: "wpickett"
---
# mimeMap Element for staticContent
> [!NOTE]
>  For more information about the `mimeMap` element, see the following topic on the Microsoft IIS.net Web site: [Adding Static Content MIME Mappings \<mimeMap>](http://www.iis.net/ConfigReference/system.webServer/staticContent/mimeMap).  
  
 Specifies a list of the file name extensions for MIME mappings.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`fileExtension`|Required `string` attribute.<br /><br /> Specifies a unique file name extension for a MIME type.<br /><br /> See the Default Configuration section later in this topic for the complete list of default values.|  
|`mimeType`|Required `string` attribute.<br /><br /> Specifies the type of file and the application that uses this kind of file name extension.<br /><br /> See the Default Configuration section later in this topic for the complete list of default values.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`staticContent`|Configures static file request handler settings.|  
  
## Remarks  
 For more information about the `mimeMap` element, see the following topic on the Microsoft IIS.net Web site: [Adding Static Content MIME Mappings \<mimeMap>](http://www.iis.net/ConfigReference/system.webServer/staticContent/mimeMap).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|