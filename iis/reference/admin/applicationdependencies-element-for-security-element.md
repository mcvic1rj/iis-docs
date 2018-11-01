---
title: "applicationDependencies Element for security element | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 32c6ca96-1e54-4704-b381-aa2e696ed315
caps.latest.revision: 17
author: "shirhatti"
manager: "wpickett"
---
# applicationDependencies Element for security element
> [!NOTE]
>  For more information about the `applicationDependencies` element, see the following topic on the Microsoft IIS.net Web site: [Application Dependencies \<applicationDependencies>](http://www.iis.net/ConfigReference/system.webServer/security/applicationDependencies).  
  
 Specifies an application that has dependencies to one or more CGI or ISAPI extension restrictions.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`application`|Optional element.<br /><br /> Specifies an application that has dependencies on a CGI or ISAPI extension restriction.|  
|`clear`|Optional element.<br /><br /> Removes all references to applications from the applicationDependencies collection.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.webServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the section group that contains security-related sections.|  
  
## Remarks  
 For more information about the `applicationDependencies` element, see the following topic on the Microsoft IIS.net Web site: [Application Dependencies \<applicationDependencies>](http://www.iis.net/ConfigReference/system.webServer/security/applicationDependencies).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|Machine.config<br /><br /> ApplicationHost.config<br /><br /> Root application Web.config<br /><br /> Application Web.config<br /><br /> Directory Web.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<application>](../../reference/admin/application-element-for-applicationdependencies.md)