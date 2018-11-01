---
title: "appliesTo Element for filteringRule for filteringRules | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: dae8b2f5-20ea-40c7-85df-2f0ff563d54c
caps.latest.revision: 6
author: "shirhatti"
manager: "wpickett"
---
# appliesTo Element for filteringRule for filteringRules
> [!NOTE]
>  For more information about the `appliesTo` element, see the following topic on the Microsoft IIS.net Web site: [File Name Extensions for Filtering Rules \<appliesTo>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/filteringRules/filteringRule/appliesTo).  
  
 Specifies the list of file name extensions to which the request filtering rule applies.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a file name extension to the list of file name extensions for a filtering rule.|  
|`clear`|Optional element.<br /><br /> Clears the list of file name extensions for a filtering rule.|  
|`remove`|Optional element.<br /><br /> Removes a file name extension from the list of file name extensions for a filtering rule.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
|`requestFiltering`|Specifies configuration settings for request filtering.|  
|`filteringRules`|Specifies a collection of custom request filtering rules which define request filtering behavior based on user-defined criteria.|  
|`filteringRule`|Adds a rule to the collection of custom request filtering rules.|  
  
## Remarks  
 For more information about the `appliesTo` element, see the following topic on the Microsoft IIS.net Web site: [File Name Extensions for Filtering Rules \<appliesTo>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/filteringRules/filteringRule/appliesTo).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-appliesto-for-filteringrule.md)