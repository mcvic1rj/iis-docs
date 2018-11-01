---
title: "hiddenSegments Element for requestFiltering | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 53220290-f0dd-4809-aebb-4fe76e7e3ef1
caps.latest.revision: 16
author: "shirhatti"
manager: "wpickett"
---
# hiddenSegments Element for requestFiltering
> [!NOTE]
>  For more information about the `hiddenSegments` element, see the following topic on the Microsoft IIS.net Web site: [Hidden Segments \<hiddenSegments>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/hiddenSegments).  
  
 Specifies that certain segments of URLs can be made inaccessible to clients.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`applyToWebDAV`|Optional `Boolean` attribute.<br /><br /> Specifies whether these settings should also apply to WebDAV requests.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a segment to the collection of hidden segments.|  
|`remove`|Optional element.<br /><br /> Removes a reference to a segment from the `hiddenSegments` collection.|  
|`clear`|Optional element.<br /><br /> Removes all references to segments from the `hiddenSegments` collection.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
|`requestFiltering`|Specifies configuration settings for request filtering.|  
  
## Remarks  
 For more information about the `hiddenSegments` element, see the following topic on the Microsoft IIS.net Web site: [Hidden Segments \<hiddenSegments>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/hiddenSegments).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-hiddensegments-for-requestfiltering.md)   
 [\<remove>](../../reference/admin/remove-element-for-hiddensegments-for-requestfiltering.md)   
 [\<clear>](../../reference/admin/clear-element-for-hiddensegments-for-requestfiltering.md)