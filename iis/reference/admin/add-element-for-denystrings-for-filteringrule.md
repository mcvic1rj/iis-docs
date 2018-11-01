---
title: "add Element for denyStrings for filteringRule | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 1ef958b1-8558-4f40-8ae0-ac7718dc5ace
caps.latest.revision: 6
author: "shirhatti"
manager: "wpickett"
---
# add Element for denyStrings for filteringRule
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Deny Strings for Filtering Rules \<add>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/filteringRules/filteringRule/denyStrings/add).  
  
 Adds a unique string to the collection of strings which a request filtering rule will deny.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`string`|Required `string` attribute.<br /><br /> Specifies a unique string which a request filtering rule will deny.<br /><br /> There is no default value.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
|`requestFiltering`|Specifies configuration settings for request filtering.|  
|`denyStrings`|Defines a collection of strings for which a request filtering rule applies.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Deny Strings for Filtering Rules \<add>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/filteringRules/filteringRule/denyStrings/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<denyStrings>](../../reference/admin/denystrings-element-for-filteringrule-for-filteringrules.md)