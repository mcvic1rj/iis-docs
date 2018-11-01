---
title: "application Element for applicationDependencies | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: ceb57258-71d8-4917-98fe-ab5c54151ec9
caps.latest.revision: 16
author: "shirhatti"
manager: "wpickett"
---
# application Element for applicationDependencies
> [!NOTE]
>  For more information about the `application` element, see the following topic on the Microsoft IIS.net Web site: [Applications for Application Dependencies \<application>](http://www.iis.net/ConfigReference/system.webServer/security/applicationDependencies/application).  
  
 Specifies an application that has dependencies on a CGI or ISAPI extension restriction.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`groupID`|Optional `string` attribute.<br /><br /> Specifies the groupID of the application that has a dependency on an extension restriction.<br /><br /> See the following Default Configuration section for the complete list of default values.|  
|`Name`|Required `string` attribute.<br /><br /> Specifies the unique name of the application that has a dependency on an extension restriction.<br /><br /> See the following Default Configuration section for the complete list of default values.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds additional groupIDs to the parent application.|  
|`clear`|Optional element.<br /><br /> Removes all references to additional groupIDs from the add collection.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
|`applicationDependencies`|Specifies an application that has dependencies to one or more CGI or ISAPI extension restrictions.|  
  
## Remarks  
 For more information about the `application` element, see the following topic on the Microsoft IIS.net Web site: [Applications for Application Dependencies \<application>](http://www.iis.net/ConfigReference/system.webServer/security/applicationDependencies/application).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-application-for-application-dependencies.md)   
 [\<clear>](../../reference/admin/clear-element-for-add-element-for-application-for-application-dependencies.md)