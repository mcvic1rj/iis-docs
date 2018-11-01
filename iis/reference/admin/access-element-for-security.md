---
title: "access Element for security | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 21a3e756-084d-45cc-b678-03e1b45d23e6
caps.latest.revision: 16
author: "shirhatti"
manager: "wpickett"
---
# access Element for security
> [!NOTE]
>  For more information about the `access` element, see the following topic on the Microsoft IIS.net Web site: [Access Security \<access>](http://www.iis.net/ConfigReference/system.webServer/security/access).  
  
 Specifies configuration settings for Secure Sockets Layer (SSL). Based upon their use of client certificates, these settings determine authentication and crypto strength.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`sslFlags`|Optional `enum` attribute.<br /><br /> The `sslFlags` attribute can be one of the following possible values. The default is None.<br /><br /> None:<br /><br /> - Disable SSL. The numeric value is 0.<br /><br /> Ssl:<br /><br /> - Require SSL. The numeric value is 8.<br /><br /> SslNegotiateCert:<br /><br /> - Accept client certificates for authentication. The numeric value is 32.<br /><br /> SslRequireCert:<br /><br /> - Require clients certificates for authentication. The numeric value is 64.<br /><br /> Ssl128:<br /><br /> - Require 128-bit SSL. The numeric value is 256.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
  
## Remarks  
 For more information about the `access` element, see the following topic on the Microsoft IIS.net Web site: [Access Security \<access>](http://www.iis.net/ConfigReference/system.webServer/security/access).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|