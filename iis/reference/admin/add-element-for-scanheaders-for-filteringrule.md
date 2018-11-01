---
title: "add Element for scanHeaders for filteringRule | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 3ce16006-6425-4b0b-b930-689e84af28d7
caps.latest.revision: 6
author: "shirhatti"
manager: "wpickett"
---
# add Element for scanHeaders for filteringRule
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding HTTP Headers for Filtering Rules \<add>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/filteringRules/filteringRule/scanHeaders/add).  
  
 Adds a unique HTTP header to the collection of HTTP headers that a request filtering rule will scan for strings that are specified in the `denyStrings` collection.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`requestHeader`|Required `string` attribute.<br /><br /> Specifies a unique HTTP header to scan for a request filtering rule.<br /><br /> There is no default value.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
|`requestFiltering`|Specifies configuration settings for request filtering.|  
|`requestFiltering`|Specifies configuration settings for request filtering.|  
|`filteringRules`|Specifies a collection of custom request filtering rules which define request filtering behavior based on user-defined criteria.|  
|`filteringRule`|Adds a rule to the collection of custom request filtering rules.|  
|`scanHeaders`|Specifies the list of HTTP headers to scan.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding HTTP Headers for Filtering Rules \<add>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/filteringRules/filteringRule/scanHeaders/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<scanHeaders>](../../reference/admin/scanheaders-element-for-filteringrule-for-filteringrules.md)