---
title: "clear Element for isapiCgiRestriction | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 9b94337a-0626-41d1-bff9-9063867898d9
caps.latest.revision: 12
author: "shirhatti"
manager: "wpickett"
---
# clear Element for isapiCgiRestriction
> [!NOTE]
>  For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [ISAPI/CGI Restrictions \<isapiCgiRestriction>](http://www.iis.net/ConfigReference/system.webServer/security/isapiCgiRestriction).  
  
 Removes all references to restrictions from the isapiCgiRestriction collection.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
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
 For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [ISAPI/CGI Restrictions \<isapiCgiRestriction>](http://www.iis.net/ConfigReference/system.webServer/security/isapiCgiRestriction).  
  
## Default Configuration  
 None.  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|