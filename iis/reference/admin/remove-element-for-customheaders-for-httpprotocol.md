---
title: "remove Element for customHeaders for httpProtocol | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 81ce1a71-bcd7-48ac-9313-c4da9ca74914
caps.latest.revision: 19
author: "shirhatti"
manager: "wpickett"
---
# remove Element for customHeaders for httpProtocol
> [!NOTE]
>  For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Custom Headers \<customHeaders>](http://www.iis.net/ConfigReference/system.webServer/httpProtocol/customHeaders).  
  
 Removes a custom response header from the `customHeaders` collection. Headers that are removed from the `customHeaders` collection are not returned in responses from the Web server.  
  
 IIS 7.0 Beta: configuration Element (IIS Settings Schema)  
IIS 7.0 Beta: system.webServer Element (IIS Settings Schema)  
IIS 7.0 Beta: httpProtocol Element (IIS Settings Schema)  
IIS 7.0 Beta: customHeaders Element for httpProtocol (IIS Settings)  
IIS 7.0 Beta: remove Element for customHeaders for httpProtocol (IIS Settings)  
  
## Syntax  
  
```  
<remove name="field name of header" />  
```  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`name`|Required`string` attribute.<br /><br /> Specifies a field name for the custom response header. In a response, a field name precedes the related field value.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`httpProtocol`|Specifies HTTP protocol configuration for a Web server.|  
|`customHeaders`|Configures a custom response header to be returned in responses from the Web server.|  
  
## Remarks  
 For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [Custom Headers \<customHeaders>](http://www.iis.net/ConfigReference/system.webServer/httpProtocol/customHeaders).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|