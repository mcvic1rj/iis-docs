---
title: "system.ftpServer Section Group | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 629e96dd-550c-4890-831c-4612d3febf38
caps.latest.revision: 17
author: "shirhatti"
manager: "wpickett"
---
# system.ftpServer Section Group
> [!NOTE]
>  For more information about the `ftpServer` element, see the following topic on the Microsoft IIS.net Web site: [\<ftpServer>](http://www.iis.net/ConfigReference/system.ftpServer).  
  
 Specifies configuration settings used by the FTP server engine and modules.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`log`|Optional element.<br /><br /> Specifies log settings for an FTP server.|  
|`firewallSupport`|Optional element.<br /><br /> Specifies the external address of the firewall that is sent to clients when passive connections using PASV command are negotiated. PASV command responses contain the IP address and Port of the Web server. By default, the local IP address is returned.|  
|`providerDefinitions`|Optional element.<br /><br /> Contains custom provider settings for an FTP server.|  
|`Security`|Optional element.<br /><br /> Specifies security-related settings for an FTP server.|  
|`Caching`|Optional element.<br /><br /> Specifies the credential cache settings for the FTP service.|  
|`serverRuntime`|Optional element.<br /><br /> Specifies settings that configure how the FTP service operates.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
  
## Remarks  
 For more information about the `ftpServer` element, see the following topic on the Microsoft IIS.net Web site: [\<ftpServer>](http://www.iis.net/ConfigReference/system.ftpServer).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<log>](../../reference/admin/log-element-for-system-ftpserver.md)   
 [\<firewallSupport>](../../reference/admin/firewallsupport-element-for-system-ftpserver.md)   
 [\<providerDefinitiions>](../../reference/admin/providerdefinitions-element-for-system-ftpserver.md)   
 [\<security>](../../reference/admin/security-element-for-system-ftpserver.md)   
 [\<caching>](../../reference/admin/caching-element-for-system-ftpserver.md)   
 [\<serverRuntime>](../../reference/admin/serverruntime-element-for-system-ftpserver.md)