---
title: "ConfigurationRedirectionSection Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: bdea9a0b-25f3-4d68-8ad1-8ec80312fb67
caps.latest.revision: 10
author: "shirhatti"
manager: "wpickett"
---
# ConfigurationRedirectionSection Class
Configures the location of the ApplicationHost.config and Administration.config files.  
  
## Syntax  
  
```vbs  
class ConfigurationRedirectionSection : ConfigurationSection  
```  
  
## Methods  
 The following table lists the methods exposed by the `ConfigurationRedirectionSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|[GetAllowDefinition](../../reference/admin/configurationsection-getallowdefinition-method.md)|(Inherited from [ConfigurationSection](../../reference/admin/configurationsection-class1.md).)|  
|[GetAllowLocation](../../reference/admin/configurationsection-getallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
|[RevertToParent](../../reference/admin/configurationsection-reverttoparent-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowDefinition](../../reference/admin/configurationsection-setallowdefinition-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowLocation](../../reference/admin/configurationsection-setallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
  
## Properties  
 The following table lists the properties exposed by the `ConfigurationRedirectionSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Enabled`|A read/write `boolean` value. `true` if the location of the ApplicationHost.config and Administration.config files is redirected to the location specified by the `RedirectionPath` property; otherwise, `false.` The default is `false`.|  
|`Location`|(Inherited from `ConfigurationSection`.) A key property.|  
|`Password`|A case-sensitive read/write encrypted `string` value that specifies the password of the identity that the configuration system impersonates when it reads the configuration files at the location specified by the `RedirectionPath` property. The default is "[enc:RsaProtectedConfigurationProvider::enc]".|  
|`Path`|(Inherited from `ConfigurationSection`.) A key property.|  
|`RedirectionPath`|A read/write `string` value that specifies the path of the location (for example, a UNC share) of the redirected ApplicationHost.config and Administration.config files. The default is an empty string ("").|  
|`SectionInformation`|(Inherited from `ConfigurationSection`.)|  
|`UserName`|A read/write `string` value that specifies the user name of the identity that the configuration system impersonates when it reads the configuration files at the location specified by the `RedirectionPath` property. The default is an empty string ("").|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 Configuration redirection settings are stored in the Redirection.config file. By default, this file is located in the *%windir%*\system32\inetsrv\config directory.  
  
## Inheritance Hierarchy  
 [ConfigurationSection](../../reference/admin/configurationsection-class1.md)  
  
 `ConfigurationRedirectionSection`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [ConfigurationSection Class](../../reference/admin/configurationsection-class1.md)