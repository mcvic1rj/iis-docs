---
title: "add Element for verbs for requestFiltering | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 3369b523-dc9c-4179-b0be-9ab4c534c04b
caps.latest.revision: 11
author: "shirhatti"
manager: "wpickett"
---
# add Element for verbs for requestFiltering
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Verbs \<add>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/verbs/add).  
  
 Adds a verb to the collection of verbs.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`allowed`|Required `Boolean` attribute.<br /><br /> Specifies whether the verb is allowed or denied. `True` allows the Web server to process these verbs. `False` prevents the Web server from processing requests.<br /><br /> The default value is `true`.|  
|`verb`|Required `string` attribute.<br /><br /> Specifies the name of the verb to allow or deny.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
|`requestFiltering`|Specifies configuration settings for request filtering.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Verbs \<add>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/verbs/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|