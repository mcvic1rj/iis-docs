---
title: "StringElement Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: e376d4dc-5ebe-6a12-b192-06cd5b8450a5
caps.latest.revision: 12
author: "shirhatti"
manager: "wpickett"
---
# StringElement Class
Contains a unique string that belongs to an array that forms a property on a class in the WMI provider for IIS.  
  
## Syntax  
  
```vbs  
class StringElement : CollectionElement  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `StringElement` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Value`|A required unique read/write `string` value that belongs to an array of similar strings that forms a property on an IIS WMI provider class. The relevant classes and properties are listed later in the Remarks section. The key property.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 The following table lists classes in the IIS WMI provider that have properties that are implemented as arrays of `StringElement` instances.  
  
|Class|Property|Description|  
|-----------|--------------|-----------------|  
|[AuthenticationProviderSettings](../../reference/admin/authenticationprovidersettings-class.md)|`Providers`|An array of security support providers that are used for Integrated Windows authentication.|  
|[FileSettings](../../reference/admin/filesettings-class1.md)|`Files`|A read/write array of `string` values that contain the names of the files that the Web server returns to clients by default.|  
|[TraceUrlSettings](../../reference/admin/traceurlsettings-class.md)|`HttpTracing`|An array of elements that configure tracing for specific types of requests.|  
  
## Inheritance Hierarchy  
 [CollectionElement](../../reference/admin/collectionelement-class.md)  
  
 `StringElement`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [AuthenticationProviderSettings Class](../../reference/admin/authenticationprovidersettings-class.md)   
 [CollectionElement Class](../../reference/admin/collectionelement-class.md)   
 [DefaultDocumentSection Class](../../reference/admin/defaultdocumentsection-class1.md)   
 [FileSettings Class](../../reference/admin/filesettings-class1.md)   
 [HttpTracingSection Class](../../reference/admin/httptracingsection-class.md)   
 [TraceUrlSettings Class](../../reference/admin/traceurlsettings-class.md)   
 [WindowsAuthenticationSection Class](../../reference/admin/windowsauthenticationsection-class.md)