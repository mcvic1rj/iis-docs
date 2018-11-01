---
title: "remove Element for isapiCgiRestriction | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: f92a3d80-7e7b-4728-baa6-5027879e0a6b
caps.latest.revision: 11
author: "shirhatti"
manager: "wpickett"
---
# remove Element for isapiCgiRestriction
> [!NOTE]
>  For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [ISAPI/CGI Restrictions \<isapiCgiRestriction>](http://www.iis.net/ConfigReference/system.webServer/security/isapiCgiRestriction).  
  
 Removes a reference to a restriction from the `isapiCgiRestriction` collection.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`description`|Optional `string` attribute.<br /><br /> Specifies the friendly description of the group associated with this `groupID`.<br /><br /> See the Default Configuration section later in this topic for the complete list of default values.|  
|`groupId`|Optional `string` attribute.<br /><br /> Specifies the `groupID` of the application that has a dependency on an extension restriction.<br /><br /> See the Default Configuration section later in this topic for the complete list of default values.|  
|`path`|Required `string` attribute.<br /><br /> Specifies the path of the CGI or ISAPI module in the file system of the server.<br /><br /> See the Default Configuration section later in this topic for the complete list of default values.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
|`isapiCgiRestriction`|Specifies settings that restrict which CGI and ISAPI programs are allowed to run on the server.|  
  
## Remarks  
 For more information about the `remove` element, see the following topic on the Microsoft IIS.net Web site: [ISAPI/CGI Restrictions \<isapiCgiRestriction>](http://www.iis.net/ConfigReference/system.webServer/security/isapiCgiRestriction).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|