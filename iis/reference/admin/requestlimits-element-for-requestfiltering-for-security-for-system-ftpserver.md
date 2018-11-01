---
title: "requestLimits Element for requestFiltering for security for system.ftpServer | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 464e7554-b378-4d3d-bf2a-23be37752d5f
caps.latest.revision: 8
author: "shirhatti"
manager: "wpickett"
---
# requestLimits Element for requestFiltering for security for system.ftpServer
> [!NOTE]
>  For more information about the `requestLimits` element, see the following topic on the Microsoft IIS.net Web site: [FTP Request Limits \<requestLimits>](http://www.iis.net/ConfigReference/system.ftpServer/security/requestFiltering/requestLimits).  
  
 Specifies limits on FTP requests that are processed by the FTP server, such as the maximum size of a request and the maximum length for a command sequence.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|maxAllowedContentLength|Optional `int64` attribute.<br /><br /> Specifies the maximum length of content in a request, in `bytes`.<br /><br /> The default value is 0 (unlimited).|  
|maxUrl|Optional `uint` attribute.<br /><br /> Specifies the maximum length of the request, in bytes. **Note:**  This value must be between 32 and 32768. <br /><br /> The default value is 4096.|  
  
### Child Elements  
 None  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.ftpServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies security settings for an FTP server.|  
  
## Remarks  
 For more information about the `requestLimits` element, see the following topic on the Microsoft IIS.net Web site: [FTP Request Limits \<requestLimits>](http://www.iis.net/ConfigReference/system.ftpServer/security/requestFiltering/requestLimits).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<requestFiltering>](../../reference/admin/requestfiltering-element-for-system-ftpserver.md)