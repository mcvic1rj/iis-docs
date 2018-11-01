---
title: "TypeElement Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 8103c618-5040-16d7-3708-0b5a74b3b95e
caps.latest.revision: 15
author: "shirhatti"
manager: "wpickett"
---
# TypeElement Class
Specifies a type in an array property on a Web-service-related WMI class.  
  
## Syntax  
  
```vbs  
class TypeElement : CollectionElement  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `TypeElement` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Type`|A required unique read/write `string` value that contains type information. The key property. **Note:**  The type reference is formed as follows (items in brackets are not required): *Namespace*.*Typename*, *Assemblyname*[,] [Version=*x*,] [Culture=*y*,] [PublicKeyToken=*z*] (for example, "ExampleNamespace.ExampleType, Example.Assembly, Version=%ASSEMBLY_VERSION%, Culture=neutral, PublicKeyToken=%MICROSOFT_PUBLICKEY%").|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the following array properties of the classes listed.  
  
|Class|Property|  
|-----------|--------------|  
|[ServiceDescriptionFormatSettings](../../reference/admin/servicedescriptionformatsettings-class.md)|`ServiceDescriptionFormatExtensionTypes`|  
|[SoapExtensionImporterTypesSettings](../../reference/admin/soapextensionimportertypessettings-class.md)|`SoapExtensionImporterTypes`|  
|[SoapExtensionReflectorTypesSettings](../../reference/admin/soapextensionreflectortypessettings-class.md)|`SoapExtensionReflectorTypesSettings`|  
  
## Inheritance Hierarchy  
 [CollectionElement](../../reference/admin/collectionelement-class.md)  
  
 `TypeElement`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [CollectionElement Class](../../reference/admin/collectionelement-class.md)   
 [ServiceDescriptionFormatSettings Class](../../reference/admin/servicedescriptionformatsettings-class.md)   
 [SoapExtensionImporterTypesSettings Class](../../reference/admin/soapextensionimportertypessettings-class.md)   
 [IIS 7.0: SoapExtensionReflectorTypesSettings Class](1e8f1231-c816-4b11-8019-865b42870a26%207fffcc59)   
 [WebServicesSection Class](../../reference/admin/webservicessection-class.md)