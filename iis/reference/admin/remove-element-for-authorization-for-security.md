---
title: "remove Element for authorization for security | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: f9797a89-8593-44e8-8702-22bcd039bffb
caps.latest.revision: 11
author: "shirhatti"
manager: "wpickett"
---
# remove Element for authorization for security
> [!NOTE]
>  For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Security Authorization \<authorization>](http://www.iis.net/ConfigReference/system.webServer/security/authorization).  
  
 Specifies removal of an authorization rule.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`roles`|Optional `string` attribute.<br /><br /> Specifies roles for an authorization rule.|  
|`users`|Optional `string` attribute.<br /><br /> Specifies users for an authorization rule.|  
|`verbs`|Optional `string` attribute.<br /><br /> Specifies verbs for an authorization rule.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
|`authorization`|Specifies authorization related settings.|  
  
## Remarks  
 For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Security Authorization \<authorization>](http://www.iis.net/ConfigReference/system.webServer/security/authorization).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|