---
title: "isapiCgiRestriction Element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: e65ee12f-0556-430a-a2c3-85ebb8f8027a
caps.latest.revision: 14
author: "shirhatti"
manager: "wpickett"
---
# isapiCgiRestriction Element
> [!NOTE]
>  For more information about the `isapiCgiRestriction` element, see the following topic on the Microsoft IIS.net Web site: [ISAPI/CGI Restrictions \<isapiCgiRestriction>](http://www.iis.net/ConfigReference/system.webServer/security/isapiCgiRestriction).  
  
 Specifies settings that restrict which CGI and ISAPI programs are allowed to run on the server.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`notListedIsapisAllowed`|Optional `Boolean` attribute.<br /><br /> Specifies whether unlisted ISAPI modules are allowed to run on this server.<br /><br /> The default value is `false`.|  
|`notListedCgisAllowed`|Optional `Boolean` attribute.<br /><br /> Specifies whether unlisted CGI programs are allowed to run on this server.<br /><br /> The default value is `false`.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a restriction to the collection of ISAPI and CGI restrictions.|  
|`remove`|Optional element.<br /><br /> Removes a reference to a restriction from the `isapiCgiRestriction` collection.|  
|`clear`|Optional element.<br /><br /> Removes all references to restrictions from the `isapiCgiRestriction` collection.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
  
## Remarks  
 For more information about the `isapiCgiRestriction` element, see the following topic on the Microsoft IIS.net Web site: [ISAPI/CGI Restrictions \<isapiCgiRestriction>](http://www.iis.net/ConfigReference/system.webServer/security/isapiCgiRestriction).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-isapicgirestriction.md)   
 [\<remove>](../../reference/admin/remove-element-for-isapicgirestriction.md)   
 [\<clear>](../../reference/admin/clear-element-for-isapicgirestriction.md)