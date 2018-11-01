---
title: "SmtpNetworkSettings Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 56fb1598-1a9e-3fa0-08c4-2789202f1d4b
caps.latest.revision: 14
author: "shirhatti"
manager: "wpickett"
---
# SmtpNetworkSettings Class
Configures Simple Mail Transfer Protocol (SMTP) network settings.  
  
## Syntax  
  
```vbs  
class SmtpNetworkSettings : EmbeddedObject  
```  
  
## Methods  
 This class contains no methods.  
  
## Properties  
 The following table lists the properties exposed by the `SmtpNetworkSettings` class.  
  
|Name|Description|  
|----------|-----------------|  
|`DefaultCredentials`|A read/write `boolean` value. `true` if default user credentials are used to access an SMTP server; otherwise, `false`. The default is `false`.|  
|`Host`|A read/write `string` value that specifies the name of the SMTP server.|  
|`Password`|A read/write `string` value that specifies the user password with which to connect to an SMTP server. **Note:**  The `DefaultCredentials` property takes precedence over the `UserName` and `Password` properties. The `UserName` and `Password` properties are used only if `DefaultCredentials` is set to `false`.|  
|`Port`|A read/write `sint32` value that specifies the port that SMTP clients use to connect to an SMTP server. The default is 25.|  
|`UserName`|A read/write `string` value that specifies the user name with which to connect to an SMTP server.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Instances of this class are contained in the `Network` property of the [SmtpMailSettingsSection](../../reference/admin/smtpmailsettingssection-class.md) class.  
  
## Inheritance Hierarchy  
 [EmbeddedObject](../../reference/admin/embeddedobject-class1.md)  
  
 `SmtpNetworkSettings`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [EmbeddedObject Class](../../reference/admin/embeddedobject-class1.md)   
 [SmtpMailSettingsSection Class](../../reference/admin/smtpmailsettingssection-class.md)