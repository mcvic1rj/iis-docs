---
title: "MembershipSection Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: f8b2a0e9-0187-8227-fa8c-7bd6f3de477c
caps.latest.revision: 17
author: "shirhatti"
manager: "wpickett"
---
# MembershipSection Class
Validates user credentials and manages user settings.  
  
## Syntax  
  
```vbs  
class MembershipSection : ConfigurationSectionWithCollection  
```  
  
## Methods  
 The following table lists the methods exposed by the `MembershipSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|[Add](../../reference/admin/configurationsectionwithcollection-add-method.md)|(Inherited from [ConfigurationSectionWithCollection](../../reference/admin/configurationsectionwithcollection-class.md).)|  
|[Clear](../../reference/admin/configurationsectionwithcollection-clear-method.md)|(Inherited from `ConfigurationSectionWithCollection`.)|  
|[Get](../../reference/admin/configurationsectionwithcollection-get-method.md)|(Inherited from `ConfigurationSectionWithCollection`.)|  
|[GetAllowDefinition](../../reference/admin/configurationsection-getallowdefinition-method.md)|(Inherited from [ConfigurationSection](../../reference/admin/configurationsection-class1.md).)|  
|[GetAllowLocation](../../reference/admin/configurationsection-getallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
|[Remove](../../reference/admin/configurationsectionwithcollection-remove-method.md)|(Inherited from `ConfigurationSectionWithCollection`.)|  
|[RevertToParent](../../reference/admin/configurationsection-reverttoparent-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowDefinition](../../reference/admin/configurationsection-setallowdefinition-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowLocation](../../reference/admin/configurationsection-setallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
  
## Properties  
 The following table lists the properties exposed by the `MembershipSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|`DefaultProvider`|A read/write `string` value that specifies the default membership provider for an application. The default is "AspNetSqlMembershipProvider".|  
|`HashAlgorithmType`|A read/write `string` value that identifies a custom algorithm that is used to hash passwords. If no value is specified, the hash algorithm specified in the `Validation` property of the [MachineKeySection](../../reference/admin/machinekeysection-class.md) class is used. **Note:**  The [!INCLUDE[dnprdnshort](../../reference/admin/includes/dnprdnshort-md.md)] enables you to configure custom cryptography classes by using the [\<cryptographySettings>](http://go.microsoft.com/fwlink/?LinkId=70955) configuration section. The `HashAlgorithmType` property must match the name attribute of the [\<nameEntry>](http://go.microsoft.com/fwlink/?LinkId=70956) element in a [\<cryptoNameMapping>](http://go.microsoft.com/fwlink/?LinkId=70957) element. For more information, see [Mapping Algorithm Names to Cryptography Classes](http://go.microsoft.com/fwlink/?LinkId=70954).|  
|`Location`|(Inherited from `ConfigurationSection`.) A key property.|  
|`Path`|(Inherited from `ConfigurationSection`.) A key property.|  
|`Providers`|A [ProvidersSettings](../../reference/admin/providerssettings-class.md) value that specifies membership providers for an [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] application (Web.config level) or for all [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] applications (Machine.config level).|  
|`SectionInformation`|(Inherited from `ConfigurationSection`.)|  
|`UserIsOnlineTimeWindow`|A read/write `datetime` value that specifies the time interval after the last-activity date/time stamp for a user during which the user is considered online. The default is 15 minutes.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Inheritance Hierarchy  
 [ConfigurationSection](../../reference/admin/configurationsection-class1.md)  
  
 [ConfigurationSectionWithCollection](../../reference/admin/configurationsectionwithcollection-class.md)  
  
 `MembershipSection`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 <xref:System.Web.Security.Membership?displayProperty=fullName>   
 [ConfigurationSectionWithCollection Class](../../reference/admin/configurationsectionwithcollection-class.md)   
 [ProvidersSettings Class](../../reference/admin/providerssettings-class.md)   
 [Mapping Algorithm Names to Cryptography Classes](http://go.microsoft.com/fwlink/?LinkId=70954)