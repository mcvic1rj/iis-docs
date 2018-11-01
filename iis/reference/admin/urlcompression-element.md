---
title: "urlCompression Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: c3afe02b-a7dc-441a-b050-f162b58a34f8
caps.latest.revision: 22
author: "shirhatti"
manager: "wpickett"
---
# urlCompression Element
> [!NOTE]
>  For more information about the `urlCompression` element, see the following topic on the Microsoft IIS.net Web site: [URL Compression \<urlCompression>](http://www.iis.net/ConfigReference/system.webServer/urlCompression).  
  
 Configures compression of static and dynamic content.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`doDynamicCompression`|Optional `Boolean` attribute.<br /><br /> Specifies whether dynamic compression is enabled for URLs. **Note:**  Use of dynamic compression may increase processor utilization and reduce the overall performance of the Web server. <br /><br /> The default value is `false`.|  
|`doStaticCompression`|Optional `Boolean` attribute.<br /><br /> Specifies whether static compression is enabled for URLs.<br /><br /> The default value is `true`.|  
|`dynamicCompressionBeforeCache`|Optional `Boolean` attribute.<br /><br /> Specifies whether the currently available response is dynamically compressed before it is put into the output cache. For more information, see the Remarks section.<br /><br /> The default value is `false`.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
  
## Remarks  
 For more information about the `urlCompression` element, see the following topic on the Microsoft IIS.net Web site: [URL Compression \<urlCompression>](http://www.iis.net/ConfigReference/system.webServer/urlCompression).  
  
 When the `dynamicCompressionBeforeCache` attribute is `true`, IIS dynamically compresses the response the first time a request is made. The compressed response is put into the output cache, and the cached response is sent to the client. Subsequent requests are served from the compressed response in the output cache.  
  
 When `dynamicCompressionBeforeCache` is `false`, IIS puts the noncompressed response into the output cache. Then, every time that the response is requested, IIS dynamically compresses the cached response as it is sent to the client.  
  
 If you set the `dynamicCompressionBeforeCache` attribute to `true`, the CPU will dynamically compress the response only one time instead of every time that the page is requested. Because dynamic compression is CPU-intensive, a setting of `true` can reduce the server load and improve site throughput.  
  
> [!NOTE]
>  If the `dynamicCompressionBeforeCache` attribute is `true` when the output cache response has been flushed, dynamic compression will not be performed before the response is put into the output cache. However, if the `doDynamicCompression` attribute is `true`, dynamic compression will still occur after the response has been put into the output cache.  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [UrlCompressionSection Class](../../reference/admin/urlcompressionsection-class.md)