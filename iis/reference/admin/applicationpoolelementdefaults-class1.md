---
title: "ApplicationPoolElementDefaults Class1 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 53b7dc67-a6ac-ff21-3112-2a3163703fed
caps.latest.revision: 27
author: "shirhatti"
manager: "wpickett"
---
# ApplicationPoolElementDefaults Class1
Contains the default properties for the [ApplicationPool](../../reference/admin/applicationpool-class1.md) class.  
  
## Syntax  
  
```vbs  
class ApplicationPoolElementDefaults : EmbeddedObject  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `ApplicationPoolElementDefaults` class.  
  
|Name|Description|  
|----------|-----------------|  
|`AutoStart`|A read/write `boolean` value. `true` if the World Wide Web Publishing Service (WWW service) will start the application pool automatically either when the application pool is created or when IIS is started; otherwise, `false`. The default is `true`.|  
|`Cpu`|An [ApplicationPoolProcessorSettings](../../reference/admin/applicationpoolprocessorsettings-class1.md) object that contains the CPU settings for an application pool.|  
|`Enable32BitAppOnWin64`|A read/write `boolean` value. `true` if 32-bit applications (both managed and native) can run on 64-bit versions of Windows; otherwise, `false`. The default is `false`.|  
|`Failure`|An [ApplicationPoolFailureSettings](../../reference/admin/applicationpoolfailuresettings-class1.md) object that defines properties that determine the actions to be taken when an application pool or worker process fails.|  
|`ManagedPipelineMode`|A read/write `sint32` value that indicates the managed pipeline mode. The possible values are listed in the Remarks section.|  
|`ManagedRuntimeVersion`|A read/write `string` value that contains the version of the [!INCLUDE[dnprdnshort](../../reference/admin/includes/dnprdnshort-md.md)] that the application pool preloads. The default is "v2.0". If the property is written to, IIS recycles the application pool and loads the newly specified [!INCLUDE[dnprdnshort](../../reference/admin/includes/dnprdnshort-md.md)] version for it.|  
|`Name`|A read/write `string` value that contains the name of the default application pool.|  
|`PassAnonymousToken`|A read/write `boolean` value. `true` if the Windows Process Activation Service (WAS) creates and passes a token for the built-in IUSR anonymous user account to the Anonymous authentication module; otherwise, `false`. The default is `true`.<br /><br /> The Anonymous authentication module uses the token to impersonate the built-in account. When `PassAnonymousToken` is `false`, the token will not be passed. **Note:**  The IUSR anonymous user account replaces the IIS_MachineName anonymous account. The IUSR account can be used by IIS or other applications. It does not have any privileges assigned to it during setup.|  
|`ProcessModel`|A [ProcessModelSettings](../../reference/admin/processmodelsettings-class1.md) object that defines the configuration settings for IIS worker processes.|  
|`QueueLength`|A read/write `uint32` value that indicates the number of requests the universal listener will queue for an application pool before rejecting further requests. The default is 1000. When the limit is exceeded, the listener rejects additional requests with a 503 (service unavailable) error.|  
|`Recycling`|A [RecyclingSettings](../../reference/admin/recyclingsettings-class1.md) object that defines the recycling configuration settings for application pools and worker processes.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `ApplicationPoolDefaults` property of the [Server](../../reference/admin/server-class1.md) class.  
  
 The following table lists the possible values for the `ManagedPipelineMode` property. The default is 0 (`Integrated`).  
  
|Value|Keyword|Description|  
|-----------|-------------|-----------------|  
|0|`Integrated`|The managed pipeline runs in Integrated mode.|  
|1|`Classic`|The managed pipeline runs in ISAPI mode.|  
  
## Inheritance Hierarchy  
 [EmbeddedObject](../../reference/admin/embeddedobject-class1.md)  
  
 `ApplicationPoolElementDefaults`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [ApplicationPool Class](../../reference/admin/applicationpool-class1.md)   
 [EmbeddedObject Class](../../reference/admin/embeddedobject-class1.md)   
 [Server Class](../../reference/admin/server-class1.md)