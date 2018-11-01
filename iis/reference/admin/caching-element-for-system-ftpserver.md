---
title: "caching Element for system.ftpServer | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 6fc7622b-e900-4706-8eff-191d889ace5e
caps.latest.revision: 6
author: "shirhatti"
manager: "wpickett"
---
# caching Element for system.ftpServer
> [!NOTE]
>  For more information about the `caching` element, see the following topic on the Microsoft IIS.net Web site: [FTP Caching \<cache>](http://www.iis.net/ConfigReference/system.ftpServer/caching).  
  
 Specifies the credential settings for an FTP service.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|credentialsCache|Optional element.<br /><br /> Specifies the credential cache settings for the FTP service.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.ftpServer`|Specifies configuration settings used by the FTP server engine and modules.|  
  
## Remarks  
 For more information about the `caching` element, see the following topic on the Microsoft IIS.net Web site: [FTP Caching \<cache>](http://www.iis.net/ConfigReference/system.ftpServer/caching).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<credentialsCache>](../../reference/admin/credentialscache-element-for-system-ftpserver.md)