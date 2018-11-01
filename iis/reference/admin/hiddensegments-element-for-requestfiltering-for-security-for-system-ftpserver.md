---
title: "hiddenSegments Element for requestFiltering for security for system.ftpServer | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: a60fb3ae-47b2-470e-8049-1318a32ea639
caps.latest.revision: 8
author: "shirhatti"
manager: "wpickett"
---
# hiddenSegments Element for requestFiltering for security for system.ftpServer
> [!NOTE]
>  For more information about the `hiddenSegements` element, see the following topic on the Microsoft IIS.net Web site: [FTP Hidden Segments \<hiddenSegments>](http://www.iis.net/ConfigReference/system.ftpServer/security/requestFiltering/hiddenSegments).  
  
 Specifies a collection of elements that identify certain URLs that FTP 7 will make inaccessible to FTP clients.  
  
## Syntax  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements for this section.  
  
### Attributes  
 None  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`add`|Optional element.<br /><br /> Adds a segment to the collection of hidden segments.|  
|`remove`|Optional element.<br /><br /> Removes all references to segments from the `hiddenSegments` collection.|  
|`clear`|Optional element.<br /><br /> Removes a reference to a segment from the `hiddenSegments` collection.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|`configuration`|Specifies the root element in every configuration file that is used by [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)].|  
|`system.ftpServer`|Specifies the top-level section group (in ApplicationHost.config) in which this element is defined.|  
|`security`|Specifies security settings for an FTP server.|  
|`requestFiltering`|Specifies configuration settings for request filtering.|  
  
## Remarks  
 For more information about the `hiddenSegements` element, see the following topic on the Microsoft IIS.net Web site: [FTP Hidden Segments \<hiddenSegments>](http://www.iis.net/ConfigReference/system.ftpServer/security/requestFiltering/hiddenSegments).  
  
## Element Information  
  
|||  
|-|-|  
|**Configuration locations**|ApplicationHost.config|  
|**Requirements**|[!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] and later|  
  
## See Also  
 [\<add>](../../reference/admin/add-element-for-hiddensegments-for-system-ftpserver.md)