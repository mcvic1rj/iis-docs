---
title: "authorization Element for system.ftpServer | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 6aa3f219-6e70-4b50-8d8f-269f8dc93e56
caps.latest.revision: 7
author: "shirhatti"
manager: "wpickett"
---
# authorization Element for system.ftpServer
> [!NOTE]
>  For more information about the `authorization` element, see the following topic on the Microsoft IIS.net Web site: [FTP Authorization \<authorization>](http://www.iis.net/ConfigReference/system.ftpServer/security/authorization).  
  
 Specifies the resources that a user account can and cannot access on an FTP server.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
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
|`security`|Specifies security settings for an FTP server.|  
  
## Remarks  
 For more information about the `authorization` element, see the following topic on the Microsoft IIS.net Web site: [FTP Authorization \<authorization>](http://www.iis.net/ConfigReference/system.ftpServer/security/authorization).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-authorization-for-system-ftpserver.md)