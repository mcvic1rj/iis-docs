---
title: "requestFiltering Element for system.ftpServer | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: e1ac901f-6ea9-426e-9d2b-efd7989e1e7d
caps.latest.revision: 7
author: "shirhatti"
manager: "wpickett"
---
# requestFiltering Element for system.ftpServer
> [!NOTE]
>  For more information about the `requestFiltering` element, see the following topic on the Microsoft IIS.net Web site: [FTP Request Filtering \<requestFiltering>](http://www.iis.net/ConfigReference/system.ftpServer/security/requestFiltering).  
  
 Configures FTP Request Filtering, which is a customizable set of rules for blocking specified FTP requests.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`allowHighBitCharacters`|Optional `Boolean` attribute.<br /><br /> Specifies whether to allow non-ASCII characters in URLs.<br /><br /> The default value is `true`.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`fileExtensions`|Optional element.<br /><br /> Specifies which file name extensions are allowed or denied to limit types of requests sent to the FTP server.|  
|`requestLimits`|Optional element.<br /><br /> Specifies limits on requests processed by the FTP server.|  
|`hiddenSegments`|Optional element.<br /><br /> Specifies that certain segments of URLs can be made inaccessible to clients.|  
|`denyUrlSequences`|Specifies sequences that should be denied to help prevent URL-based attacks on the FTP server.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.ftpServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the root element for configuring security settings on an FTP server.|  
  
## Remarks  
 For more information about the `requestFiltering` element, see the following topic on the Microsoft IIS.net Web site: [FTP Request Filtering \<requestFiltering>](http://www.iis.net/ConfigReference/system.ftpServer/security/requestFiltering).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<fileExtensions>](../../reference/admin/fileextensions-element-for-requestfiltering-for-security-for-system-ftpserver.md)   
 [\<requestLimits>](../../reference/admin/requestlimits-element-for-requestfiltering-for-security-for-system-ftpserver.md)   
 [\<hiddenSegments>](../../reference/admin/hiddensegments-element-for-requestfiltering-for-security-for-system-ftpserver.md)   
 [\<denyUrlSequences>](../../reference/admin/denyurlsequences-element-for-requestfiltering-for-security-for-system-ftpserver.md)