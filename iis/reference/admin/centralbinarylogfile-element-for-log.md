---
title: "centralBinaryLogFile Element for log | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: a8c6fa5b-5240-4703-8217-7651395a40cd
caps.latest.revision: 26
author: "shirhatti"
manager: "wpickett"
---
# centralBinaryLogFile Element for log
> [!NOTE]
>  For more information about the `centralBinaryLogFile` element, see the following topic on the Microsoft IIS.net Web site: [Central Binary Log File \<centralBinaryLogFile>](http://www.iis.net/ConfigReference/system.applicationHost/log/centralBinaryLogFile).  
  
 Specifies the central binary log settings for all sites on a server.  
  
> [!NOTE]
>  Central logging must be enabled and `centralLogFileMode` must be set to `CentralBinary` for these settings to work.  For more information about `centralLogFileMode`, see [\<log>](../../reference/admin/log-element-for-system-applicationhost.md).  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`directory`|Optional `string` attribute.<br /><br /> Specifies the directory where log entries are written.|  
|`enabled`|Optional `Boolean` attribute.<br /><br /> Specifies whether central binary logging is enabled. Additionally, `centralLogFileMode` must be set to `CentralBinary` in order to fully enable central binary logging. For more information about `centralLogFileMode`, see [\<log>](../../reference/admin/log-element-for-system-applicationhost.md).<br /><br /> The default value is `false`.|  
|`localTimeRollover`|Optional `Boolean` attribute.<br /><br /> Specifies whether a new log file is created based on local time or Coordinated Universal Time (UTC).<br /><br /> The default value is `false`.|  
|`period`|Optional `enum` attribute.<br /><br /> Specifies how frequently the log file contents should be cleared.<br /><br /> The `period` attribute can be one of the following possible values.<br /><br /> The default value is `false`.<br /><br /> `MaxSize`:<br /><br /> - Log files are cleared whenever the log file reaches the size specified by the `truncateSize` attribute. The numeric value is 0.<br /><br /> `Daily`:<br /><br /> - Log files are cleared every day. The numeric value is 1.<br /><br /> `Weekly`:<br /><br /> - Log files are cleared once a week. The numeric value is 2.<br /><br /> `Monthly`:<br /><br /> - Log files are cleared once a month. The numeric value is 3.<br /><br /> `Hourly`:<br /><br /> - Log files are cleared every hour. The numeric value is 4.|  
|`truncateSize`|Optional `int` attribute.<br /><br /> Specifies the size at which the log file contents should be truncated. This attribute must be set when the value of the `period` attribute is `maxSize`. The size must be between 1048576 (1 megabyte) and 4294967295 (4 gigabytes).<br /><br /> The default value is 20971520 (20 megabytes).|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`log`|Specifies the logging mode for a server.|  
  
## Remarks  
 For more information about the `centralBinaryLogFile` element, see the following topic on the Microsoft IIS.net Web site: [Central Binary Log File \<centralBinaryLogFile>](http://www.iis.net/ConfigReference/system.applicationHost/log/centralBinaryLogFile).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<centralW3CLogFile>](../../reference/admin/centralw3clogfile-element-for-log.md)