---
title: "IPSecuritySection Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: aec39e60-f2d7-6a9c-3ef4-83d4b4dce196
caps.latest.revision: 23
author: "shirhatti"
manager: "wpickett"
---
# IPSecuritySection Class
Configures access to Web server content based on IP address-related information.  
  
## Syntax  
  
```vbs  
class IPSecuritySection : ConfigurationSectionWithCollection  
```  
  
## Methods  
 The following table lists the methods exposed by the `IPSecuritySection` class.  
  
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
 The following table lists the properties exposed by the `IPSecuritySection` class.  
  
|Name|Description|  
|----------|-----------------|  
|`AllowUnlisted`|A read/write `boolean` value. `true` if access is granted to IP address, domain name, and subnet mask combinations not specified in the `IPAddressFilters` property; otherwise, `false`. The default is `true`. This property is processed last in ordering. **Note:**  If you are using the local host address (127.0.0.1) and the `AllowUnlisted` property is set to `false`, users will be denied access unless 127.0.0.1 is specified as an `IPSecurity` entry with its `Allowed` property set to `true`.|  
|`EnableReverseDNS`|A read/write `boolean` value. `true` if a reverse DNS lookup is performed to verify the domain name to which an IP address resolves; otherwise, `false`. The default is `false`. **Note:**  When this property is enabled, IIS must resolve the DNS name of each client IP address. A single DNS lookup may require several seconds, and IIS is required to wait until the domain name can be verified. You should take this behavior into consideration when planning large-scale implementations.|  
|`IpSecurity`|An array of read/write [IPAddressFilterElement](../../reference/admin/ipaddressfilterelement-class.md) values that specify IP address, domain name, and subnet mask combinations to which access is granted or denied. **Note:**  The entries in this property are processed in order. A best practice is to place the entries to be denied first in the list.|  
|`Location`|(Inherited from `ConfigurationSection`.) A key property.|  
|`Path`|(Inherited from `ConfigurationSection`.) A key property.|  
|`SectionInformation`|(Inherited from `ConfigurationSection`.)|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 In IIS 6.0, URLs were granted or denied individually. However, in [!INCLUDE[iisver](../../reference/admin/includes/iisver-md.md)], access rules are inherited and their semantics are merged to determine final access, which is why the ordering of rules is important.  
  
## Example  
 The following example displays `IPSecuritySection` settings for the default Web site.  
  
```  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = _  
    GetObject("winmgmts:root\WebAdministration")  
  
' Get the IP security section for the default Web site.  
Set oSite = oWebAdmin.Get("Site.Name='Default Web Site'")  
oSite.GetSection "IPSecuritySection", oSection  
  
' Display the Path and Location properties.  
WScript.Echo "=============================="  
WScript.Echo "IP Security Section Properties"  
WScript.Echo "=============================="  
WScript.Echo "Path: " & oSection.Path  
WScript.Echo "Location: " & oSection.Location  
WScript.Echo  
  
' Display the AllowUnlisted and   
' EnableReverseDns properties.  
WScript.Echo "AllowUnlisted: " & oSection.AllowUnlisted  
WScript.Echo "EnableReverseDns: " & _  
                oSection.EnableReverseDns  
WScript.Echo  
  
' Display the IP and domain restrictions.  
WScript.Echo "--------------------------"  
WScript.Echo "IP and domain restrictions"  
WScript.Echo "--------------------------"  
For Each oIPAddressFilter In oSection.IpSecurity  
    WScript.Echo "IpAddress: " & oIPAddressFilter.IpAddress      
    WScript.Echo "DomainName: " & _  
        oIPAddressFilter.DomainName  
    WScript.Echo "SubnetMask: " & _  
        oIPAddressFilter.SubnetMask  
    WScript.Echo "Allowed: " & oIPAddressFilter.Allowed  
    WScript.Echo  
Next  
  
```  
  
## Inheritance Hierarchy  
 [ConfigurationSection](../../reference/admin/configurationsection-class1.md)  
  
 [ConfigurationSectionWithCollection](../../reference/admin/configurationsectionwithcollection-class.md)  
  
 `IPSecuritySection`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [ConfigurationSectionWithCollection Class](../../reference/admin/configurationsectionwithcollection-class.md)   
 [IPAddressFilterElement Class](../../reference/admin/ipaddressfilterelement-class.md)