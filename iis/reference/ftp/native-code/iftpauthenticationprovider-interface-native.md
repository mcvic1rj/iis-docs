---
title: "IFtpAuthenticationProvider Interface (Native) | Microsoft Docs"
ms.custom: ""
ms.date: "09/06/2017"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 843eaeff-6349-465d-958f-12d940763122
caps.latest.revision: 8
author: "shirhatti"
ms.author: "robmcm"
manager: "wpickett"
---
# IFtpAuthenticationProvider Interface (Native)
Provides an interface for authentication checks.  
  
## Syntax  
  
```cpp#  
interface IFtpAuthenticationProvider : IUknown  
```  
  
## Methods  
 The following table lists the methods exposed by the `IFtpAuthenticationProvider` interface.  
  
|||  
|-|-|  
|Name|Definition|  
|[IFtpAuthenticationProvider::AuthenticateUser Method](../../../reference/ftp/native-code/iftpauthenticationprovider-authenticateuser-method.md)|Checks to see whether a user name and password are valid.|  
  
## Example  
 The following code example illustrates how to use the `IFtpAuthenticationProvider` interface to create a custom authentication module that implements user name checks for the FTP service.  
  
```  
public:  
   STDMETHOD(AuthenticateUser)(LPWSTR pszSessionId,  
      LPWSTR pszSiteName,  
      LPWSTR pszUserName,  
      LPWSTR pszPassword,  
      LPWSTR * ppszCanonicalUserName,  
      long * pfAuthenticated)  
      {  
      // Note: You would add your own custom logic here.  
      *ppszCanonicalUserName = pszUserName;  
  
      CString strUserName = L"MyUser";  
      CString strPassword = L"MyPassword";  
  
      // Verify that the user name and password are valid.  
      // In this example, the user name is case-insensitive  
      // and the password is case-sensitive.  
      if ((strUserName.CompareNoCase(pszUserName)==0) &&  
          (strPassword.Compare(pszPassword)==0))  
      {  
         *pfAuthenticated = TRUE;  
      }  
      else  
      {  
         *pfAuthenticated = FALSE;  
   }  
      return S_OK;  
   }  
```  
  
## Requirements  
  
|||  
|-|-|  
|Type|Description|  
|Client|-   [!INCLUDE[iis75](../../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[win7](../../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[win8](../../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[win10](../../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis75](../../../reference/admin/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../../reference/admin/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../../reference/admin/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../../reference/admin/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../../reference/admin/includes/iis70-md.md)], [!INCLUDE[iis75](../../../reference/admin/includes/iis75-md.md)], [!INCLUDE[iis80](../../../reference/admin/includes/iis80-md.md)], [!INCLUDE[iis85](../../../reference/admin/includes/iis85-md.md)], [!INCLUDE[iis100](../../../reference/admin/includes/iis100-md.md)]|  
|Reference|ftpext.tlb|  
  
## See Also  
 [IFtpRoleProvider Interface](../../../reference/ftp/native-code/iftproleprovider-interface-native.md)