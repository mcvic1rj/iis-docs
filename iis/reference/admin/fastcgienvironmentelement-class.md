---
title: "FastCgiEnvironmentElement Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 29bb4657-10a8-4665-9390-f07818bab9da
caps.latest.revision: 6
author: "shirhatti"
manager: "wpickett"
---
# FastCgiEnvironmentElement Class
Configures environment variables for the process executable program of an application pool.  
  
## Syntax  
  
```vbs  
class FastCgiEnvironmentElement : CollectionElement  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `FastCgiEnvironmentElement` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Name`|A read/write `string` value that specifies the name of an environment variable. The key property.|  
|`Value`|A read/write `string` that specifies a value for the `Name` property.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `EnvironmentVariables` array property of the [FastCgiEnvironmentSettings](../../reference/admin/fastcgienvironmentsettings-class.md) class.  
  
 You can use this class to control PHP process recycling behavior by specifying the *PHP_FCGI_MAX_REQUESTS* environment variable for the `Name` property and a value for the `Value` property.  
  
 The FastCGI process recycling behavior is controlled by the `InstanceMaxRequests` configuration property of the [FastCgiApplicationElement](../../reference/admin/fastcgiapplicationelement-class.md) class. The `InstanceMaxRequests` property specifies the maximum number of requests that a FastCGI process will handle before it recycles. Similarly, in PHP, the value of the  *PHP_FCGI_MAX_REQUESTS* environment variable controls process recycling.  
  
 You can fine-tune the stability and performance of Web applications by configuring these properties. Shorter recycling periods can improve Web application stability, whereas longer recycling periods can improve Web application performance. If you use longer recycling periods, then fewer CPU cycles will be spent on starting and stopping php-cgi.exe processes. This improves performance, but at the risk of stability.  
  
 By setting `InstanceMaxRequests` to a value that is smaller or equal to that of *PHP_FCGI_MAX_REQUESTS*, you can ensure that the native PHP process recycling logic will never be activated. If you do not set these parameters, the default settings will be used.  
  
> [!NOTE]
>  The default setting for `InstanceMaxRequests` is 200; the default setting on most PHP builds for *PHP_FCGI_MAX_REQUESTS* is 500. Although the default values are sufficient for development scenarios on a stand-alone computer, you should fine-tune these settings when you deploy FastCGI and PHP in a shared hosting environment.  
  
## Inheritance Hierarchy  
 [CollectionElement](../../reference/admin/collectionelement-class.md)  
  
 `FastCgiEnvironmentElement`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [CollectionElement Class](../../reference/admin/collectionelement-class.md)   
 [FastCgiApplicationElement Class](../../reference/admin/fastcgiapplicationelement-class.md)   
 [FastCgiEnvironmentSettings Class](../../reference/admin/fastcgienvironmentsettings-class.md)   
 [FastCgiSection Class](../../reference/admin/fastcgisection-class.md)