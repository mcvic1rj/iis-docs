---
title: "security Element for system.ftpServer | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 796753f6-1782-4292-b10b-d29f805c198a
caps.latest.revision: 6
author: "shirhatti"
manager: "wpickett"
---
# security Element for system.ftpServer
> [!NOTE]
>  For more information about the `security` element, see the following topic on the Microsoft IIS.net Web site: [FTP Security \<security>](http://www.iis.net/ConfigReference/system.ftpServer/security).  
  
 Specifies security settings for an FTP server.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
 None  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`authorization`|Optional element.<br /><br /> Specifies authorization-related settings.|  
|`ipSecurity`|Optional element.<br /><br /> Specifies access restrictions based on the IP version 4 address or DNS domain name.|  
|`requestFiltering`|Optional element.<br /><br /> Specifies configuration settings for request filtering.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.ftpServer`|Specifies the top-level section group in which this element is defined.|  
  
## Remarks  
 For more information about the `security` element, see the following topic on the Microsoft IIS.net Web site: [FTP Security \<security>](http://www.iis.net/ConfigReference/system.ftpServer/security).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<authorization>](../../reference/admin/authorization-element-for-system-ftpserver.md)   
 [\<ipSecurity>](../../reference/admin/ipsecurity-element-for-system-ftpserver.md)   
 [\<requestFiltering>](../../reference/admin/requestfiltering-element-for-system-ftpserver.md)