---
title: "scope Element for authorizationRules for authorization | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 311168f8-1a01-42d7-926f-2205462a2bea
caps.latest.revision: 10
author: "shirhatti"
manager: "wpickett"
---
# scope Element for authorizationRules for authorization
> [!NOTE]
>  For more information about the `scope` element, see the following topic on the Microsoft IIS.net Web site: [Management Authorization Rules Scope \<scope>](http://www.iis.net/ConfigReference/system.webServer/management/authorization/authorizationRules/scope).  
  
 Configures the virtual path of the site or application to which [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] users and Windows users are authorized to connect by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`path`|Required `string` attribute.<br /><br /> Specifies the virtual path of a site or an application. [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] users and Windows users can then be added to the child `<add>` collection so they are authorized to connect to that site or application by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds an [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] user or Windows user or group to the collection of users who are authorized to connect to a site or an application by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in Administration.config) in which this element is defined.|  
|`management`|Configures a Web server for remote management by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
|`authorization`|Configures authorization settings for remote management of the Web server.|  
|`authorizationRules`|Configures the [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] users and Windows users who are authorized to connect to a site or an application by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
  
## Remarks  
 For more information about the `scope` element, see the following topic on the Microsoft IIS.net Web site: [Management Authorization Rules Scope \<scope>](http://www.iis.net/ConfigReference/system.webServer/management/authorization/authorizationRules/scope).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Root Administration.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-scope-for-authorizationrules-for-authorization.md)