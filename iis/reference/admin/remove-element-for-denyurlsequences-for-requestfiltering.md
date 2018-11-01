---
title: "remove Element for denyUrlSequences for requestFiltering | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 56ca3a68-30a1-441b-9649-f70aedf49918
caps.latest.revision: 12
author: "shirhatti"
manager: "wpickett"
---
# remove Element for denyUrlSequences for requestFiltering
> [!NOTE]
>  For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Deny URL Sequences \<denyUrlSequences>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/denyUrlSequences).  
  
 Removes a reference to a sequence from the `denyUrlSequences` collection.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`Sequence`|Required `string` attribute.<br /><br /> Specifies sequences of characters in URLs that the Web server should never process to help prevent URL-based attacks on the Web server.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`Security`|Specifies the section group that contains security related sections.|  
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