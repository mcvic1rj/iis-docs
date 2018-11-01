---
title: "add Element for hiddenSegments for system.ftpServer | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: aad7ffaa-85e6-41db-b3da-1f85d9eee41d
caps.latest.revision: 7
author: "shirhatti"
manager: "wpickett"
---
# add Element for hiddenSegments for system.ftpServer
> [!NOTE]
>  For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding FTP Hidden Segments \<add>](http://www.iis.net/ConfigReference/system.ftpServer/security/requestFiltering/hiddenSegments/add).  
  
 Specifies a unique URL segment to add to the collection of hidden segments for FTP 7.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`segments`|Required `string` attribute.<br /><br /> Specifies part of the file system that should never be served to clients. **Note:**  There is no default value, but FTP access to the _vti_bin virtual directory is blocked when the FTP service is installed.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.ftpServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies the root element for configuring security settings for an FTP Server.|  
|`requestFiltering`|Specifies configuration settings for request filtering.|  
  
## Remarks  
 For more information about the `add` element, see the following topic on the Microsoft IIS.net Web site: [Adding FTP Hidden Segments \<add>](http://www.iis.net/ConfigReference/system.ftpServer/security/requestFiltering/hiddenSegments/add).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [IIS 7.0: add Element for hiddenSegments for system.ftpServer (IIS Settings Schema)](../../reference/admin/add-element-for-hiddensegments-for-system-ftpserver.md)