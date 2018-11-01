---
title: "centralW3CLogFile Element for log | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: d1c1626f-d845-4647-be3b-23d3a006114e
caps.latest.revision: 29
author: "shirhatti"
manager: "wpickett"
---
# centralW3CLogFile Element for log
> [!NOTE]
>  For more information about the `centralW3CLogFile` element, see the following topic on the Microsoft IIS.net Web site: [Central W3C Log File \<centralW3CLogFile>](http://www.iis.net/ConfigReference/system.applicationHost/log/centralW3CLogFile).  
  
 Specifies the central W3C log settings for all sites on a server.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`directory`|Optional `string` attribute.<br /><br /> Specifies the directory where log entries are written.<br /><br /> The default value is "%SystemDrive%\inetpub\logs\LogFiles".|  
|`enabled`|Optional `Boolean` attribute.<br /><br /> Specifies whether central W3C logging is enabled.<br /><br /> The default value is `true`.|  
|`localTimeRollover`|Optional `Boolean` attribute.<br /><br /> Specifies whether a new log file is created based on local time or Coordinated Universal Time (UTC).<br /><br /> Note:<br /><br /> A value of `true` means the new log file is based on local time; `false` means it is based on UTC.<br /><br /> The default value is `talse`.|  
|`logExtFileFlags`|Optional `enum` attribute.<br /><br /> Specifies which fields to log.<br /><br /> The `logExtFileFlags` attribute can be one of the following values or a list of these values. The default is a list of these values: `Date`, `Time`, `ClientIP`, `UserName`, `SiteName`, `ServerIP`, `Method`, `UriStem`, `UriQuery`, `HttpStatus`, `Win32Status`, `ServerPort`, `UserAgent`, `HttpSubStatus`.<br /><br /> `Date`:<br /><br /> - The date on which the activity occurred. The numeric value is 1.<br /><br /> `Time`:<br /><br /> - The time, in Coordinated Universal Time (UTC), at which the activity occurred. The numeric value is 2.<br /><br /> `ClientIP`:<br /><br /> - The IP address of the client that made the request. The numeric value is 4.<br /><br /> `UserName`:<br /><br /> - The name of the authenticated user who accessed your server. Anonymous users are indicated by a hyphen. The numeric value is 8.<br /><br /> `SiteName`:<br /><br /> - The name of the server on which the log file entry was generated. The numeric value is 16.<br /><br /> `ComputerName`:<br /><br /> - The name of the computer from which the request was made. The numeric value is 32.<br /><br /> `ServerIP`:<br /><br /> - The IP address of the server on which the log file entry was generated. The numeric value is 64.<br /><br /> `Method`:<br /><br /> - The requested action, for example, a `GET` method. The numeric value is 128.<br /><br /> `UriStem`:<br /><br /> - The target of the action, for example, Default.htm. The numeric value is 256.<br /><br /> `UriQuery`:<br /><br /> - The query, if any, that the client was trying to perform. A Universal Resource Identifier (URI) query is necessary only for dynamic pages. The numeric value is 512.<br /><br /> `HttpStatus`:<br /><br /> - The HTTP status code. The numeric value is 1024.<br /><br /> `Win32Status`:<br /><br /> - The Windows status code. The numeric value is 2048.<br /><br /> `BytesSent`:<br /><br /> - The number of bytes that the server sent. The numeric value is 4096.<br /><br /> `BytesRecv`:<br /><br /> - The number of bytes that the server received. The numeric value is 8192.<br /><br /> `TimeTaken`:<br /><br /> - The time that the action took, in milliseconds. The numeric value is 16384.<br /><br /> `ServerPort`:<br /><br /> - The server port number that is configured for the service. The numeric value is 32768.<br /><br /> `UserAgent`:<br /><br /> - The browser type that the client used. The numeric value is 65536.<br /><br /> `Cookie`:<br /><br /> - The content of the cookie sent or received, if a cookie was sent or received. The numeric value is 131072.<br /><br /> `Referer` :<br /><br /> - The site that the user last visited. This site provided a link to the current site. The numeric value is 262144.<br /><br /> `ProtocolVersion`:<br /><br /> - The protocol version that the client used. The numeric value is 524288.<br /><br /> `Host`:<br /><br /> - The host header name, if there is a host header. The numeric value is 1048576.<br /><br /> `HttpSubStatus`:<br /><br /> - The substatus error code. The numeric value is 2097152.|  
|`period`|Optional `enum` attribute.<br /><br /> Specifies how frequently the current log file is closed and a new log file is started.<br /><br /> The `period` attribute can be one of the following possible values. The default is `false`.<br /><br /> `MaxSize`:<br /><br /> - Log files are cleared whenever the log file reaches the size specified by the `truncateSize` attribute. The numeric value is 0.<br /><br /> `Daily`:<br /><br /> - Log files are cleared every day. The numeric value is 1.<br /><br /> `Weekly`:<br /><br /> - Log files are cleared once a week. The numeric value is 2.<br /><br /> `Monthly`:<br /><br /> - Log files are cleared once a month. The numeric value is 3.<br /><br /> `Hourly`:<br /><br /> - Log files are cleared every hour. The numeric value is 4.|  
|`truncateSize`|Optional `int` attribute.<br /><br /> Specifies the size, in bytes, at which the log file contents will be truncated. This attribute must be set when the value of the `period` attribute is `maxSize`. The size must be between 1048576 (1 megabyte) and 4294967295 (4 gigabytes).<br /><br /> The default value is 20971520 (20 megabytes).|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`log`|Specifies the logging mode for a server.|  
  
## Remarks  
 For more information about the `centralW3CLogFile` element, see the following topic on the Microsoft IIS.net Web site: [Central W3C Log File \<centralW3CLogFile>](http://www.iis.net/ConfigReference/system.applicationHost/log/centralW3CLogFile).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<centralBinaryLogFile>](../../reference/admin/centralbinarylogfile-element-for-log.md)