---
title: "remove for staticContent Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: ee54436d-eac8-4744-85fc-05b71415ac61
caps.latest.revision: 11
author: "shirhatti"
manager: "wpickett"
---
# remove for staticContent Element
> [!NOTE]
>  For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Static Content \<staticContent>](http://www.iis.net/ConfigReference/system.webServer/staticContent).  
  
 Removes a single MIME mapping.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`fileExtension`|Required `string` attribute.<br /><br /> Specifies a unique file name extension for a MIME type.<br /><br /> See the following Default Configuration section for the complete list of default values.|  
|`mimeType`|Required `string` attribute.<br /><br /> Specifies the type of file and the application that uses this type of file name extension.<br /><br /> See the following Default Configuration section for the complete list of default values.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`staticContent`|Configures static file request handler settings.|  
  
## Remarks  
 For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Static Content \<staticContent>](http://www.iis.net/ConfigReference/system.webServer/staticContent).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|