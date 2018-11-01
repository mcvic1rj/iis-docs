---
title: "ObjectContainerAssociation Class1 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 40a82997-34e7-1626-d580-a3d6b90ce7f6
caps.latest.revision: 21
author: "shirhatti"
manager: "wpickett"
---
# ObjectContainerAssociation Class1
Associates an object with its child objects.  
  
## Syntax  
  
```vbs  
class ObjectContainerAssociation  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `ObjectContainerAssociation` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Container`|An `object ref` value that represents a containing object.|  
|`Element`|An `object ref` value that represents the object within the container.|  
  
## Subclasses  
  
|Name|Description|  
|----------|-----------------|  
|[ApplicationContainsVirtualDirectory](../../reference/admin/applicationcontainsvirtualdirectory-class2.md)|Provides a relationship between an IIS application and its virtual directories.|  
|[ApplicationPoolContainsApplication](../../reference/admin/applicationpoolcontainsapplication-class1.md)|Provides a relationship between an application pool and its applications.|  
|[ApplicationPoolContainsProcess](../../reference/admin/applicationpoolcontainsprocess-class1.md)|Provides a relationship between an application pool and its worker processes.|  
|[ServerContainsApplicationPool](../../reference/admin/servercontainsapplicationpool-class1.md)|Provides a relationship between a Web server and its application pools.|  
|[ServerContainsSite](../../reference/admin/servercontainssite-class1.md)|Provides a relationship between a Web server and its Web sites.|  
|[ServerContainsSSLBinding](../../reference/admin/servercontainssslbinding-class.md)|Provides a relationship between a Secure Sockets Layer (SSL) binding and a Web server that is running IIS.|  
|[SiteContainsApplication](../../reference/admin/sitecontainsapplication-class1.md)|Provides a relationship between a Web site and its applications.|  
|[SiteUsesSSLBinding](../../reference/admin/siteusessslbinding-class1.md)|Provides a relationship between an IIS Web site and a Secure Sockets Layer (SSL) binding.|  
|[WorkerProcessContainsAppDomain](../../reference/admin/workerprocesscontainsappdomain-class2.md)|Provides a relationship between a worker process and its application domains.|  
  
## Remarks  
 This base class allows one member of the [Object](../../reference/admin/object-class1.md) class to contain another member of the `Object` class. The containing object (for example, [Site](../../reference/admin/site-class1.md)) is called a *container*, and the contained object (for example, [Application](../../reference/admin/application-class1.md)) is called an *element*. A container object may contain one or more elements. `ObjectContainerAssociation` classes are useful because they enable you to create intuitive parent/child associations that would otherwise be difficult to implement in the relatively flat WMI namespace.  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [AppDomain Class](../../reference/admin/appdomain-class.md)   
 [Application Class](../../reference/admin/application-class1.md)   
 [ApplicationPool Class](../../reference/admin/applicationpool-class1.md)   
 [ApplicationContainsVirtualDirectory Class](../../reference/admin/applicationcontainsvirtualdirectory-class2.md)   
 [ApplicationPoolContainsApplication Class](../../reference/admin/applicationpoolcontainsapplication-class1.md)   
 [ApplicationPoolContainsProcess Class](../../reference/admin/applicationpoolcontainsprocess-class1.md)   
 [ConfiguredObject Class](../../reference/admin/configuredobject-class1.md)   
 [EmbeddedObject Class](../../reference/admin/embeddedobject-class1.md)   
 [WMI Provider](../../reference/admin/wmi-provider.md)   
 [Object Class](../../reference/admin/object-class1.md)   
 [Site Class](../../reference/admin/site-class1.md)   
 [SiteContainsApplication Class](../../reference/admin/sitecontainsapplication-class1.md)   
 [VirtualDirectory Class](../../reference/admin/virtualdirectory-class2.md)   
 [WorkerProcess Class](../../reference/admin/workerprocess-class2.md)   
 [WorkerProcessContainsAppDomain Class](../../reference/admin/workerprocesscontainsappdomain-class2.md)