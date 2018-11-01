---
title: "denyUrlSequences Element for requestFiltering | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 45d79b37-a7be-4525-a862-9170339092c4
caps.latest.revision: 16
author: "shirhatti"
manager: "wpickett"
---
# denyUrlSequences Element for requestFiltering
> [!NOTE]
>  For more information about the `denyUrlSequences` element, see the following topic on the Microsoft IIS.net Web site: [Deny URL Sequences \<denyUrlSequences>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/denyUrlSequences).  
  
 Specifies sequences that should be denied to help prevent URL-based attacks on the Web server.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a sequence to the collection of denied URL sequences.|  
|`remove`|Optional element.<br /><br /> Removes a reference to a sequence from the `denyUrlSequences` collection.|  
|`clear`|Optional element.<br /><br /> Removes all references to sequences from the `denyUrlSequences` collection.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
|`requestFiltering`|Specifies configuration settings for request filtering.|  
  
## Remarks  
 For more information about the `denyUrlSequences` element, see the following topic on the Microsoft IIS.net Web site: [Deny URL Sequences \<denyUrlSequences>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/denyUrlSequences).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-denyurlsequences-for-requestfiltering.md)   
 [\<remove>](../../reference/admin/remove-element-for-denyurlsequences-for-requestfiltering.md)   
 [\<clear>](../../reference/admin/clear-element-for-denyurlsequences-for-requestfiltering.md)