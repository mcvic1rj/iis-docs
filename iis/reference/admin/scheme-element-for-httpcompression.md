---
title: "scheme Element for httpCompression | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 6d59654c-27d5-42a6-b46a-77138f65725b
caps.latest.revision: 42
author: "shirhatti"
manager: "wpickett"
---
# scheme Element for httpCompression
Configures the GNU zip (Gzip) and Deflate compression schemes.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`dll`|Required `string` attribute.<br /><br /> Specifies the fully qualified file system path and file name of the compression DLL associated with the compression scheme. The World Wide Web Publishing Service (WWW service) must be restarted before any changes to this attribute take effect.|  
|`doDynamicCompression`|Optional `Boolean` attribute.<br /><br /> Specifies whether responses to requests for dynamic content, such as scripts in Active Server Pages (ASP) and ISAPI extensions, are compressed. Because this attribute cannot be inherited, it must be set to true at both the global level (`httpCompression`) and at the individual scheme level if the `name` attribute is set to `Gzip`. If this value is changed at the individual compression scheme level, the WWW service must be restarted before the change takes effect.<br /><br /> The default value is `true`.|  
|`doStaticCompression`|Optional `Boolean` attribute.<br /><br /> Specifies whether IIS compresses responses to requests for static content. Because this attribute cannot be inherited, it must be set to true at both the global level (`httpCompression`) and the individual scheme level if the `name` attribute is set to `Gzip`. If this value is changed at the individual compression scheme level, the WWW service must be restarted before the change takes effect. **Note:**  The static compression store needs to be located in a disk partition or remote share formatted with NTFS. If the file store is not NTFS, static compression is disabled. For security reasons, no compressed responses will be served from a FAT cache store. <br /><br /> The default value is `true`.|  
|`dynamicCompressionLevel`|Optional `integer` attribute.<br /><br /> Specifies the compression level for the compression scheme when dynamic content is being compressed. The levels range from 0 (lowest compression level and lowest CPU usage) to 10 (highest compression level and highest CPU usage). 0 means that compression is disabled. The WWW service must be restarted before any changes to this attribute take effect. **Note:**  Because dynamic compression consumes considerable CPU time and memory resources, use it only on servers that have slow network connections but CPU time to spare. Compressed static responses can be cached and, therefore, do not affect CPU resources like dynamic responses do. <br /><br /> The default value is 0.|  
|`name`|Required `string` attribute.<br /><br /> Specifies the name of the compression scheme, for example, Gzip or Deflate.|  
|`staticCompressionLevel`|Optional `integer` attribute.<br /><br /> Specifies the compression level for the compression scheme when static content is being compressed. The levels range from 0 (lowest compression level and lowest CPU usage) to 10 (highest compression level and lowest CPU usage). 0 means that compression is disabled. The WWW service must be restarted before any changes to this attribute take effect.<br /><br /> The default value is 7.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`remove`|Optional element.<br /><br /> Removes a reference to an HTTP compression scheme from the HTTP compression scheme collection.|  
|`clear`|Optional element.<br /><br /> Removes all references to HTTP compression schemes from the HTTP compression scheme collection.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the root element in ApplicationHost.config that is the top-level section group in which this element is defined.|  
|`httpCompression`|Configures HTTP compression settings for a Web server.|  
  
## Remarks  
 For more information about the `scheme` element, see the following topic on the Microsoft IIS.net Web site: [Scheme \<scheme>](http://www.iis.net/ConfigReference/system.webServer/httpCompression/scheme).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root level Web.config<br /><br /> Application level Web.config<br /><br /> Virtual or physical directory level Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [Scheme \<scheme>](http://www.iis.net/ConfigReference/system.webServer/httpCompression/scheme)   
 [\<remove>](../../reference/admin/remove-element-for-scheme-for-httpcompression.md)   
 [\<clear>](../../reference/admin/clear-element-for-scheme-for-httpcompression.md)