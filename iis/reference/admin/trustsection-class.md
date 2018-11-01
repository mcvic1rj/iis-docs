---
title: "TrustSection Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 4fdfb984-ac44-52c5-b709-b0dd2b08a942
caps.latest.revision: 21
author: "shirhatti"
manager: "wpickett"
---
# TrustSection Class
Configures the level of code-access security that is applied to an application.  
  
## Syntax  
  
```vbs  
class TrustSection : ConfigurationSection  
```  
  
## Methods  
 The following table lists the methods exposed by the `TrustSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|[GetAllowDefinition](../../reference/admin/configurationsection-getallowdefinition-method.md)|(Inherited from [ConfigurationSection](../../reference/admin/configurationsection-class1.md).)|  
|[GetAllowLocation](../../reference/admin/configurationsection-getallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
|[RevertToParent](../../reference/admin/configurationsection-reverttoparent-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowDefinition](../../reference/admin/configurationsection-setallowdefinition-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowLocation](../../reference/admin/configurationsection-setallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
  
## Properties  
 The following table lists the properties exposed by the `TrustSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Level`|A required read/write `string` value that specifies the trust level under which the Web application will run. Each trust level is mapped to an individual XML policy file by using a [TrustLevel](../../reference/admin/trustlevel-class.md) configuration element. The policy file lists the set of permissions that are granted by each trust level. For more information about [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] and policy files, see [ASP.NET Trust Levels and Policy Files](http://go.microsoft.com/fwlink/?LinkId=69328).<br /><br /> The `Level` property can contain a user-defined value if there is a matching security policy mapping defined in a `T``rustLevel` element in the [SecurityPolicySection](../../reference/admin/securitypolicysection-class.md) class, or it can contain one of the possible values listed later in the Remarks section.|  
|`Location`|(Inherited from `ConfigurationSection`.) A key property.|  
|`OriginUrl`|An optional read/write `string` value that specifies a URL for use with the `WebPermission` permission that is granted in `High` and `Medium` trust. If present, this can be used for some permissions, such as `WebRequest`, that allow connectivity only to specific URLs that are specified by a `WebPermission`.|  
|`Path`|(Inherited from `ConfigurationSection`.) A key property.|  
|`ProcessRequestInApplicationTrust`|A read/write `boolean` value. `true` if page requests are automatically restricted to the permissions that are configured in the trust policy file that is applied to the [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] application; otherwise, `false`. The default is `true`.<br /><br /> Trust policy files are specified in `TrustLevel` configuration elements in the `SecurityPolicySection` class. You can apply a single trust policy to an [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] application by using the `Level` property. **Note:**  If the `ProcessRequestInApplicationTrust` property is set to `false`, [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] requests can potentially execute under `Full` trust, even if the `Level` property specifies a different trust level. Unless there are specific reasons for doing this, do not reset this property from the default of `true`. This property is new in the [!INCLUDE[dnprdnlong](../../reference/admin/includes/dnprdnlong-md.md)].|  
|`SectionInformation`|(Inherited from `ConfigurationSection`.)|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 The possible values for the `Level` property are listed in the following table. The default is `Full` (no restrictions).  
  
|Value|Description|  
|-----------|-----------------|  
|`Full`|Specifies unrestricted permissions. Grants the [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] application permissions to access any resource that is subject to operating system security. All privileged operations are supported. This setting is named `Unrestricted` in the [System.Web.AspNetHostingPermissionLevel](http://go.microsoft.com/fwlink/?LinkId=69330) enumeration.|  
|`High`|Specifies a high level of code access security, which means that the application cannot do any of the following things:<br /><br /> -   Call unmanaged code.<br />-   Call serviced components.<br />-   Write to the event log.<br />-   Access Microsoft Windows Message Queuing queues.<br />-   Access ODBC, OLE DB, or Oracle data sources.|  
|`Medium`|Specifies a medium level of code access security, which means that, in addition to the restrictions for `High`, the [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] application cannot do any of the following things:<br /><br /> -   Access files outside the application directory.<br />-   Access the registry.|  
|`Low`|Specifies a low level of code access security, which means that, in addition to the restrictions for `Medium`, the application cannot do any of the following things:<br /><br /> -   Write to the file system.<br />-   Call the [System.Security.CodeAccessPermission.Assert](http://go.microsoft.com/fwlink/?LinkId=69334) method to expand permissions to resources.|  
|`Minimal`|Specifies a minimal level of code access security, which means that the application has only execute permission.|  
  
## Inheritance Hierarchy  
 [ConfigurationSection](../../reference/admin/configurationsection-class1.md)  
  
 `TrustSection`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 <xref:System.Web.Configuration.SystemWebSectionGroup.Trust%2A?displayProperty=fullName>   
 <xref:System.Web.Configuration.TrustSection?displayProperty=fullName>   
 [System.Web.AspNetHostingPermissionLevel Enumeration](http://go.microsoft.com/fwlink/?LinkId=69330)   
 [ASP.NET Trust Levels and Policy Files](http://go.microsoft.com/fwlink/?LinkId=69328)   
 [ConfigurationSection Class](../../reference/admin/configurationsection-class1.md)   
 [TrustLevel Class](../../reference/admin/trustlevel-class.md)   
 [System.Net.WebPermission Class](http://go.microsoft.com/fwlink/?LinkId=69331)   
 [System.Net.WebRequest Class](http://go.microsoft.com/fwlink/?LinkId=69332)