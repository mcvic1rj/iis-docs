---
title: "providerDefinitions Element for system.ftpServer | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: f3c4ff6b-3535-4ba9-aed1-b244ca97a4c5
caps.latest.revision: 9
author: "shirhatti"
manager: "wpickett"
---
# providerDefinitions Element for system.ftpServer
> [!NOTE]
>  For more information about the `providerDefinitions` element, see the following topic on the Microsoft IIS.net Web site: [Provider Definitions \<providerDefinitions>](http://www.iis.net/ConfigReference/system.ftpServer/providerDefinitions).  
  
 Specifies a collection of custom FTP providers.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Specifies the registration information for a managed-code or native-code (COM) provider.|  
|`activation`|Optional element.<br /><br /> Specifies a collection of custom name/value pairs that define any parameters that a custom provider requires. **Note:**  This element was added in FTP 7.5.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.ftpServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
  
## Remarks  
 For more information about the `providerDefinitions` element, see the following topic on the Microsoft IIS.net Web site: [Provider Definitions \<providerDefinitions>](http://www.iis.net/ConfigReference/system.ftpServer/providerDefinitions).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<activation>](../../reference/admin/activation-element-for-system-ftpserver.md)