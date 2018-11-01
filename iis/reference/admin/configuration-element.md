---
title: "configuration Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: e2c8d8d4-a787-4302-8ee5-2613aa76490e
caps.latest.revision: 20
author: "shirhatti"
manager: "wpickett"
---
# configuration Element
> [!NOTE]
>  For more information about the `configuration` element, see the following topic on the Microsoft IIS.net Web site: [IIS 7 Configuration Reference](http://www.iis.net/ConfigReference).  
  
 Specifies the root element in every configuration file. This element must appear first and last in every configuration file.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`system.applicationHost`|Contains configuration settings for the Web services process model.|  
|`system.ftpServer`|Contains global and URL level configuration settings for the FTP service.|  
|`system.webServer`|Contains configuration settings for a Web server that is running [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`administrators`|This has been deprecated. Do not use.|  
|`administratorProviders`|This has been deprecated. Do not use.|  
|`configPaths`|Lists the locations where a configuration setting is set across the distributed configuration file system.|  
|`configurationRedirection`|Shares IIS configuration files and encryption keys between one or more IIS servers.|  
|`modules`|Configures modules for [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)]. The `<modules>` list specifies the features that are available in [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)] when a user is connected to a site or an application.|  
|`moduleProviders`|Configures module providers for [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)]. A module provider contains the registration information for a module and determines whether a module can run in [!INCLUDE[iismgr](../../reference/admin/includes/iismgr-md.md)].|  
  
### Parent Elements  
 None.  
  
## Remarks  
 There must be one `configuration` element in every applicationHost.config file.  
  
 For more information about the `configuration` element, see the following topic on the Microsoft IIS.net Web site: [IIS 7 Configuration Reference](http://www.iis.net/ConfigReference).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<system.applicationHost>](../../reference/admin/system-applicationhost-section-group.md)   
 [\<system.ftpServer>](../../reference/admin/system-ftpserver-section-group.md)   
 [\<system.webServer>](../../reference/admin/system-webserver-section-group.md)