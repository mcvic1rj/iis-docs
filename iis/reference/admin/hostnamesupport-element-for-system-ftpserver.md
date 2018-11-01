---
title: "hostNameSupport Element for system.ftpServer | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 5a6a1933-45f1-4cb3-ba7f-e77c7b210889
caps.latest.revision: 6
author: "shirhatti"
manager: "wpickett"
---
# hostNameSupport Element for system.ftpServer
> [!NOTE]
>  For more information about the `hostNameSupport` element, see the following topic on the Microsoft IIS.net Web site: [FTP Host Name Support \<hostHameSupport>](http://www.iis.net/ConfigReference/system.ftpServer/serverRuntime/hostNameSupport).  
  
 Specifies whether domain name syntax for virtual host names is allowed.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`useDomainNameAsHostName`|Optional `Boolean` attribute.<br /><br /> `true` if domain name syntax is supported for virtual host names; otherwise, `false`.<br /><br /> The default value is `false`.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.ftpServer`|Specifies configuration settings used by the FTP server engine and modules.|  
|`serverRuntime`|Specifies settings that configure how the FTP service operates.|  
  
## Remarks  
 For more information about the `hostNameSupport` element, see the following topic on the Microsoft IIS.net Web site: [FTP Host Name Support \<hostHameSupport>](http://www.iis.net/ConfigReference/system.ftpServer/serverRuntime/hostNameSupport).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<serverRuntime>](../../reference/admin/serverruntime-element-for-system-ftpserver.md)