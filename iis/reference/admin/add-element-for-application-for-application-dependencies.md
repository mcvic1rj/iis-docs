---
title: "add Element for application for application Dependencies | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: e8121a4f-0116-4f2f-99ce-547bb1d4d5e6
caps.latest.revision: 12
author: "shirhatti"
manager: "wpickett"
---
# add Element for application for application Dependencies
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Applications for Application Dependencies \<add>](http://www.iis.net/ConfigReference/system.webServer/security/applicationDependencies/application/add).  
  
 Adds additional groupIDs to the parent application.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`groupID`|Required `string` attribute.<br /><br /> Specifies additional groupIDs associated with the parent application.|  
  
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
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding Applications for Application Dependencies \<add>](http://www.iis.net/ConfigReference/system.webServer/security/applicationDependencies/application/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|