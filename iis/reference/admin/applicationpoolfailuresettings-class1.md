---
title: "ApplicationPoolFailureSettings Class1 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 8e1aa657-4665-39cb-afee-d927d33c3f85
caps.latest.revision: 24
author: "shirhatti"
manager: "wpickett"
---
# ApplicationPoolFailureSettings Class1
Exposes properties that determine the actions to be taken when an application pool or worker process fails.  
  
## Syntax  
  
```vbs  
class ApplicationPoolFailureSettings : EmbeddedObject  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `ApplicationPoolFailureSettings` class.  
  
|Name|Description|  
|----------|-----------------|  
|`AutoShutdownExe`|A read/write `string` value that specifies an executable file to run when the World Wide Web Publishing Service (WWW service) shuts down an application pool. The default is `null`. Use the `AutoShutdownParams` property to send parameters to the executable.|  
|`AutoShutdownParams`|A read/write `string` value that contains the command-line parameters for the executable file specified by the `AutoShutdownExe` property. The default is `null`.|  
|`LoadBalancerCapabilities`|A read/write `sint32` value that specifies application pool behavior when a service is unavailable. The possible values are listed later in the Remarks section.|  
|`OrphanActionExe`|A read/write `string` value that specifies an executable file to run when the WWW service orphans a worker process. The default is `null`. Use the `OrphanActionParams` property to send parameters to the executable file.|  
|`OrphanActionParams`|A read/write `string` value that contains the command-line parameters for the executable file specified by the `OrphanActionExe` property. To specify the process ID of the orphaned worker process, use "%1%". The default is `null`.|  
|`OrphanWorkerProcess`|A read/write `boolean` value. `true` if the WWW service orphans a worker process that fails to respond to requests; otherwise, `false`. The default is `false`. When the value is set to `false`, any worker process that fails to respond will be terminated.|  
|`RapidFailProtection`|A read/write `boolean` value. `true` if the WWW service will terminate all applications in an application pool when the number of worker process failures reaches the maximum specified by `RapidFailProtectionMaxCrashes` within the number of seconds specified by `RapidFailProtectionInterval`; otherwise, `false`. The default is `true`.|  
|`RapidFailProtectionInterval`|A read/write `datetime` value that specifies the number of seconds before the failure count for a worker process is reset. The default is 5.|  
|`RapidFailProtectionMaxCrashes`|A read/write `uint32` value that specifies the maximum number of permissible worker process failures. The default is 5.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `Failure` property of the [ApplicationPool](../../reference/admin/applicationpool-class1.md) class and the [ApplicationPoolElementDefaults](../../reference/admin/applicationpoolelementdefaults-class1.md) class.  
  
 The following table lists the possible values and the associated keywords and actions for the `LoadBalancerCapabilities` property. The default is 2 (`HttpLevel`).  
  
|Value|Keyword|Action|  
|-----------|-------------|------------|  
|1|`TcpLevel`|Terminates the connection.|  
|2|`HttpLevel`|Sends error code 503 (service unavailable).|  
  
## Inheritance Hierarchy  
 [EmbeddedObject](../../reference/admin/embeddedobject-class1.md)  
  
 `ApplicationPoolFailureSettings`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [CIM_DATETIME](http://go.microsoft.com/fwlink/?LinkId=57551)   
 [ApplicationPool Class](../../reference/admin/applicationpool-class1.md)   
 [ApplicationPoolElementDefaults Class](../../reference/admin/applicationpoolelementdefaults-class1.md)   
 [EmbeddedObject Class](../../reference/admin/embeddedobject-class1.md)