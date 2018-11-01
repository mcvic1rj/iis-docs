---
title: "requestFiltering Element for security | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 23af9c9d-50d3-4db8-918c-6214259aa59c
caps.latest.revision: 14
author: "shirhatti"
manager: "wpickett"
---
# requestFiltering Element for security
> [!NOTE]
>  For more information about the `RequestFiltering` element, see the following topic on the Microsoft IIS.net Web site: [Request Filtering \<requestFiltering>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering).  
  
 Specifies configuration settings for request filtering.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`allowDoubleEscaping`|Optional `Boolean` attribute.<br /><br /> Specifies whether to allow URLs with double escape characters.<br /><br /> The default value is `false`.|  
|`allowHighBitCharacters`|Optional `Boolean` attribute.<br /><br /> Specifies whether to allow non-ASCII characters in URLs.<br /><br /> The default value is `true`.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`fileExtensions`|Optional element.<br /><br /> Specifies which file name extensions are allowed or denied to limit types of requests sent to the Web server.|  
|`filteringRules`|Optional element.<br /><br /> Specifies a collection of custom request filtering rules. **Note:**  This element was added in IIS 7.5.|  
|`requestLimits`|Optional element.<br /><br /> Specifies limits on requests processed by the Web server.|  
|`verbs`|Optional element.<br /><br /> Specifies which HTTP verbs are allowed or denied to limit types of requests sent to the Web server.|  
|`hiddenSegments`|Optional element.<br /><br /> Specifies that certain segments of URLs can be made inaccessible to clients.|  
|`denyUrlSequences`|Optional element.<br /><br /> Specifies sequences that should be denied to help prevent URL-based attacks on the Web server.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
  
## Remarks  
 For more information about the `RequestFiltering` element, see the following topic on the Microsoft IIS.net Web site: [Request Filtering \<requestFiltering>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<fileExtensions>](../../reference/admin/fileextensions-element-for-requestfiltering.md)   
 [\<filteringRules>](../../reference/admin/filteringrules-element-for-requestfiltering-for-security.md)   
 [\<requestLimits>](../../reference/admin/requestlimits-element-for-requestfiltering.md)   
 [\<verbs>](../../reference/admin/verbs-element-for-requestfiltering.md)   
 [\<hiddenSegments>](../../reference/admin/hiddensegments-element-for-requestfiltering.md)   
 [\<denyUrlSequences>](../../reference/admin/denyurlsequences-element-for-requestfiltering.md)