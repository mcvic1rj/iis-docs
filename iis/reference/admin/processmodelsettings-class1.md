---
title: "ProcessModelSettings Class1 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: acf029ed-e4b4-bde7-3b94-fc42b4ddaca0
caps.latest.revision: 26
author: "shirhatti"
manager: "wpickett"
---
# ProcessModelSettings Class1
Exposes configuration settings for IIS worker processes.  
  
## Syntax  
  
```vbs  
class ProcessModelSettings : EmbeddedObject  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `ProcessModelSettings` class.  
  
|Name|Description|  
|----------|-----------------|  
|`IdentityType`|A read/write `sint32` value that designates the account type under which an application pool will run. The possible values are listed later in the Remarks section.|  
|`IdleTimeout`|A read/write `datetime` value that specifies the amount of time, in minutes, that a worker process should continue to run when no new requests are received and the worker process is not currently processing requests. The default is 20. After the specified time passes, the worker process notifies the World Wide Web Publishing Service (WWW service), which then terminates the worker process.|  
|`LoadUserProfile`|A read/write `boolean` value. `true` if the Windows Process Activation Service (WAS) should load the user profile for a worker process; otherwise, `false`. The default is `true`. This setting is application pool specific.|  
|`ManualGroupMembership`|A read/write `boolean` value. `true` if access rights to content directories or resources need to be manually configured through Access Control Lists (ACLs); otherwise, `false`. The default is `false`. A value of `false` means that the built-in IIS_IUSRS group membership will be used.|  
|`MaxProcesses`|A read/write `uint32` value that specifies the maximum number of worker processes in an application pool. The default is 1.|  
|`Password`|A read/write `string` value that specifies the default password for the account that IIS uses as the identity for newly created out-of-process COM+ applications. **Note:**  The default values of the `Password` and `UserName` properties are set when IIS is installed. The values match the user name and password in the corresponding Microsoft Windows user account that is established at installation.|  
|`PingingEnabled`|A read/write `boolean` value. `true` if the WWW service should monitor the health of a worker process by periodically verifying that it is running; otherwise, `false`. The `PingingInterval` property specifies the time delay between these verifications. The default is `true`.|  
|`PingInterval`|A read/write `datetime` value that specifies the time delay, in seconds, between the health-monitoring requests that the WWW service sends to a worker process. The default is 30.|  
|`PingResponseTime`|A read/write `datetime` value that specifies the amount of time, in seconds, that a worker process is given to respond to a health-monitoring request. The default is 90. After the time limit is exceeded, the WWW service terminates the worker process.|  
|`ShutdownTimeLimit`|A read/write `datetime` value that specifies the amount of time, in seconds, that the WWW service should wait after a recycle threshold has been reached to terminate a worker process. The specified time enables a worker process to complete existing requests. The default is 90.|  
|`StartupTimeLimit`|A read/write `datetime` value that specifies the amount of time, in seconds, that the WWW service should wait for a worker process to start and report its ready status to the WWW service. The default is 90.|  
|`UserName`|A read/write `string` value that specifies the default user name for the account that IIS uses as the identity for newly created out-of-process COM+ applications. **Note:**  The default values of the `UserName` and `Password` properties are set when IIS is installed. The values match the user name and password in the corresponding Microsoft Windows user account that is established at installation. **Important:**  If you change the value of `UserName`, you must change it to a value that matches a valid Windows user account, and you must also change `Password` to the password for that Windows account.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `ProcessModel` property of the [ApplicationPool](../../reference/admin/applicationpool-class1.md) class and the [ApplicationPoolElementDefaults](../../reference/admin/applicationpoolelementdefaults-class1.md) class.  
  
 For more information on the Windows Management Instrumentation (WMI) date/time format, see [CIM_DATETIME](http://go.microsoft.com/fwlink/?LinkId=57551).  
  
 The following table contains the possible values and account types for the `IdentityType` property. The default type is 2 (NetworkService).  
  
|Value|Account type|  
|-----------|------------------|  
|0|Local System|  
|1|Local Service|  
|2|Network Service|  
|3|Specific User|  
  
## Inheritance Hierarchy  
 [EmbeddedObject](../../reference/admin/embeddedobject-class1.md)  
  
 `ProcessModelSettings`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [ApplicationPool Class](../../reference/admin/applicationpool-class1.md)   
 [ApplicationPoolElementDefaults Class](../../reference/admin/applicationpoolelementdefaults-class1.md)   
 [EmbeddedObject Class](../../reference/admin/embeddedobject-class1.md)   
 [WorkerProcess Class](../../reference/admin/workerprocess-class2.md)