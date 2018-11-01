---
title: "clientCertificateMappingAuthentication Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: afdf3f09-9529-48ae-8445-7aad2179fa3d
caps.latest.revision: 22
author: "shirhatti"
manager: "wpickett"
---
# clientCertificateMappingAuthentication Element
> [!NOTE]
>  For more information about the `basicAuthentication` element, see the following topic on the Microsoft IIS.net Web site: [Basic Authentication \<basicAuthentication>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/basicAuthentication).  
  
 Configures mapping for client certificates using Active Directory.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`enabled`|Optional `Boolean` attribute.<br /><br /> Specifies whether Client Certificate Mapping authentication using Active Directory is enabled. For this setting to take effect, you must set this attribute with [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)]. If you use any other method to set this attribute, you must restart the Web server for the setting to take effect.<br /><br /> The default value is `False`.|  
  
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
 For more information about the `basicAuthentication` element, see the following topic on the Microsoft IIS.net Web site: [Basic Authentication \<basicAuthentication>](http://www.iis.net/ConfigReference/system.webServer/security/authentication/basicAuthentication).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|