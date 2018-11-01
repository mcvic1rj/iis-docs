---
title: "remove Element for verbs for requestFiltering | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: ce7fac64-1e55-4d93-abef-8006127fb9af
caps.latest.revision: 11
author: "shirhatti"
manager: "wpickett"
---
# remove Element for verbs for requestFiltering
> [!NOTE]
>  For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Verbs \<verbs>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/verbs).  
  
 Removes a reference to a verb from the `verbs` collection.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`allowed`|Required `Boolean` attribute.<br /><br /> Specifies whether the verb is allowed or denied. `True` allows the Web server to process these verbs. `False` prevents the Web server from processing requests.<br /><br /> The default value is `true`.|  
|`verbs`|Required `string` attribute.<br /><br /> Specifies the name of the verbs to allow or deny.|  
  
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
 For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Verbs \<verbs>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/verbs).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|