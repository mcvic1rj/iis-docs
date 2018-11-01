---
title: "clientCache Element for staticContent | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 1530d6b3-7235-4902-b363-b4e14de6505d
caps.latest.revision: 18
author: "shirhatti"
manager: "wpickett"
---
# clientCache Element for staticContent
> [!NOTE]
>  For more information about the `clientCache` element, see the following topic on the Microsoft IIS.net Web site: [Client Cache \<clientCache>](http://www.iis.net/ConfigReference/system.webServer/staticContent/clientCache).  
  
 Specifies settings for caching static content that is sent to the client.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`cacheControlCustom`|Optional `string` attribute.<br /><br /> Specifies custom HTTP 1.1 cache control directives. Multiple directives can be specified if they are separated by carriage return/line feed (CRLF) pairs.|  
|`cacheControlMaxAge`|Optional `timeSpan` attribute.<br /><br /> Specifies the maximum age (in seconds) of the cache control value.<br /><br /> The default value is 1.00:00:00 (1 day).|  
|`cacheControlMode`|Optional `enum` attribute.<br /><br /> Specifies the mode to use for client caching.<br /><br /> The `cacheControlMode` attribute can be one of the following possible values.<br /><br /> The default is `NoControl`.<br /><br /> `NoControl`:<br /><br /> - Does not add a Cache-Control or Expires header to the response. The numeric value is 0.<br /><br /> `DisableCache`:<br /><br /> - Adds a Cache-Control: no-cache header to the response. The numeric value is 1.<br /><br /> `UseMaxAge`:<br /><br /> - Adds a Cache-Control: max-age=\<nnn> header to the response based on the value specified in the `CacheControlMaxAge` attribute. The numeric value is 2.<br /><br /> `UseExpires`:<br /><br /> - Adds an Expires: \<date> header to the response based on the date specified in the `httpExpires` attribute. The numeric value is 3.|  
|`httpExpires`|Optional `string` attribute.<br /><br /> Specifies, in Request for Comments (RFC) 1123 format, the date and time after which a page that is cached on the client is considered stale. The value is returned to the browser in the HTML file header. The user agent compares the given value with the current date to determine whether to display a cached page or to request an updated page from the server.<br /><br /> For more information on date and time formats, see RFC 1123, "Requirements for Internet Hosts -- Application and Support." For more information on header fields, see Request for Comments (RFC) 2616, "Hypertext Transfer Protocol -- HTTP/1.1."|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`staticContent`|Configures static file request handler settings.|  
  
## Remarks  
 For more information about the `clientCache` element, see the following topic on the Microsoft IIS.net Web site: [Client Cache \<clientCache>](http://www.iis.net/ConfigReference/system.webServer/staticContent/clientCache).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<mimeMap>](../../reference/admin/mimemap-element-for-staticcontent.md)