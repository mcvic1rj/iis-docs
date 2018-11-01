---
title: "log Element for system.applicationHost | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 9127b3e4-9be8-458d-9f5a-049a0ad4f4e4
caps.latest.revision: 28
author: "shirhatti"
manager: "wpickett"
---
# log Element for system.applicationHost
> [!NOTE]
>  For more information about the `log` element, see the following topic on the Microsoft IIS.net Web site: [Log \<log>](http://www.iis.net/ConfigReference/system.applicationHost/log).  
  
 Specifies the logging mode for a server.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`centralLogFileMode`|Optional `enum` attribute.<br /><br /> Specifies the central logging mode for the server.<br /><br /> The `centralLogFileMode` attribute can be one of the following possible values.<br /><br /> The default is `Site`.<br /><br /> `Site`:<br /><br /> - Configures all sites to use site logging instead of central logging. This is the default setting. The numerical value is 0.<br /><br /> `CentralBinary`:<br /><br /> - Creates one log file for all Web sites on a Web server. The data in the log file is binary-based, unformatted data that is not customizable. The numerical value is 1.<br /><br /> `CentralW3C`:<br /><br /> - Logs requests for all sites on a Web server to a single central log file in a text-based, customizable ASCII format. The numerical value is 2.|  
|`logInUTF8`|Optional `Boolean` attribute.<br /><br /> Specifies whether IIS should log all strings in UCS Transformation Format 8 (UTF-8). This setting applies to all text-mode logging server-wide.<br /><br /> The default value is `true`.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`centralBinaryLogFile`|Optional element.<br /><br /> Specifies the central binary log settings for all sites on a server.|  
|`centralW3CLogFile`|Optional element.<br /><br /> Specifies the central W3C log settings for all sites on a server.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
  
## Remarks  
 For more information about the `log` element, see the following topic on the Microsoft IIS.net Web site: [Log \<log>](http://www.iis.net/ConfigReference/system.applicationHost/log).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<centralBinaryLogFile>](../../reference/admin/centralbinarylogfile-element-for-log.md)   
 [\<centralW3CLogFile>](../../reference/admin/centralw3clogfile-element-for-log.md)