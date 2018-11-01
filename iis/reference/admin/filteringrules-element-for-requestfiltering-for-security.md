---
title: "filteringRules Element for requestFiltering for security | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 91ccb3c3-0568-4794-bd74-3e4764b15b5c
caps.latest.revision: 6
author: "shirhatti"
manager: "wpickett"
---
# filteringRules Element for requestFiltering for security
> [!NOTE]
>  For more information about the `filteringRules` element, see the following topic on the Microsoft IIS.net Web site: [Request Filtering Rules \<filteringRules>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/filteringRules).  
  
 Specifies a collection of custom request filtering rules which define request filtering behavior based on user-defined criteria.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`filteringRule`|Optional element.<br /><br /> Adds a rule to the collection of custom request filtering rules.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
|`requestFiltering`|Specifies configuration settings for request filtering.|  
  
## Remarks  
 For more information about the `filteringRules` element, see the following topic on the Microsoft IIS.net Web site: [Request Filtering Rules \<filteringRules>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/filteringRules).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<filteringRule>](../../reference/admin/filteringrule-element-for-filteringrules-for-requestfiltering.md)