---
title: "credentialsCache Element for system.ftpServer | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 8e18a9d0-b0fd-4269-832c-bd5b53d4672e
caps.latest.revision: 6
author: "shirhatti"
manager: "wpickett"
---
# credentialsCache Element for system.ftpServer
> [!NOTE]
>  For more information about the `credentialsCache` element, see the following topic on the Microsoft IIS.net Web site: [FTP Credentials Cache \<credentialsCache>](http://www.iis.net/ConfigReference/system.ftpServer/caching/credentialsCache).  
  
 Specifies the credential settings for the FTP service.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`enabled`|Optional `Boolean` attribute.<br /><br /> `true` if credential caching is enabled; otherwise, `false`.<br /><br /> The default value is true.|  
|`flushInterval`|Optional `uint` attribute.<br /><br /> Specifies the cache lifetime, in seconds, for credentials that are stored in the cache. **Note:**  This value must be between 5 and 604,800 seconds. <br /><br /> The default value is 900.|  
  
### Child Elements  
 None  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.ftpServer`|Specifies the top-level section group in which this element is defined.|  
|`caching`|Specifies the credential settings for an FTP service.|  
  
## Remarks  
 For more information about the `credentialsCache` element, see the following topic on the Microsoft IIS.net Web site: [FTP Credentials Cache \<credentialsCache>](http://www.iis.net/ConfigReference/system.ftpServer/caching/credentialsCache).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<caching>](../../reference/admin/caching-element-for-system-ftpserver.md)