---
title: "serverRuntime Element for system.ftpServer | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: bef9d858-65a1-440a-86b2-0ea272436713
caps.latest.revision: 6
author: "shirhatti"
manager: "wpickett"
---
# serverRuntime Element for system.ftpServer
> [!NOTE]
>  For more information about the `serverRuntime` element, see the following topic on the Microsoft IIS.net Web site: [FTP Server Runtime \<serverRuntime>](http://www.iis.net/ConfigReference/system.ftpServer/serverRuntime).  
  
 Specifies settings that configure how the FTP service operates. More specifically, the `serverRuntime` element contains the `hostNameSupport` element, which lets you configure whether domain name syntax can be used to specify FTP virtual hosts.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`hostNameSupport`|Optional element.<br /><br /> Specifies whether domain name syntax for virtual host names is allowed.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.ftpServer`|Specifies configuration settings used by the FTP server engine and modules.|  
  
## Remarks  
 For more information about the `serverRuntime` element, see the following topic on the Microsoft IIS.net Web site: [FTP Server Runtime \<serverRuntime>](http://www.iis.net/ConfigReference/system.ftpServer/serverRuntime).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<hostNameSupport>](../../reference/admin/hostnamesupport-element-for-system-ftpserver.md)