---
title: "FtpCachePolicySettings Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: bcc87d56-7455-34dd-d844-bb0a439ea2d2
caps.latest.revision: 12
author: "shirhatti"
manager: "wpickett"
---
# FtpCachePolicySettings Class
Represents the default FTP cache policy for network resources.  
  
## Syntax  
  
```vbs  
class FtpCachePolicySettings : EmbeddedObject  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `FtpCachePolicySettings` class.  
  
|Name|Description|  
|----------|-----------------|  
|`PolicyLevel`|A read/write `sint32` value that specifies the FTP caching behavior for the local computer. The possible values are listed later in the Remarks section.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `DefaultFtpCachePolicy` property of the [RequestCachingSection](../../reference/admin/requestcachingsection-class.md) class.  
  
 The following table lists the possible values for the `PolicyLevel` property. The default is 0 (`Default`).  
  
|Value|Keyword|Description|  
|-----------|-------------|-----------------|  
|0|`Default`|Satisfies a request for a resource either by using the cached copy of the resource or by sending a request for the resource to the server. The action taken is determined by the current cache policy and the age of the content in the cache. This is the cache level that most applications should use.|  
|1|`BypassCache`|Satisfies a request by using the server. No entries are taken from caches, added to caches, or removed from caches between the client and server. This is the default cache behavior specified in the computer configuration file that is included with the [!INCLUDE[dnprdnshort](../../reference/admin/includes/dnprdnshort-md.md)].|  
|2|`CacheOnly`|Satisfies a request by using the locally cached resource; does not send a request for an item that is not in the cache. When this cache policy level is specified, a [WebException](http://go.microsoft.com/fwlink/?LinkId=67062) exception is thrown if the item is not in the client cache.|  
|3|`CacheIfAvailable`|Satisfies a request for a resource from the cache if the resource is available in the cache; otherwise, sends a request for a resource to the server. If the requested item is not available in the local cache, but it is available in a cache between the client and the server, the intermediate cache satisfies the request.|  
|4|`Revalidate`|Satisfies a request by using the cached copy of the resource if the time stamp is the same as the time stamp of the resource on the server; otherwise, the resource is downloaded from the server, presented to the caller, and stored in the cache.|  
|5|`Reload`|Satisfies a request by using the server. The response might be saved in the cache, depending on the settings of the `no-cache` and `Pragma: no-cache` directives in the HTTP caching protocol.|  
|6|`NoCacheNoStore`|Never satisfies a request by using resources from the cache, and does not cache resources. If the resource is present in the local cache, it is removed. This policy level indicates to intermediate caches that they should remove the resource.|  
  
## Inheritance Hierarchy  
 [EmbeddedObject](../../reference/admin/embeddedobject-class1.md)  
  
 `FtpCachePolicySettings`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [EmbeddedObject Class](../../reference/admin/embeddedobject-class1.md)   
 [RequestCachingSection Class](../../reference/admin/requestcachingsection-class.md)   
 [System.Net.Cache.RequestCacheLevel Enumeration](http://go.microsoft.com/fwlink/?LinkId=70921)   
 [System.Net.WebException Class](http://go.microsoft.com/fwlink/?LinkId=67062)