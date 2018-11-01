---
title: "clear Element for add Element for application for application Dependencies | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: cbf6f06a-7678-4f70-bef8-0de0c78f3232
caps.latest.revision: 10
author: "shirhatti"
manager: "wpickett"
---
# clear Element for add Element for application for application Dependencies
> [!NOTE]
>  For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [Applications for Application Dependencies \<application>](http://www.iis.net/ConfigReference/system.webServer/security/applicationDependencies/application).  
  
 Removes all references to additional groupIDs from the add collection.  
  
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
|`applicationDependencies`|Specifies an application that has dependencies to one or more extension restrictions.|  
|`application`|Specifies an application that has dependencies on an extension restriction.|  
  
## Remarks  
 For more information about the `clear` element, see the following topic on the Microsoft IIS.net Web site: [Applications for Application Dependencies \<application>](http://www.iis.net/ConfigReference/system.webServer/security/applicationDependencies/application).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|