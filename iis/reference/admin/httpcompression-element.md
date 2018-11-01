---
title: "httpCompression Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 82ee89fa-8c3f-404f-b5e5-63008a536797
caps.latest.revision: 36
author: "shirhatti"
manager: "wpickett"
---
# httpCompression Element
> [!NOTE]
>  For more information about the `httpCompression` element, see the following topic on the Microsoft IIS.net Web site: [HTTP Compression \<httpCompression>](http://www.iis.net/ConfigReference/system.webServer/httpCompression).  
  
 Configures HTTP compression settings for a Web server.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`cacheControlHeader`|Optional `string` attribute.<br /><br /> Specifies the directive that IIS adds to the `Cache-Control` header that overrides the `HTTP Expires` header. This attribute ensures that older clients and proxy servers do not attempt to cache compressed files. To enable this setting, you must set the `sendCacheHeaders` attribute to `true`. The WWW service must be restarted before changes to this property take effect.<br /><br /> The default value is "max-age=86400".|  
|`directory`|Optional `string` attribute.<br /><br /> Specifies the directory where compressed versions of static files are temporarily stored and cached.<br /><br /> The default value is "%SystemDrive%\inetpub\temp\IIS Temporary Compressed Files". **Note:**  In IIS 6.0, the default directory path for IIS temporary compressed files was "%Windir%\IIS Temporary Compressed Files".|  
|`doDiskSpaceLimiting`|Optional `Boolean` attribute.<br /><br /> Specifies whether a limit exists for the amount of disk space that all compressed files, which are stored in the compression directory specified by the `directory` attribute, can occupy.<br /><br /> The default value is `true`.|  
|`dynamicCompressionDisableCpuUsage`|Optional `integer` attribute.<br /><br /> Specifies the percentage of CPU utilization at which dynamic compression will be disabled. **Note:**  This attribute acts as an upper CPU limit at which dynamic compression is turned off. When CPU utilization falls below the value specified in the `dynamicCompressionEnableCpuUsage` attribute, dynamic compression will be reenabled. <br /><br /> The default value is 90.|  
|`dynamicCompressionEnableCpuUsage`|Optional `integer` attribute.<br /><br /> Specifies the percentage of CPU utilization below which dynamic compression will be enabled. The value must be between 0 and 100. Average CPU utilization is calculated every 30 seconds. **Note:**  This attribute acts as a lower CPU limit below which dynamic compression is turned on. When CPU utilization rises above the value specified in the `dynamicCompressionDisableCpuUsage` attribute, dynamic compression will be disabled. <br /><br /> The default value is 50.|  
|`expiresHeader`|Optional `string` attribute.<br /><br /> Specifies the content of the `HTTP Expires` header that is sent with all requested compressed files, together with the `Cache-Control` header specified in the `cacheControlHeader` attribute. This combination of headers ensures that older clients and proxy servers do not try to cache compressed files. To enable this setting, you must set the `sendCacheHeaders` attribute to `true`. The World Wide Web Publishing Service (WWW service) must be restarted before changes to this property take effect.<br /><br /> The default value is "Wed, 01 Jan 1997 12:00:00 GMT".|  
|`maxDiskSpaceUsage`|Optional `integer` attribute.<br /><br /> Specifies the number of megabytes of disk space that compressed files can occupy in the compression directory. When the space used by compressed files exceeds 90 percent of the value in this attribute, IIS deletes the least recently used files until a 90-percent usage level is reached. **Note:**  In IIS 6.0, this limit is expressed in bytes; in IIS 7.0, it is expressed in megabytes. In IIS 7.0 the limit is applied per application pool. <br /><br /> The default value is 100.|  
|`minFileSizeForComp`|Optional `integer` attribute.<br /><br /> Specifies the minimum number of kilobytes a file must contain in order to use on-demand compression.<br /><br /> The default value is 256.|  
|`noCompressionForHttp10`|Optional `Boolean` attribute.<br /><br /> Specifies whether compression is disabled for requests that contain an HTTP 1.0 version number. **Note:**  Some HTTP 1.0 clients do not handle the caching of compressed objects correctly. You can use this setting to avoid returning a compressed file to a client that cannot decompress it. <br /><br /> The default value is `true`.|  
|`noCompressionForProxies`|Optional `Boolean` attribute.<br /><br /> Specifies whether the HTTP 1.1 response is disabled for compression requests that come through proxy servers. **Note:**  Some HTTP proxy servers do not handle the caching of compressed objects correctly. You can use this setting to avoid returning a compressed file to a proxy server that cannot decompress it. <br /><br /> The default value is `true`.|  
|`noCompressionForRange`|Optional `Boolean` attribute.<br /><br /> Specifies whether compression is disabled for HTTP requests that include the Range header. **Note:**  Some clients cannot handle range requests correctly. You can use this setting to avoid returning a compressed file to a client that cannot decompress it. <br /><br /> The default value is `true`.|  
|`sendCacheHeaders`|Optional `Boolean` attribute.<br /><br /> Specifies whether the headers configured in `cacheControlHeader` and `expiresHeader` are sent with each compressed response.<br /><br /> The default value is `false`.|  
|`staticCompressionDisableCpuUsage`|Optional `integer` attribute.<br /><br /> Specifies the percentage of CPU utilization at which static compression is disabled. The value must be between 0 and 100. Average CPU utilization is calculated every 30 seconds. **Note:**  This property acts as an upper CPU limit at which static compression is turned off. When CPU utilization falls below the value specified in the `staticCompressionEnableCpuUsage` attribute, static compression will be reenabled. <br /><br /> The default value is 100.|  
|`staticCompressionEnableCpuUsage`|Optional `integer` attribute.<br /><br /> Specifies the percentage of CPU utilization at which static compression is enabled. The value must be between 0 and 100. Average CPU utilization is calculated every 30 seconds. **Note:**  This property acts as a lower CPU limit below which static compression is turned on. When CPU utilization rises above the value specified in the `staticCompressionDisableCpuUsage` attribute, static compression will be disabled. <br /><br /> The default value is 50.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`scheme`|Optional element.<br /><br /> Specifies the compression scheme (Gzip or Deflate) IIS uses to compress client requests.|  
|`dynamicTypes`|Optional element.<br /><br /> Specifies configuration settings for dynamic compression.|  
|`staticTypes`|Optional element.<br /><br /> Specifies configuration settings for static compression.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
  
## Remarks  
 For more information about the `httpCompression` element, see the following topic on the Microsoft IIS.net Web site: [HTTP Compression \<httpCompression>](http://www.iis.net/ConfigReference/system.webServer/httpCompression).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<scheme>](../../reference/admin/scheme-element-for-httpcompression.md)   
 [\<staticTypes>](../../reference/admin/statictypes-element-for-httpcompression.md)   
 [\<dynamicTypes>](../../reference/admin/dynamictypes-element-for-httpcompression.md)