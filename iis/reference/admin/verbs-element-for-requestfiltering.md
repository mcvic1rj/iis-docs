---
title: "verbs Element for requestFiltering | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 66153b1d-1a5a-4f8d-8543-6ba8973c2ed2
caps.latest.revision: 14
author: "shirhatti"
manager: "wpickett"
---
# verbs Element for requestFiltering
> [!NOTE]
>  For more information about the `verbs` element, see the following topic on the Microsoft IIS.net Web site: [Verbs \<verbs>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/verbs).  
  
 Specifies which HTTP verbs are allowed or denied to limit types of requests sent to the Web server.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`allowUnlisted`|Optional `Boolean` attribute.<br /><br /> Specifies whether the Web server should process unlisted verbs. If you set this attribute to `true`, you must list all verbs you want to deny. If you set this attribute to `false`, you must list all verbs you want to allow.<br /><br /> The default value is `true`.|  
|`applyToWebDAV`|Optional `Boolean` attribute.<br /><br /> Specifies whether these settings should also apply to WebDAV requests.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a verb to the `verbs` collection.|  
|`remove`|Optional element.<br /><br /> Removes a reference to a verb from the `verbs` collection.|  
|`clear`|Optional element.<br /><br /> Removes all references to verbs from the `verbs` collection.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
|`requestFiltering`|Specifies configuration settings for request filtering.|  
  
## Remarks  
 For more information about the `verbs` element, see the following topic on the Microsoft IIS.net Web site: [Verbs \<verbs>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/verbs).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-verbs-for-requestfiltering.md)   
 [\<remove>](../../reference/admin/remove-element-for-verbs-for-requestfiltering.md)   
 [\<clear>](../../reference/admin/clear-element-for-verbs-for-requestfiltering.md)