---
title: "ProviderFactoryElement Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 6cee1598-11a6-3211-c3e1-24b5e68e46e8
caps.latest.revision: 13
author: "shirhatti"
manager: "wpickett"
---
# ProviderFactoryElement Class
Contains configuration settings for an [!INCLUDE[ado_whidbey_long](../../reference/admin/includes/ado-whidbey-long-md.md)] provider factory.  
  
## Syntax  
  
```vbs  
class ProviderFactoryElement : CollectionElement  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `ProviderFactoryElement` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Description`|A read/write `string` value that contains the verbose name of the data provider specified in the `Name` and `Invariant` properties (for example, ".NET Framework Data Provider for ODBC").|  
|`Invariant`|A read/write `string` value that contains the invariant name of the provider that is specified in the `Description` and `Name` properties (for example, "System.Data.Odbc"). The invariant name can be passed to the [System.Data.Common.DBProviderFactories.GetFactory](http://go.microsoft.com/fwlink/?LinkId=70912) method to obtain a [System.Data.Common.DBProviderFactory](http://go.microsoft.com/fwlink/?LinkId=70913) object for the provider.|  
|`Name`|A required unique read/write `string` value that contains the name of a data provider (for example, "ODBC Data Provider"). The key property.|  
|`Type`|A read/write `string` value that specifies the type for the provider specified in the `Name`, `Description`, and `Invariant` properties (for example, "System.Data.Odbc.OdbcFactory, System.Data, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089").|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `DbProviderFactories` array property of the [DbProviderFactorySettings](../../reference/admin/dbproviderfactorysettings-class.md) class.  
  
## Inheritance Hierarchy  
 [CollectionElement](../../reference/admin/collectionelement-class.md)  
  
 `ProviderFactoryElement`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [CollectionElement Class](../../reference/admin/collectionelement-class.md)   
 [DbProviderFactorySettings Class](../../reference/admin/dbproviderfactorysettings-class.md)   
 [SystemDataSection Class](../../reference/admin/systemdatasection-class.md)   
 [ADO.NET 2.0 Feature Matrix](http://go.microsoft.com/fwlink/?LinkId=70915)