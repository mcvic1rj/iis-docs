---
title: "authorizationRules Element for authorization | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 614bdc02-a65d-48f6-9c17-5df41667fc03
caps.latest.revision: 10
author: "shirhatti"
manager: "wpickett"
---
# authorizationRules Element for authorization
> [!NOTE]
>  For more information about the `authorizationRules` element, see the following topic on the Microsoft IIS.net Web site: [Management Authorization Rules \<authorizationRules>](http://www.iis.net/ConfigReference/system.webServer/management/authorization/authorizationRules).  
  
 Configures the [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] users and Windows users who are authorized to connect to a site or an application by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`scope`|Optional element.<br /><br /> Configures the virtual path of the site or application to which [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] users and Windows users are authorized to connect by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in Administration.config) in which this element is defined.|  
|`management`|Configures a Web server for remote management by using [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
|`authorization`|Configures authorization settings for remote management of the Web server.|  
  
## Remarks  
 For more information about the `authorizationRules` element, see the following topic on the Microsoft IIS.net Web site: [Management Authorization Rules \<authorizationRules>](http://www.iis.net/ConfigReference/system.webServer/management/authorization/authorizationRules).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Root Administration.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<scope>](../../reference/admin/scope-element-for-authorizationrules-for-authorization.md)