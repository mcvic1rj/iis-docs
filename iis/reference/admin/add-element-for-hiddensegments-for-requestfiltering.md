---
title: "add Element for hiddenSegments for requestFiltering | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: ab078959-93c9-471b-9098-0aee93a50cd5
caps.latest.revision: 12
author: "shirhatti"
manager: "wpickett"
---
# add Element for hiddenSegments for requestFiltering
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Hidden Segments \<add>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/hiddenSegments/add).  
  
 Adds a segment to the collection of hidden segments.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`segment`|Required `string` attribute.<br /><br /> Specifies part of the file system that should never be served to clients.<br /><br /> See the Default Configuration section later in this topic for the complete list of default values.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
|`requestFiltering`|Specifies configuration settings for request filtering.|  
|`hiddenSegments`|Specifies that certain segments of URLs can be made inaccessible to clients.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Hidden Segments \<add>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/hiddenSegments/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|