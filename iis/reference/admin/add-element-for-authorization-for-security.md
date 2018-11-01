---
title: "add Element for authorization for security | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 194e2e97-09b6-447c-a438-62739e03b63d
caps.latest.revision: 13
author: "shirhatti"
manager: "wpickett"
---
# add Element for authorization for security
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Security Authorization \<add>](http://www.iis.net/ConfigReference/system.webServer/security/authorization/add).  
  
 Specifies Allow and Deny rules to be added for authorization.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`accessType`|Required `Enum` attribute.<br /><br /> The `accessType` attribute can be one of the following possible values.<br /><br /> Allow:<br /><br /> - Specifies a rule that allows authorization. The numeric value is 0.<br /><br /> Deny:<br /><br /> - Specifies a rule that denies authorization. The numeric value is 1.|  
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
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Security Authorization \<add>](http://www.iis.net/ConfigReference/system.webServer/security/authorization/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|