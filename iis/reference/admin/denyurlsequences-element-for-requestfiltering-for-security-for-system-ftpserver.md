---
title: "denyUrlSequences Element for requestFiltering for security for system.ftpServer | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 015ef75b-404c-4af5-928a-534fb9d28f9c
caps.latest.revision: 7
author: "shirhatti"
manager: "wpickett"
---
# denyUrlSequences Element for requestFiltering for security for system.ftpServer
> [!NOTE]
>  For more information about the `denyUrlSequences` element, see the following topic on the Microsoft IIS.net Web site: [FTP Deny URL Sequences \<denyUrlSequences>](http://www.iis.net/ConfigReference/system.ftpServer/security/requestFiltering/denyUrlSequences).  
  
 Specifies character sequences that should be denied to help prevent URL-based attacks on the FTP server.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a sequence to the collection of denied URL sequences.|  
|`remove`|Optional element.<br /><br /> Removes all references to sequences from the `denyUrlSequences` collection.|  
|`clear`|Optional element.<br /><br /> Removes a reference to a sequence from the `denyUrlSequences` collection.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.ftpServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies security settings for an FTP server.|  
|`requestFiltering`|Specifies configuration settings for request filtering.|  
  
## Remarks  
 For more information about the `denyUrlSequences` element, see the following topic on the Microsoft IIS.net Web site: [FTP Deny URL Sequences \<denyUrlSequences>](http://www.iis.net/ConfigReference/system.ftpServer/security/requestFiltering/denyUrlSequences).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-denyurlsequences-for-system-ftpserver.md)