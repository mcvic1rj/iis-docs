---
title: "Object Class1 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: e0c0f720-51e6-d244-eb1a-e4551d427019
caps.latest.revision: 20
author: "shirhatti"
manager: "wpickett"
---
# Object Class1
Serves as a base class from which to derive the primary namespace objects for the [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)] WMI provider.  
  
## Syntax  
  
```vbs  
class Object  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 This class contains no properties.  
  
## Subclasses  
 The following table lists the classes derived from the `Object` class.  
  
|Name|Description|  
|----------|-----------------|  
|[AppDomain](../../reference/admin/appdomain-class.md)|Represents an IIS application domain.|  
|[ApplicationPool](../../reference/admin/applicationpool-class1.md)|Represents an IIS application pool.|  
|[ConfiguredObject](../../reference/admin/configuredobject-class1.md)|Acts as a base type for namespace objects whose configuration can be specified in configuration sections.|  
|[HttpRequest](../../reference/admin/httprequest-class.md)|Represents an HTTP request in a worker process.|  
|[Server](../../reference/admin/server-class1.md)|Exposes default configuration settings for applications, application pools, Web sites, and virtual directories on a Web server running IIS.|  
|[SSLBinding](../../reference/admin/sslbinding-class.md)|Represents a Secure Sockets Layer (SSL) binding.|  
|[WorkerProcess](../../reference/admin/workerprocess-class2.md)|Represents a Windows Process Activation Service (WAS) worker process (w3wp.exe).|  
  
## Remarks  
 Although the `Object` class is not directly useful for scripting, it enables the WMI CIM Studio tool to conveniently group `WebAdministration` classes. CIM Studio is a utility that you can use to view WMI classes, properties, qualifiers, and instances. It is available from the [Microsoft Download Center](http://go.microsoft.com/fwlink/?LinkId=72615) as part of WMITools.exe suite of WMI Administrative Tools.  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [WMI Provider](../../reference/admin/wmi-provider.md)   
 [ConfiguredObject Class](../../reference/admin/configuredobject-class1.md)   
 [EmbeddedObject Class](../../reference/admin/embeddedobject-class1.md)   
 [ObjectConfigurationAssociation Class](../../reference/admin/objectconfigurationassociation-class.md)   
 [ObjectContainerAssociation Class](../../reference/admin/objectcontainerassociation-class1.md)