---
title: "digestAuthentication Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: ab0c0305-b77e-46c1-8209-93ae7ecaa515
caps.latest.revision: 18
author: "shirhatti"
manager: "wpickett"
---
# digestAuthentication Element
> [!NOTE]
>  For more information about the `digestAuthentication` element, see the following topic on the Microsoft IIS.net Web site: [Digest Authentication \<digestAuthentication>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/digestAuthentication).  
  
 Specifies Digest authentication configuration.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`enabled`|Optional `Boolean` attribute.<br /><br /> Specifies whether Digest authentication is enabled.<br /><br /> The default value is `False`.|  
|`realm`|Optional `String` attribute.<br /><br /> Specifies the realm for Digest authentication.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
|`authentication`|Specifies the section group that contains authentication sections.|  
  
## Remarks  
 For more information about the `digestAuthentication` element, see the following topic on the Microsoft IIS.net Web site: [Digest Authentication \<digestAuthentication>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/digestAuthentication).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|