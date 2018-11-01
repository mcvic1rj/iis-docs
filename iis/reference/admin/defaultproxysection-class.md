---
title: "DefaultProxySection Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: d2318b31-4a59-2850-0eb2-c8a5230a1b64
caps.latest.revision: 15
author: "shirhatti"
manager: "wpickett"
---
# DefaultProxySection Class
Configures Web proxy server defaults.  
  
## Syntax  
  
```vbs  
class DefaultProxySection : ConfigurationSectionWithCollection  
```  
  
## Methods  
 The following table lists the methods exposed by the `DefaultProxySection` class.  
  
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
 The following table lists the properties exposed by the `DefaultProxySection` class.  
  
|Name|Description|  
|----------|-----------------|  
|`BypassList`|A [BypassListSettings](../../reference/admin/bypasslistsettings-class.md) value that represents resources that bypass the Web proxy server.|  
|`Enabled`|A read/write `boolean` value. `true` if a Web proxy will be used; otherwise, `false`. The default is `true`.|  
|`Location`|(Inherited from `ConfigurationSection`.) A key property.|  
|`Module`|A [ModuleSettings](../../reference/admin/modulesettings-class.md) value that specifies type, assembly, and version information for custom Web proxy implementations.|  
|`Path`|(Inherited from `ConfigurationSection`.) A key property.|  
|`Proxy`|A [ProxySettings](../../reference/admin/proxysettings-class.md) value that identifies Web proxy servers to use for resources that are not specified in the `BypassList` property.|  
|`SectionInformation`|(Inherited from `ConfigurationSection`.)|  
|`UseDefaultCredentials`|A read/write `boolean` value. `true` if default credentials will be used to access a Web proxy server; otherwise, `false`. The default is `false`.|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Inheritance Hierarchy  
 [ConfigurationSection](../../reference/admin/configurationsection-class1.md)  
  
 [ConfigurationSectionWithCollection](../../reference/admin/configurationsectionwithcollection-class.md)  
  
 `DefaultProxySection`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [BypassElement Class](../../reference/admin/bypasselement-class.md)   
 [BypassListSettings Class](../../reference/admin/bypasslistsettings-class.md)   
 [ConfigurationSectionWithCollection Class](../../reference/admin/configurationsectionwithcollection-class.md)   
 [ModuleSettings Class](../../reference/admin/modulesettings-class.md)   
 [ProxySettings Class](../../reference/admin/proxysettings-class.md)