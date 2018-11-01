---
title: "ipSecurity Element for system.ftpServer | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: b721cce5-67d6-4aac-a5fb-c2fb39051a7a
caps.latest.revision: 7
author: "shirhatti"
manager: "wpickett"
---
# ipSecurity Element for system.ftpServer
> [!NOTE]
>  For more information about the `ipSecurity` element, see the following topic on the Microsoft IIS.net Web site: [FTP IP Security \<ipSecurity>](http://www.iis.net/ConfigReference/system.ftpServer/security/ipSecurity).  
  
 Defines a list of IP-based security restrictions in FTP 7. These restrictions can be based on the IP version 4 address, a range of IP version 4 addresses, or a DNS domain name.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`allowUnlisted`|Optional `Boolean` attribute.<br /><br /> Specifies whether to allow unlisted IP addresses. Setting the `allowUnlisted` attribute to `true` allows an unlisted IP address to access the server. Setting the `allowUnlisted` attribute to `false` locks down the server, preventing access to all IP address unless they are listed. If you set this attribute to `false` and do not list the local loopback address (127.0.0.1) as an allowed IP address, you will not be able to access your server by using a browser from a local console.<br /><br /> The default value is `true`.|  
|`enableReverseDns`|Optional `Boolean` attribute.<br /><br /> Specifies whether to enable or disable reverse Domain Name System (DNS) lookups for the FTP server. Reverse lookups involve looking up the domain name when the IP address is known.<br /><br /> Caution: Reverse DNS lookups will use significant resources and time.<br /><br /> The default value is `false`.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds an IP restriction to the collection of IP address restrictions.|  
|`remove`|Optional element.<br /><br /> Removes a reference to a restriction from the ipSecurity collection.|  
|`clear`|Optional element.<br /><br /> Removes all references to restrictions from the ipSecurity collection.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.ftpServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the root element for configuring FTP server settings.|  
  
## Remarks  
 For more information about the `ipSecurity` element, see the following topic on the Microsoft IIS.net Web site: [FTP IP Security \<ipSecurity>](http://www.iis.net/ConfigReference/system.ftpServer/security/ipSecurity).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-ipsecurity-for-system-ftpserver.md)