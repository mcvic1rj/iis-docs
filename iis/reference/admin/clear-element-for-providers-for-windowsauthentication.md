---
title: "clear Element for providers for windowsAuthentication | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: baf5591b-2819-4cdf-9056-e44b8d4649d0
caps.latest.revision: 11
author: "shirhatti"
manager: "wpickett"
---
# clear Element for providers for windowsAuthentication
> [!NOTE]
>  For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [Windows Authentication Providers \<providers>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/windowsAuthentication/providers).  
  
 Clears security providers for Windows authentication from parent configuration files.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
|`authentication`|Specifies the section group that contains authentication sections.|  
|`windowsAuthentication`|Specifies Windows authentication configuration.|  
|`providers`|Specifies security support providers used for Windows authentication.|  
  
## Remarks  
 For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [Windows Authentication Providers \<providers>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/windowsAuthentication/providers).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|