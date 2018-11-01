---
title: "ipSecurity Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: a78cf98a-a041-4c2c-911e-446b79da281d
caps.latest.revision: 24
author: "shirhatti"
manager: "wpickett"
---
# ipSecurity Element
> [!NOTE]
>  For more information about the `ipSecurity` element, see the following topic on the Microsoft IIS.net Web site: [IP Security \<ipSecurity>](http://www.iis.net/ConfigReference/system.webServer/security/ipSecurity).  
  
 Specifies access restrictions based on the IP version 4 address or DNS domain name.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`allowUnlisted`|Optional `Boolean` attribute.<br /><br /> Specifies whether to allow unlisted IP addresses. `True` allows an unlisted IP address to access the server. `False` locks down the server, preventing access to all IP address unless they are listed. If you were to set this attribute to `false` and not list the local loopback address (127.0.0.1) as an allowed IP address, you would not be able to access your server by using a browser from a local console.<br /><br /> This attribute can also affect delegation. If you were to set this attribute to `false` in a parent configuration, you would not be able use the <`clear`> element to clear this configuration in child configuration files.<br /><br /> The default value is true.|  
|`enableReverseDns`|Optional `Boolean` attribute.<br /><br /> Specifies whether to enable or disable reverse Domain Name System (DNS) lookups for the Web server. Reverse lookups involve looking up the domain name when the IP address is known. **Caution:**  Reverse DNS lookups will use significant resources and time. <br /><br /> The default value is `false`.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds an IP restriction to the collection of IP address restrictions.|  
|`remove`|Optional element.<br /><br /> Removes a reference to a restriction from the `ipSecurity` collection.|  
|`clear`|Optional element.<br /><br /> Removes all references to restrictions from the `ipSecurity` collection.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
  
## Remarks  
 For more information about the `ipSecurity` element, see the following topic on the Microsoft IIS.net Web site: [IP Security \<ipSecurity>](http://www.iis.net/ConfigReference/system.webServer/security/ipSecurity).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-ipsecurity.md)   
 [\<remove>](../../reference/admin/remove-element-for-ipsecurity.md)   
 [\<clear>](../../reference/admin/clear-element-for-ipsecurity.md)