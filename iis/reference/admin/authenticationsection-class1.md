---
title: "AuthenticationSection Class1 | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: e8860ac3-d303-c19e-a3df-f1b1456f42ba
caps.latest.revision: 23
author: "shirhatti"
manager: "wpickett"
---
# AuthenticationSection Class1
Configures [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] authentication.  
  
## Syntax  
  
```vbs  
class AuthenticationSection : ConfigurationSectionWithCollection  
```  
  
## Methods  
 The following table lists the methods exposed by the `AuthenticationSection` class.  
  
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
 The following table lists the properties exposed by the `AuthenticationSection` class.  
  
|Name|Description|  
|----------|-----------------|  
|`Forms`|A [FormsAuthenticationConfiguration](../../reference/admin/formsauthenticationconfiguration-class.md) value that configures Forms authentication for the Web application.|  
|`Location`|(Inherited from `ConfigurationSection`.) A key property.|  
|`Mode`|A read/write `sint32` value that specifies the authentication mode for the Web application. The possible values are listed later in the Remarks section.|  
|`Passport`|A [PassportAuthentication](../../reference/admin/passportauthentication-class.md) value that contains a URL to which the authentication request will be redirected.|  
|`Path`|(Inherited from `ConfigurationSection`.) A key property.|  
|`SectionInformation`|(Inherited from `ConfigurationSection`.)|  
  
## Subclasses  
 This class contains no subclasses.  
  
## Remarks  
 The following table lists the possible values for the `Mode` property. The default is 1 (`Windows`).  
  
|Value|Keyword|Description|  
|-----------|-------------|-----------------|  
|0|`None`|Specifies no authentication.|  
|1|`Windows`|Specifies Windows as the authentication mode. This mode applies when [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] uses the Basic, Digest, Integrated Windows (NTLM/Kerberos), or Client Certificate Mapping authentication methods.|  
|2|`Passport`|Specifies Microsoft Passport Network authentication as the authentication mode.|  
|3|`Forms`|Specifies [!INCLUDE[vstecasp](../../reference/includes/vstecasp-md.md)] Forms authentication as the authentication mode.|  
  
## Example  
 The following example displays the authentication mode for the default Web site. If the authentication mode is `Passport`, the redirect URL is displayed. If the mode is `Forms`, the corresponding information is displayed.  
  
```  
' Connect to the WMI WebAdministration namespace.  
Set oWebAdmin = _  
    GetObject("winmgmts:root\WebAdministration")  
  
' Get the authentication section.  
Set oSite = oWebAdmin.Get("Site.Name='Default Web Site'")  
oSite.GetSection "AuthenticationSection", oAuthSection  
  
' Display the path and location.  
WScript.Echo "Path: " & oAuthSection.Path  
WScript.Echo "Location: " & oAuthSection.Location  
WScript.Echo   
  
' Get the authentication mode and display it in text.  
strAuthMode = ModeText(oAuthSection.Mode)  
WScript.Echo "Authentication Mode: " &  _  
    "[ " & strAuthMode & " ]"  
  
' If the mode is Passport or Forms, display the   
' additional information.  
If strAuthMode = "Passport" Then  
  
    WScript.Echo "Passport URL: " & "[" & _  
        oAuthSection.Passport.RedirectUrl & "]"  
  
ElseIf strAuthMode = "Forms" then  
  
    DisplayFormsAuthSettings(oAuthSection.Forms)  
  
End If  
  
' Convert the Mode enumeration values to text.  
Function ModeText(enumValue)  
    Select Case enumValue  
        Case 0  
            ModeText = "None"  
        Case 1  
            ModeText = "Windows"  
        Case 2  
            ModeText = "Passport"  
        Case 3  
            ModeText = "Forms"  
        Case Else  
            ModeText = "Undefined enumeration value."  
    End Select  
End Function  
  
' Display the Forms authentication settings.  
Sub DisplayFormsAuthSettings(oFormsAuthConfig)  
    WScript.Echo vbCrLf & "Forms Authentication Settings"  
    WScript.Echo "-----------------------------"  
  
    WScript.Echo "Cookieless: [ " & _  
        CookielessText(oFormsAuthConfig.Cookieless) & " ]"  
  
    WScript.Echo "Default Url: [ " & _  
        oFormsAuthConfig.DefaultUrl & " ]"  
  
    WScript.Echo "Domain: [ " & _  
        oFormsAuthConfig.Domain & " ]"  
  
    WScript.Echo "EnableCrossAppRedirects: [" & _  
        oFormsAuthConfig.EnableCrossAppRedirects & " ]"  
  
    WScript.Echo "LoginUrl: [ " & _  
        oFormsAuthConfig.LoginUrl & " ]"  
  
    WScript.Echo "Name: [ " & _  
        oFormsAuthConfig.Name & " ]"  
  
    WScript.Echo "Path: [ " & _  
        oFormsAuthConfig.Path & " ]"  
  
    WScript.Echo "Protection: [ " & _  
        ProtectionText(oFormsAuthConfig.Protection) & " ]"  
  
    WScript.Echo "RequireSSL: [ " & _  
        oFormsAuthConfig.RequireSSL & " ]"  
  
    WScript.Echo "SlidingExpiration: [ " & _  
        oFormsAuthConfig.SlidingExpiration & " ]"  
  
    WScript.Echo "Timeout: [ " & _  
        oFormsAuthConfig.Timeout & " ]"  
  
    DisplayCredentials(oFormsAuthConfig.Credentials)  
  
End Sub  
  
' Convert the Cookieless enumeration values to text.  
Function CookielessText(enumValue)  
    Select Case enumValue  
        Case 0  
            CookielessText = "UseUri"  
        Case 1  
            CookielessText = "UseCookies"  
        Case 2  
            CookielessText = "AutoDetect"  
        Case 3  
            CookielessText = "UseDeviceProfile"  
        Case Else  
            CookielessText = "Undefined enumeration value."  
    End Select  
End Function  
  
' Convert the Protection enumeration values to text.  
Function ProtectionText(enumValue)  
    Select Case enumValue  
        Case 0  
            ProtectionText = "All"  
        Case 1  
            ProtectionText = "None"  
        Case 2  
            ProtectionText = "Encryption"  
        Case 3  
            ProtectionText = "Validation"  
        Case Else  
            ProtectionText = "Undefined enumeration value."  
    End Select  
End Function  
  
' Display the Forms authentication credentials.  
Sub DisplayCredentials(FA_Credentials)  
    WScript.Echo vbCrLf & "Forms Authentication Credentials"  
    WScript.Echo "--------------------------------"  
    WScript.Echo "Password Format: " & _  
        PwdFormatText(FA_Credentials.PasswordFormat) & VbCrLf  
  
    For Each FormsAuthUser In FA_Credentials.Credentials  
        WScript.Echo "    Name: [ " & FormsAuthUser.Name & " ]"  
        WScript.Echo "Password: [ " & _  
            FormsAuthUser.Password& " ]"  
        WScript.Echo  
    Next  
End Sub  
  
' Convert the PasswordFormat enumeration values to text.  
Function PwdFormatText(enumValue)  
    Select Case enumValue  
        Case 0  
            PwdFormatText = "Clear"  
        Case 1  
            PwdFormatText = "SHA1"  
        Case 2  
            PwdFormatText = "MD5"  
        Case Else  
            PwdFormatText = "Undefined enumeration value."  
    End Select  
End Function  
  
```  
  
## Inheritance Hierarchy  
 [ConfigurationSection](../../reference/admin/configurationsection-class1.md)  
  
 [ConfigurationSectionWithCollection](../../reference/admin/configurationsectionwithcollection-class.md)  
  
 `AuthenticationSection`  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winvista](../../reference/admin/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../reference/admin/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../reference/admin/includes/iis100-md.md)]|  
|MOF file|WebAdministration.mof|  
  
## See Also  
 [AnonymousAuthenticationSection Class](../../reference/admin/anonymousauthenticationsection-class1.md)   
 [BasicAuthenticationSection Class](../../reference/admin/basicauthenticationsection-class.md)   
 [ClientCertificateMappingAuthenticationSection Class](../../reference/admin/clientcertificatemappingauthenticationsection-class.md)   
 [ConfigurationSectionWithCollection Class](../../reference/admin/configurationsectionwithcollection-class.md)   
 [DigestAuthenticationSection Class](../../reference/admin/digestauthenticationsection-class.md)   
 [FormsAuthenticationConfiguration Class](../../reference/admin/formsauthenticationconfiguration-class.md)   
 [FormsAuthenticationCredentials Class](../../reference/admin/formsauthenticationcredentials-class.md)   
 [FormsAuthenticationUser Class](../../reference/admin/formsauthenticationuser-class.md)   
 [IisClientCertificateMappingAuthenticationSection Class](../../reference/admin/iisclientcertificatemappingauthenticationsection-class.md)   
 [PassportAuthentication Class](../../reference/admin/passportauthentication-class.md)   
 [WindowsAuthenticationSection Class](../../reference/admin/windowsauthenticationsection-class.md)