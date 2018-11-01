---
title: "add Element for headerLimits | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: f9d90124-e1a7-44f3-8c80-8c39d550801d
caps.latest.revision: 11
author: "shirhatti"
manager: "wpickett"
---
# add Element for headerLimits
> [!NOTE]
>  For more information about the `headerLimits` element, see the following topic on the Microsoft IIS.net Web site: [Header Limits \<headerLimits>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/requestLimits/headerLimits).  
  
 Adds a limit for HTML headers for a specific domain to the `headerLimits` collection.  
  
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
 For more information about the `headerLimits` element, see the following topic on the Microsoft IIS.net Web site: [Header Limits \<headerLimits>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/requestLimits/headerLimits).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|