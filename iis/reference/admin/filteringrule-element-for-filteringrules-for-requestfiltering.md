---
title: "filteringRule Element for filteringRules for requestFiltering | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: daf31353-55dd-4602-ae9f-c9d075b47757
caps.latest.revision: 5
author: "shirhatti"
manager: "wpickett"
---
# filteringRule Element for filteringRules for requestFiltering
> [!NOTE]
>  For more information about the `filteringRule` element, see the following topic on the Microsoft IIS.net Web site: [Request Filtering Rule \<filteringRule>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/filteringRules/filteringRule).  
  
 Adds a rule to the collection of custom request filtering rules.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`denyUnescapedPercent`|Optional `Boolean` attribute.<br /><br /> `true` if request filtering should deny the request if it contains percent symbols that are not escaped; otherwise, `false`.<br /><br /> The default value is `true`.|  
|`name`|Required `string` attribute.<br /><br /> Specifies the name of the request filtering rule.<br /><br /> There is no default value.|  
|`scanAllRaw`|Optional `Boolean` attribute.<br /><br /> `true` if request filtering should scan the raw headers for the strings that are specified in the `denyStrings` element; otherwise, `false`.<br /><br /> The default value is `false`.|  
|`scanQueryString`|Optional `Boolean` attribute.<br /><br /> `true` if request filtering should scan the query string for the strings that are specified in the `denyStrings` element; otherwise, `false`.<br /><br /> If the `unescapeQueryString` attribute of the `requestFiltering` element is set to `true`, then two scans will be made of the query string: one scan with the raw query string and a second scan with the query string unescaped.<br /><br /> The default value is `false`.|  
|`scanUrl`|Optional `Boolean` attribute.<br /><br /> `true` if request filtering should scan the URL for the strings that are specified in the `denyStrings` element; otherwise, `false`.<br /><br /> The default value is `false`.|  
  
### Child Elements  
  
|Element|Descriptio|  
|-------------|----------------|  
|`appliesTo`|Optional element.<br /><br /> Specifies the list of file name extensions to which the request filtering rule applies.|  
|`denyStrings`|Optional element.<br /><br /> Specifies the list of strings to deny for the request filtering rule.|  
|`scanHeaders`|Optional element.<br /><br /> Specifies the list of HTTP headers to scan.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
|`requestFiltering`|Specifies configuration settings for request filtering.|  
|`filteringRules`|Specifies a collection of custom request filtering rules.|  
  
## Remarks  
 For more information about the `filteringRule` element, see the following topic on the Microsoft IIS.net Web site: [Request Filtering Rule \<filteringRule>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/filteringRules/filteringRule).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<appliesTo>](../../reference/admin/appliesto-element-for-filteringrule-for-filteringrules.md)   
 [\<denyStrings>](../../reference/admin/denystrings-element-for-filteringrule-for-filteringrules.md)   
 [\<scanHeaders>](../../reference/admin/scanheaders-element-for-filteringrule-for-filteringrules.md)