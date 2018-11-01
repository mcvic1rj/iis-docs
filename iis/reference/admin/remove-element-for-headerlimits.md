---
title: "remove Element for headerLimits | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 1c584b81-f6e6-4b1a-aabb-59553401b385
caps.latest.revision: 11
author: "shirhatti"
manager: "wpickett"
---
# remove Element for headerLimits
> [!NOTE]
>  For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Header Limits \<headerLimits>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/requestLimits/headerLimits).  
  
 Removes a reference to an HTML header for a specific domain from the `headerLimits` collection.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`header`|Required `string` attribute.<br /><br /> Specifies the domain of the header.|  
|`sizeLimit`|Required `uint` attribute.<br /><br /> Specifies the maximum size of the request, in bytes. Setting the value to 0, effectively denies all headers from the domain.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
|`requestFiltering`|Specifies configuration settings for request filtering.|  
|`requestLimits`|Specifies limits on requests processed by the Web server.|  
|`headerLimits`|Specifies size limits for HTML headers.|  
  
## Remarks  
 For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Header Limits \<headerLimits>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/requestLimits/headerLimits).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|