---
title: "add Element for appliesTo for filteringRule | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: ea49516f-3f8a-42e6-b1ec-3a12e29325dc
caps.latest.revision: 6
author: "shirhatti"
manager: "wpickett"
---
# add Element for appliesTo for filteringRule
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding File Name Extensions for Filtering Rules \<add>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/filteringRules/filteringRule/appliesTo/add).  
  
 Adds a unique file name extension to the collection of file name extensions to which a request filtering rule applies.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`fileExtension`|Required `string` attribute.<br /><br /> Specifies a unique file name extension to add to the list of file name extensions for a filtering rule.<br /><br /> There is no default value.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
|`requestFiltering`|Specifies configuration settings for request filtering.|  
|`filteringRules`|Specifies a collection of custom request filtering rules which define request filtering behavior based on user-defined criteria.|  
|`filteringRule`|Adds a rule to the collection of custom request filtering rules.|  
|`appliesTo`|Specifies the list of file name extensions to which the request filtering rule applies.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding File Name Extensions for Filtering Rules \<add>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/filteringRules/filteringRule/appliesTo/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<appliesTo>](../../reference/admin/appliesto-element-for-filteringrule-for-filteringrules.md)