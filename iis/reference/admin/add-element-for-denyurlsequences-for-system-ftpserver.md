---
title: "add Element for denyUrlSequences for system.ftpServer | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 47bde6d1-2077-4a7f-a48a-0fa673d5821c
caps.latest.revision: 7
author: "shirhatti"
manager: "wpickett"
---
# add Element for denyUrlSequences for system.ftpServer
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding FTP Deny URL Sequences \<add>](http://www.iis.net/ConfigReference/system.ftpServer/security/requestFiltering/denyUrlSequences/add).  
  
 Specifies a unique sequence of characters to add to the collection of denied URL sequences for FTP 7.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`sequence`|Required `string` attribute.<br /><br /> Specifies sequences of characters in URLs that the FTP server should never process to help prevent URL-based attacks on the FTP server.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.ftpServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies security settings for an FTP server.|  
|`requestFiltering`|Specifies configuration settings for request filtering.|  
|`denyUrlSequences`|Specifies sequences that should be denied to help prevent URL-based attacks on the FTP server.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding FTP Deny URL Sequences \<add>](http://www.iis.net/ConfigReference/system.ftpServer/security/requestFiltering/denyUrlSequences/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<denyUrlSequences>](../../reference/admin/denyurlsequences-element-for-requestfiltering-for-security-for-system-ftpserver.md)