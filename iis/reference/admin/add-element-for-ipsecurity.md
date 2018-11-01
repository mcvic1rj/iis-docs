---
title: "add Element for ipSecurity | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 55350831-3ca9-4dae-acd7-a6ab9eae7174
caps.latest.revision: 18
author: "shirhatti"
manager: "wpickett"
---
# add Element for ipSecurity
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding IP Security \<add>](http://www.iis.net/ConfigReference/system.webServer/security/ipSecurity/add).  
  
 Adds an IP restriction to the collection of IP address restrictions.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`allowed`|Optional `Boolean` attribute.<br /><br /> Specifies whether to allow access to the address space.<br /><br /> The default value is `false`.|  
|`domainName`|Optional `string` attribute.<br /><br /> Specifies domain name on which to impose a restriction rule. You can use an asterisk (*) as a wildcard.|  
|`ipAddress`|Optional `string` attribute.<br /><br /> Specifies the IP version 4 address on which to impose a restriction rule.|  
|`subnetMask`|Optional `string` attribute.<br /><br /> Specifies the subnet mask with which to evaluate the IP address for this restriction rule. You can use a subnet mask to identify a range of IP addresses in an address space. The default value requires a direct match of the IP address being evaluated (effectively, a range of a single address).<br /><br /> The default value is 255.255.255.255.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
|`ipSecurity`|Specifies access restrictions based on IP version 4 address or DNS domain name.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding IP Security \<add>](http://www.iis.net/ConfigReference/system.webServer/security/ipSecurity/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|