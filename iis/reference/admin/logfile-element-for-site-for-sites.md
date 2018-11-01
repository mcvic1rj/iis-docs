---
title: "logFile Element for site for sites | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: ce782ec3-ce54-4402-ab91-c999bb486e26
caps.latest.revision: 21
author: "shirhatti"
manager: "wpickett"
---
# logFile Element for site for sites
> [!NOTE]
>  For more information about the `logFile` element, see the following topic on the Microsoft IIS.net Web site: [Log Files for a Web Site \<logFile>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/logFile).  
  
 Configures settings for handling and storage of log files for the site.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`customLogPluginClsid`|Optional `string` attribute.<br /><br /> Specifies the COM object class ID (CLSID) or IDs, in order of precedence, for custom modules.|  
|`directory`|Optional `string` attribute.<br /><br /> Specifies the logging directory, where the log file and logging-related support files are stored.<br /><br /> The default value is %systemdrive%\inetpub\logs\LogFiles.|  
|`enabled`|Optional `Boolean` attribute.<br /><br /> Specifies whether logging is enabled (`true`) or disabled (`false`) for a site.<br /><br /> Note:<br /><br /> ASP and ODBC errors are not logged in the IIS log files.<br /><br /> The default value is `true`.|  
|`localTimeRollover`|Optional `Boolean` attribute.<br /><br /> Specifies whether a new log file is created based on local time or Coordinated Universal Time (UTC), which was previously called Greenwich Mean Time (GMT). When `false`, a new log file is created based on UTC.<br /><br /> Note:<br /><br /> Regardless of the setting, the time stamp for each W3C Extended Logging log record is UTC-based.<br /><br /> The default value is `false`.|  
|`logExtFileFlags`|Optional `flags` attribute.<br /><br /> Specifies the categories of information that are written to either the log file (when you use W3C Extended log file format) or to the ODBC data source during logging events for a site.<br /><br /> The `logExtFileFlags` attribute can be one or more of the following values. If you specify more than one value, separate them with a comma (,). The default values are `Date`, `Time`, `ClientIP`, `UserName`, `ServerIP`, `Method`, `UriStem`, `UriQuery`, `HttpStatus`, `Win32Status`, `ServerPort`, `UserAgent`, `HttpSubStatus`.<br /><br /> `BytesRecv:` Log the number of bytes that the server received.<br /><br /> `BytesSent:` Log the number of bytes that the server sent.<br /><br /> `ClientIP:` Log the IP address of the client that made the request.<br /><br /> `ComputerName:` Log the name of the server on which the log file entry was generated.<br /><br /> `Cookie:` Log the content of the cookie sent or received, if any.<br /><br /> `Date:` Log the date on which the activity occurred.<br /><br /> `Host:` Log the host header name, if any.<br /><br /> `HttpStatus:` Log the HTTP status code.<br /><br /> `HttpSubStatus:` Log the sub-status code of the HTTP error. For example, for the 500.18 HTTP error, the status code is 500 and the sub-status code is 18.<br /><br /> `Method:` Log the requested action, for example, a `GET` method.<br /><br /> `ProtocolVersion:` Log the protocol version that the client used.<br /><br /> `Referer:` Log the site that the user last visited. This site provided a link to the current site.<br /><br /> `ServerIP:` Log the IP address of the server on which the log file entry was generated.<br /><br /> `ServerPort:` Log the server port number that is configured for the service.<br /><br /> `SiteName:` Log the Internet service name and instance number that was running on the client.<br /><br /> `Time:` Log the time in Coordinated Universal Time (UTC), at which the activity occurred.<br /><br /> `TimeTaken:` Log the length of time taken for a request to be completed. The time taken is recorded in milliseconds.<br /><br /> Note:<br /><br /> The client-request timestamp is initialized when HTTP.sys receives the first byte, but before HTTP.sys begins to parse the request. The client-request timestamp is stopped when the last IIS send completion occurs. Time taken does not reflect time across the network. The first request to the site shows a slightly longer time taken than other similar requests because HTTP.sys opens the log file that contains the first request.<br /><br /> `UriQuery:` Log the query, if any, that the client was trying to perform. A Universal Resource Identifier (URI) query is necessary only for dynamic pages, and usually consists of parameters passed to the URL by using the URL?Parameters format.<br /><br /> `UriStem:` Log the Universal Resource Identifier (URI) stem information, which is the target of the action such as Default.htm.<br /><br /> `UserAgent:` Log the browser type that the client used.<br /><br /> `UserName:` Log the name of the authenticated user who accessed your server. Anonymous users are indicated by a hyphen.<br /><br /> `Win32Status:` Log the Windows status code.|  
|`logFormat`|Optional `enum` attribute.<br /><br /> Specifies the log file format.<br /><br /> The `logFormat` attribute can be one of the following values. The default value is `W3C`.<br /><br /> `Custom:` Use a custom log file format for a custom logging module.<br /><br /> The numeric value is 3.<br /><br /> `IIS:` Use the Microsoft IIS log file format to log information about a site. This format is handled by HTTP.sys, and is a *fixed* ASCII text-based format, which means that you cannot customize the fields that are logged. Fields are separated by commas, and time is recorded as local time.<br /><br /> The following list is a list of fields that are logged when you use the IIS log file format:<br /><br /> - `Client IP address`<br /><br /> - `User name`<br /><br /> - `Date`<br /><br /> - `Time`<br /><br /> - `Service and instance`<br /><br /> - `Server name`<br /><br /> - `Server IP address`<br /><br /> - `Time taken`<br /><br /> - `Client bytes sent`<br /><br /> - `Server bytes sent`<br /><br /> - `Service status code` (A value of 200 indicates that the request was fulfilled successfully.)<br /><br /> - `Windows status code` (A value of 0 indicates that the request was fulfilled successfully.)<br /><br /> - `Request type`<br /><br /> - `Target of operation`<br /><br /> - `Parameters` (the parameters that are passed to a script)<br /><br /> Not all fields will contain data. When a field does not contain data, a hyphen (-) appears as a placeholder. When a field contains a non-printable character, HTTP.sys replaces it with a plus sign (+) to preserve the log file format.<br /><br /> The numeric value is 0.<br /><br /> `NCSA:` Use the National Center for Supercomputing Applications (NCSA) Common log file format to log information about a site. This format is handled by HTTP.sys, and is a *fixed* ASCII text-based format, which means that you cannot customize the fields that are logged. Fields are separated by spaces, and time is recorded as local time with the Coordinated Universal Time (UTC) offset.<br /><br /> The following list is a list of fields that are logged when you use the NCSA Common log file format:<br /><br /> - `Remote host address`<br /><br /> - `Remote log name` (This value is always a hyphen.)<br /><br /> - `User name`<br /><br /> - `Date, time, and UTC offset`<br /><br /> -                             `Request and protocol version`<br /><br /> -                             `Service status code` (A value of 200 indicates that the request was fulfilled successfully.)<br /><br /> - `Bytes sent`<br /><br /> Not all fields will contain data. When a field does not contain data, a hyphen (-) appears as a placeholder. When a field contains a non-printable character, HTTP.sys replaces it with a plus sign (+) to preserve the log file format.<br /><br /> The numeric value is 1.<br /><br /> `W3C:` Use the W3C Extended log file format to log information about a site. This format is handled by HTTP.sys, and is a *customizable* ASCII text-based format, which means that you specify the fields that are logged. Specify the fields that are logged in the `logExtFileFlags` attribute. Fields are separated by spaces, and time is recorded in Coordinated Universal Time (UTC).<br /><br /> The numeric value is 2.|  
|`period`|Optional `enum` attribute.<br /><br /> Specifies how often IIS creates a new log file.<br /><br /> The `period` attribute can be one of the following possible values. The default value is `Daily`.<br /><br /> `Daily`<br /><br /> - Create a new log file daily.<br /><br /> - The numeric value is 1.<br /><br /> `Hourly`<br /><br /> - Create a new log file hourly.<br /><br /> - The numeric value is 4.<br /><br /> `MaxSize`<br /><br /> - Create a new log file when a maximum size is reached. The maximum size is specified in the `truncateSize` attribute.<br /><br /> - The numeric value is 0.<br /><br /> `Monthly`<br /><br /> - Create a new log file monthly.<br /><br /> - The numeric value is 3.<br /><br /> `Weekly`<br /><br /> - Create a new log file weekly.<br /><br /> - The numeric value is 2.|  
|`truncateSize`|Optional `int64` attribute.<br /><br /> Specifies the maximum size of the log file (in bytes) after which to create a new log file. This value is only applicable when `MaxSize` is chosen for the `period` attribute.<br /><br /> The minimum file size is 131,072 bytes. If this attribute is set to a value less than 131,072 bytes, the default value is implicitly assumed as 131,072 bytes.<br /><br /> The default value is 20971520.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.applicationHost`|Specifies the root element for configuring Web process settings.|  
|`sites`|Specifies configuration settings for all sites on the server, and includes settings for applications and virtual directories in those sites.|  
|`site`|Specifies configuration settings for a site.|  
  
## Remarks  
 For more information about the `logFile` element, see the following topic on the Microsoft IIS.net Web site: [Log Files for a Web Site \<logFile>](http://www.iis.net/ConfigReference/system.applicationHost/sites/site/logFile).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|