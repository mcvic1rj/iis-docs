---
title: "add Element for denyUrlSequences for requestFiltering | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 792efe34-ac17-44dc-bf02-073b0e56ca9d
caps.latest.revision: 12
author: "shirhatti"
manager: "wpickett"
---
# add Element for denyUrlSequences for requestFiltering
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding URL Sequences To Deny \<add>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/denyUrlSequences/add).  
  
 Adds a sequence to the collection of denied URL sequences.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`sequence`|Required `string` attribute.<br /><br /> Specifies sequences of characters in URLs that the Web server should never process to help prevent URL-based attacks on the Web server.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
|`requestFiltering`|Specifies configuration settings for request filtering.|  
|`denyUrlSequences`|Specifies sequences that should be denied to help prevent URL-based attacks on the Web server.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding URL Sequences To Deny \<add>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/denyUrlSequences/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|