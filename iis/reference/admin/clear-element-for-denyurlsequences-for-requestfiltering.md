---
title: "clear Element for denyUrlSequences for requestFiltering | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 4aee81ac-7c19-4013-a10b-31ccb3a4ed94
caps.latest.revision: 12
author: "shirhatti"
manager: "wpickett"
---
# clear Element for denyUrlSequences for requestFiltering
> [!NOTE]
>  For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Deny URL Sequences \<denyUrlSequences>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/denyUrlSequences).  
  
 Removes all references to sequences from the denyUrlSequences collection.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
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
 For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Deny URL Sequences \<denyUrlSequences>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/denyUrlSequences).  
  
## Default Configuration  
 None.  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|