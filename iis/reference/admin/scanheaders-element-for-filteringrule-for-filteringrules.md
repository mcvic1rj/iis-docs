---
title: "scanHeaders Element for filteringRule for filteringRules | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 849ecd8d-929b-48f3-bd48-d44cf29c80bf
caps.latest.revision: 6
author: "shirhatti"
manager: "wpickett"
---
# scanHeaders Element for filteringRule for filteringRules
> [!NOTE]
>  For more information about the `scanHeaders` element, see the following topic on the Microsoft IIS.net Web site: [HTTP Headers for Filtering Rules \<scanHeaders>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/filteringRules/filteringRule/scanHeaders).  
  
 Defines a collection of HTTP headers that a request filtering rule will scan for strings that are specified in the `denyStrings` collection.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a unique HTTP header to the collection of HTTP headers which a request filtering rule will scan.|  
|`clear`|Optional element.<br /><br /> Clears the collection of HTTP headers which a request filtering rule will scan.|  
|`remove`|Optional element.<br /><br /> Removes a unique HTTP header from the collection of HTTP headers which a request filtering rule will scan.|  
  
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
 For more information about the `scanHeaders` element, see the following topic on the Microsoft IIS.net Web site: [HTTP Headers for Filtering Rules \<scanHeaders>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/filteringRules/filteringRule/scanHeaders).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-scanheaders-for-filteringrule.md)