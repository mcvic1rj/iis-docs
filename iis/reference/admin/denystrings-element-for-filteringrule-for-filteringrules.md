---
title: "denyStrings Element for filteringRule for filteringRules | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 4b1bcbb8-16a2-49ef-b73b-ba593b03be1b
caps.latest.revision: 6
author: "shirhatti"
manager: "wpickett"
---
# denyStrings Element for filteringRule for filteringRules
> [!NOTE]
>  For more information about the `denyStrings` element, see the following topic on the Microsoft IIS.net Web site: [Deny Strings for Filtering Rules \<denyStrings>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/filteringRules/filteringRule/denyStrings).  
  
 Defines a collection of strings for which a request filtering rule applies.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a unique string to the collection of strings which a request filtering rule will deny.|  
|`clear`|Optional element.<br /><br /> Clears the collection of strings which a request filtering rule will deny.|  
|`remove`|Optional element.<br /><br /> Removes a unique string from the collection of strings which a request filtering rule will deny.|  
  
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
 For more information about the `denyStrings` element, see the following topic on the Microsoft IIS.net Web site: [Deny Strings for Filtering Rules \<denyStrings>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/filteringRules/filteringRule/denyStrings).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-denystrings-for-filteringrule.md)