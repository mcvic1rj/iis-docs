---
title: "ConformanceWarning Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 6143dc15-7a1d-c00b-94ed-a446964cb705
caps.latest.revision: 17
author: "shirhatti"
manager: "wpickett"
---
# ConformanceWarning Class
Exposes a Web Services Interoperability (WS-I) specification to which a Web service declares that it conforms.  
  
## Syntax  
  
```vbs  
class ConformanceWarning : CollectionElement  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `ConformanceWarning` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Name`|A read-only `sint32` enumeration that represents the Web Services Interoperability (WS-I) specification to which a Web service declares that it conforms. The possible values are listed later in the Remarks section. The key property.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `ConformanceWarnings` array property of the [ConformanceWarningSettings](../../reference/admin/conformancewarningsettings-class.md) class.  
  
 The following table lists the possible values for the `Name` property. Currently, the only WS-I profile supported in the [!INCLUDE[dnprdnshort](../../reference/admin/includes/dnprdnshort-md.md)] is Basic Profile Version 1.1 (BasicProfile 1_1).  
  
|Value|Keyword|Description|  
|-----------|-------------|-----------------|  
|0|`None`|The Web service claims no conformance to a WS-I specification.|  
|1|`BasicProfile1_1`|The Web service claims conformance with the WS-I Basic Profile 1.1 set of nonproprietary Web service specifications.|  
  
## Inheritance Hierarchy  
 [CollectionElement](../../reference/admin/collectionelement-class.md)  
  
 `ConformanceWarning`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [CollectionElement Class](../../reference/admin/collectionelement-class.md)   
 [ConformanceWarningSettings Class](../../reference/admin/conformancewarningsettings-class.md)   
 [WebServicesSection Class](../../reference/admin/webservicessection-class.md)   
 [Basic Profile Version 1.1 (WS-I)](http://go.microsoft.com/fwlink/?LinkId=69313)