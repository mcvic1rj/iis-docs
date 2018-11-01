---
title: "firewallSupport Element for system.ftpServer | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: a0d9b015-e127-4eb3-9a9b-e88911f55aba
caps.latest.revision: 7
author: "shirhatti"
manager: "wpickett"
---
# firewallSupport Element for system.ftpServer
> [!NOTE]
>  For more information about the `firewallSupport` element, see the following topic on the Microsoft IIS.net Web site: [FTP Firewall Support \<firewallSupport>](http://www.iis.net/ConfigReference/system.ftpServer/firewallSupport).  
  
 Specifies the port range settings for passive connections to an FTP server.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`lowDataChannelPort`|Optional `int` attribute.Specifies the lowest port for data channel activity for passive data connections.The default value is 0.|  
|`highDataChannelPort`|Optional `int` attribute.Specifies the lowest port for data channel activity for passive data connections.The default value is 0.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.ftpServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
  
## Remarks  
 For more information about the `firewallSupport` element, see the following topic on the Microsoft IIS.net Web site: [FTP Firewall Support \<firewallSupport>](http://www.iis.net/ConfigReference/system.ftpServer/firewallSupport).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [IIS 7.0: system.ftpServer Section Group (IIS Settings Schema)](629e96dd-550c-4890-831c-4612d3febf38[GUID])