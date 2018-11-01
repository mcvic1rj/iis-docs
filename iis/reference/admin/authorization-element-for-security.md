---
title: "authorization Element for security | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: a75f5aa1-164d-43f0-bd65-200b6c87750d
caps.latest.revision: 15
author: "shirhatti"
manager: "wpickett"
---
# authorization Element for security
> [!NOTE]
>  For more information about the `authorization` element, see the following topic on the Microsoft IIS.net Web site: [Security Authorization \<authorization>](http://www.iis.net/ConfigReference/system.webServer/security/authorization).  
  
 Specifies authorization-related settings.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`bypassLoginPages`|Optional `Boolean` attribute.<br /><br /> Specifies whether to skip authorization check for the page specified as the login page for Forms authentication. This enables unauthenticated users to access the login page to log on.<br /><br /> The default value is `True`.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds an authorization rule to the collection of authorization rules.|  
|`remove`|Optional element.<br /><br /> Removes a reference to an authorization rule to the collection of authorization rules.|  
|`clear`|Optional element.<br /><br /> Removes all references to authorization rules from the collection of authorization rules.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
  
## Remarks  
 For more information about the `authorization` element, see the following topic on the Microsoft IIS.net Web site: [Security Authorization \<authorization>](http://www.iis.net/ConfigReference/system.webServer/security/authorization).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-authorization-for-security.md)   
 [\<remove>](../../reference/admin/remove-element-for-authorization-for-security.md)   
 [\<clear>](../../reference/admin/clear-element-for-authorization-for-security.md)