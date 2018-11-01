---
title: "add Element for profiles for caching | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 9ee9f176-d6d4-446f-bd1a-5a31125f5f98
caps.latest.revision: 27
author: "shirhatti"
manager: "wpickett"
---
# add Element for profiles for caching
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Caching Profiles \<add>](http://www.iis.net/ConfigReference/system.webServer/caching/profiles/add).  
  
 Adds an output caching profile to the collection of output caching profiles.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`duration`|Optional `timeSpan` attribute.<br /><br /> Specifies the time (in seconds) that the page or user control is cached<br /><br /> The default is 00:00:30.|  
|`extension`|Required `string` attribute.<br /><br /> Specifies the file type extension for the files you want to cache.|  
|`kernelCachePolicy`|Optional `enum` attribute.<br /><br /> Configures the kernel caching policy.<br /><br /> The `kernelCachePolicy` attribute can be one of the following values. The default is `DontCache`.<br /><br /> `DontCache`:<br /><br /> - Content is not cached. The numeric value is 0.<br /><br /> `CacheUntilChange`:<br /><br /> - Content is only cached until the content changes. The numeric value is 1.<br /><br /> `CacheForTimePeriod`:<br /><br /> - Content is cached for the length of time specified by the `duration` attribute. The numeric value is 2.<br /><br /> `DisableCache`:<br /><br /> - The cache is disabled and no caching will occur. The numeric value is 3|  
|`location`|Optional `enum` attribute.<br /><br /> Specifies the valid values for controlling the location of the output-cached HTTP response for a resource.<br /><br /> The `location` attribute can be one of the following possible values. The default is `Server`.<br /><br /> `Any`:<br /><br /> - The output cache can be located on the browser client (where the request originated), on a proxy server (or any other server) participating in the request, or on the server where the request was processed. The numeric value is 0.<br /><br /> `Client`:<br /><br /> - The output cache is located on the browser client where the request originated. The numeric value is 1.<br /><br /> `Downstream`:<br /><br /> - The output cache can be stored in any HTTP 1.1 cache-capable devices other than the origin server. This includes proxy servers and the client that made the request. The numeric value is 2.<br /><br /> `Server`:<br /><br /> - The output cache is located on the Web server where the request was processed. The numeric value is 3.<br /><br /> `None`:<br /><br /> - The output cache is disabled for the requested page. The numeric value is 4.<br /><br /> `ServerAndClient`:<br /><br /> - The output cache can be stored only at the origin server or at the requesting client. Proxy servers are not allowed to cache the response. The numeric value is 5.|  
|`policy`|Optional `enum` attribute.<br /><br /> Configures the output caching policy.<br /><br /> The `policy` attribute can be one of the following possible values. The default is `DontCache`.<br /><br /> `DontCache`:<br /><br /> - Content is not cached. The numeric value is 0.<br /><br /> `CacheUntilChange`:<br /><br /> - Content is only cached until the content changes. The numeric value is 1.<br /><br /> `CacheForTimePeriod`:<br /><br /> - Content is cached for the length of time specified by the `duration` attribute. The numeric value is 2<br /><br /> `DisableCache`:<br /><br /> - The cache is disabled and no caching will occur. The numeric value is 3.|  
|`varyByHeaders`|Optional `string` attribute.<br /><br /> Specifies a semicolon-separated list of HTTP headers used to vary the output cache. When this attribute is set to multiple headers, the output cache contains a different version of the requested document for each combination of specified headers.|  
|`varyByQueryString`|Optional `string` attribute.<br /><br /> Specifies a semicolon-separated list of strings used to vary the output cache. By default, these strings correspond to a query string value sent with `GET` method attributes, or a parameter sent by using the `POST` method. When this attribute is set to multiple parameters, the output cache contains a different version of the requested document for each combination of specified parameters. Possible values include `none`, an asterisk (*), and any valid query string or `POST` parameter name.|  
  
### Child Elements  
 None  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`caching`|Configures output cache settings.|  
|`profiles`|Configures the profile to use for output caching.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Caching Profiles \<add>](http://www.iis.net/ConfigReference/system.webServer/caching/profiles/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<clear>](../../reference/admin/clear-element-for-profiles-for-caching.md)   
 [\<remove>](../../reference/admin/remove-element-for-profiles-for-caching.md)