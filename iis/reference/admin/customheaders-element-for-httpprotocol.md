---
title: "customHeaders Element for httpProtocol | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 68f7134f-3f70-4702-88c0-5ba0ab12cfe3
caps.latest.revision: 24
author: "shirhatti"
manager: "wpickett"
---
# customHeaders Element for httpProtocol
> [!NOTE]
>  For more information about the `customHeaders` element, see the following topic on the Microsoft IIS.net Web site: [Custom Headers \<customHeaders>](http://www.iis.net/ConfigReference/system.webServer/httpProtocol/customHeaders).  
  
 Configures custom response headers that are returned in responses from the Web server.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a custom response header to the customHeaders collection.|  
|`clear`|Optional element.<br /><br /> Removes all references to custom response headers from the customHeaders collection.|  
|`remove`|Optional element.<br /><br /> Removes a reference to a custom response header from the customHeaders collection.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
  
## Remarks  
 For more information about the `customHeaders` element, see the following topic on the Microsoft IIS.net Web site: [Custom Headers \<customHeaders>](http://www.iis.net/ConfigReference/system.webServer/httpProtocol/customHeaders).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-customheaders-for-httpprotocol.md)   
 [\<remove>](../../reference/admin/remove-element-for-customheaders-for-httpprotocol.md)   
 [\<clear>](../../reference/admin/clear-element-for-customheaders-for-httpprotocol.md)