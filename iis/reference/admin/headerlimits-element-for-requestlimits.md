---
title: "headerLimits Element for requestLimits | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 2efaa1de-3892-4055-9fb4-206f509877ed
caps.latest.revision: 13
author: "shirhatti"
manager: "wpickett"
---
# headerLimits Element for requestLimits
> [!NOTE]
>  For more information about the `headerLimits` element, see the following topic on the Microsoft IIS.net Web site: [Header Limits \<headerLimits>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/requestLimits/headerLimits).  
  
 Specifies size limits for HTML headers.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a limit for HTML headers for a specific domain to the `headerLimits` collection.|  
|`remove`|Optional element.<br /><br /> Removes a reference to an HTML header for a specific domain from the `headerLimits` collection.|  
|`clear`|Optional element.<br /><br /> Removes all references to HTML header from the `headerLimits` collection.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
|`requestFiltering`|Specifies configuration settings for request filtering.|  
|`requestLimits`|Specifies limits on requests processed by the Web server.|  
  
## Remarks  
 For more information about the `headerLimits` element, see the following topic on the Microsoft IIS.net Web site: [Header Limits \<headerLimits>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/requestLimits/headerLimits).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-headerlimits.md)   
 [\<remove>](../../reference/admin/remove-element-for-headerlimits.md)   
 [\<clear>](../../reference/admin/clear-element-for-headerlimits.md)