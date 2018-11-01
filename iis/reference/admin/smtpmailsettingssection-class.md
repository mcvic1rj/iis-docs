---
title: "SmtpMailSettingsSection Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 9d122b83-5fc7-477e-2496-3292c6d1b0ba
caps.latest.revision: 17
author: "shirhatti"
manager: "wpickett"
---
# SmtpMailSettingsSection Class
Contains Simple Mail Transfer Protocol (SMTP) configuration settings.  
  
## Syntax  
  
```vbs  
class SmtpMailSettingsSection : ConfigurationSection  
```  
  
## Methods  
 The following table lists the methods exposed by the `SmtpMailSettingsSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|[GetAllowDefinition](../../reference/admin/configurationsection-getallowdefinition-method.md)|(Inherited from [ConfigurationSection](../../reference/admin/configurationsection-class1.md).)|  
|[GetAllowLocation](../../reference/admin/configurationsection-getallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
|[RevertToParent](../../reference/admin/configurationsection-reverttoparent-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowDefinition](../../reference/admin/configurationsection-setallowdefinition-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowLocation](../../reference/admin/configurationsection-setallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
  
## Properties  
 The following table lists the properties exposed by the `SmtpMailSettingsSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|`DeliveryMethod`|A read/write `sint32` value that specifies the SMTP delivery method. The possible values are listed later in the Remarks section.|  
|`From`|A read/write `string` value that sets the **From** field in e-mails that are sent to users by using the SMTP mail APIs.|  
|`Location`|(Inherited from `ConfigurationSection`.) A key property.|  
|`Network`|A read/write [SmtpNetworkSettings](../../reference/admin/smtpnetworksettings-class.md) value that represents a network element in the SMTP configuration file.|  
|`Path`|(Inherited from `ConfigurationSection`.) A key property.|  
|`SectionInformation`|(Inherited from `ConfigurationSection`.)|  
|`SpecifiedPickupDirectory`|A read/write [SmtpSpecifiedPickupDirectorySettings](../../reference/admin/smtpspecifiedpickupdirectorysettings-class.md) value that specifies the pickup directory that will be used by the SMTP client.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 The following table lists the possible values for the `DeliveryMethod` property. The default is 0 (`Network`).  
  
|Value|Keyword|Description|  
|-----------|-------------|-----------------|  
|0|`Network`|E-mail is sent through the network to an SMTP server.|  
|1|`SpecifiedPickupDirectory`|E-mail is copied to the pickup directory that is used by a local IIS server for delivery.|  
|2|`PickupDirectoryFromIis`|E-mail is copied to the directory specified by the `SpecifiedPickupDirectory` property for delivery by an external application.|  
  
## Inheritance Hierarchy  
 [ConfigurationSection](../../reference/admin/configurationsection-class1.md)  
  
 `SmtpMailSettingsSection`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [ConfigurationSection Class](../../reference/admin/configurationsection-class1.md)   
 [SmtpNetworkSettings Class](../../reference/admin/smtpnetworksettings-class.md)   
 [SmtpSpecifiedPickupDirectorySettings Class](../../reference/admin/smtpspecifiedpickupdirectorysettings-class.md)