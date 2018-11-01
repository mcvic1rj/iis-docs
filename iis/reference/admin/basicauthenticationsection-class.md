---
title: "BasicAuthenticationSection Class | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 55a1ded7-a01b-c38c-b661-ea61ab261400
caps.latest.revision: 24
author: "shirhatti"
manager: "wpickett"
---
# BasicAuthenticationSection Class
Configures Basic authentication.  
  
## Syntax  
  
```vbs  
class BasicAuthenticationSection : ConfigurationSection  
```  
  
## Methods  
 The following table lists the methods exposed by the `BasicAuthenticationSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|[GetAllowDefinition](../../reference/admin/configurationsection-getallowdefinition-method.md)|(Inherited from [ConfigurationSection](../../reference/admin/configurationsection-class1.md).)|  
|[GetAllowLocation](../../reference/admin/configurationsection-getallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
|[RevertToParent](../../reference/admin/configurationsection-reverttoparent-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowDefinition](../../reference/admin/configurationsection-setallowdefinition-method.md)|(Inherited from `ConfigurationSection`.)|  
|[SetAllowLocation](../../reference/admin/configurationsection-setallowlocation-method.md)|(Inherited from `ConfigurationSection`.)|  
  
## Properties  
 The following table lists the properties exposed by the `BasicAuthenticationSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|`DefaultLogonDomain`|A read/write `string` value that specifies the default domain that the server uses to authenticate users when the client does not specify a domain in the logon dialog box.|  
|`Enabled`|A read/write `boolean` value. `true` if Basic authentication is enabled; otherwise, `false`. The default is `false`.|  
|`Location`|(Inherited from `ConfigurationSection`.) A key property.|  
|`LogonMethod`|A read/write `sint32` enumeration that specifies the default logon method for a local user. The type of logon will determine whether the resulting token can also be used remotely. The possible values are listed later in the Remarks section.|  
|`Path`|(Inherited from `ConfigurationSection`.) A key property.|  
|`Realm`|A read/write `string` value that contains the name of the realm that is used by the client for credential caching.|  
|`SectionInformation`|(Inherited from `ConfigurationSection`.)|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 The following table contains the possible values for the `LogonMethod` property. The default is 3 (`ClearText`). For more information, see the [LogonUserEx](http://go.microsoft.com/fwlink/?LinkId=60074) function.  
  
|Value|Keyword|Description|  
|-----------|-------------|-----------------|  
|0|`Interactive`|This logon type is intended for users who will be interactively using the computer.|  
|1|`Batch`|This logon type is intended for batch servers, where processes may be executing on behalf of a user without their direct intervention. Credentials are not cached for this logon type.|  
|2|`Network`|This logon type is intended for high performance servers to authenticate plaintext passwords. Credentials are not cached for this logon type.|  
|3|`ClearText`|This logon type preserves the name and password in the authentication package, which allows the server to make connections to other network servers while impersonating the client.|  
  
## Example  
 The following example displays the `BasicAuthenticationSection` configuration for the default Web site.  
  
```  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = _  
    GetObject("winmgmts:root\WebAdministration")  
  
' Get the Basic authentication section for the default Web site.  
Set oSite = oWebAdmin.Get("Site.Name='Default Web Site'")  
oSite.GetSection "BasicAuthenticationSection", oBasicAuth  
  
' Display the path and location.  
WScript.Echo "Basic Authentication Settings"  
WScript.Echo "-----------------------------"  
WScript.Echo "Path: " & oBasicAuth.Path  
WScript.Echo "Location: " & oBasicAuth.Location  
WScript.Echo   
  
' Display the Enabled, DefaultLogonDomain, Realm, and   
' LogonMethod properties.  
WScript.Echo "Enabled: " & _  
    "[" & oBasicAuth.Enabled & "]"  
  
WScript.Echo "DefaultLogonDomain: " & _  
    "[" & oBasicAuth.DefaultLogonDomain & "]"  
  
WScript.Echo "Realm: " & "[" & oBasicAuth.Realm & "]"  
  
WScript.Echo "LogonMethod: " &  _  
    "[" & GetLogonMethodText(oBasicAuth.LogonMethod) & "]"  
  
' Translate the LogonMethod enumeration values to text.  
Function GetLogonMethodText(LogonMethodValue)  
    Select Case LogonMethodValue  
        Case 0  
            GetLogonMethodText = "Interactive"  
        Case 1  
            GetLogonMethodText = "Batch"  
        Case 2  
            GetLogonMethodText = "Network"  
        Case 3  
            GetLogonMethodText = "ClearText"  
        Case Else  
            GetLogonMethodText = "Undefined enumeration."  
    End Select  
End Function  
  
```  
  
## Inheritance Hierarchy  
 [ConfigurationSection](../../reference/admin/configurationsection-class1.md)  
  
 `BasicAuthenticationSection`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [AnonymousAuthenticationSection Class](../../reference/admin/anonymousauthenticationsection-class1.md)   
 [AuthenticationSection Class](../../reference/admin/authenticationsection-class1.md)   
 [ClientCertificateMappingAuthenticationSection Class](../../reference/admin/clientcertificatemappingauthenticationsection-class.md)   
 [DigestAuthenticationSection Class](../../reference/admin/digestauthenticationsection-class.md)   
 [FormsAuthenticationConfiguration Class](../../reference/admin/formsauthenticationconfiguration-class.md)   
 [FormsAuthenticationCredentials Class](../../reference/admin/formsauthenticationcredentials-class.md)   
 [FormsAuthenticationUser Class](../../reference/admin/formsauthenticationuser-class.md)   
 [IisClientCertificateMappingAuthenticationSection Class](../../reference/admin/iisclientcertificatemappingauthenticationsection-class.md)   
 [PassportAuthentication Class](../../reference/admin/passportauthentication-class.md)   
 [WindowsAuthenticationSection Class](../../reference/admin/windowsauthenticationsection-class.md)   
 [LogonUserEx](http://go.microsoft.com/fwlink/?LinkId=60074)