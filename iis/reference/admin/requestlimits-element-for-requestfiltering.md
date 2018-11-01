---
title: "requestLimits Element for requestFiltering | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 2464898f-f4aa-4955-919e-ed7492ad2b78
caps.latest.revision: 13
author: "shirhatti"
manager: "wpickett"
---
# requestLimits Element for requestFiltering
> [!NOTE]
>  For more information about the `requestLimits` element, see the following topic on the Microsoft IIS.net Web site: [Request Limits \<requestLimits>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/requestLimits).  
  
 Specifies limits on requests processed by the Web server.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`maxAllowedContentLength`|Optional `uint` attribute.<br /><br /> Specifies the maximum length of content in a request, in bytes.<br /><br /> The default value is 30000000.|  
|`maxQueryString`|Optional `uint` attribute.<br /><br /> Specifies the maximum length of the query string, in bytes.<br /><br /> The default value is 2048.|  
|`maxUrl`|Optional `uint` attribute.<br /><br /> Specifies maximum length of the URL, in bytes.<br /><br /> The default value is 4096.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`headerlimits`|Optional element.<br /><br /> Specifies size limits for HTML headers.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
|`requestFiltering`|Specifies configuration settings for request filtering.|  
  
## Remarks  
 For more information about the `requestLimits` element, see the following topic on the Microsoft IIS.net Web site: [Request Limits \<requestLimits>](http://www.iis.net/ConfigReference/system.webServer/security/requestFiltering/requestLimits).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<headerLimits>](../../reference/admin/headerlimits-element-for-requestlimits.md)