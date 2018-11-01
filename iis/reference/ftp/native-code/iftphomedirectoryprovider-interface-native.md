---
title: "IFtpHomeDirectoryProvider Interface (Native) | Microsoft Docs"
ms.custom: ""
ms.date: "09/06/2017"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: b7bc3cf4-96eb-4cb2-ad39-1323d581da3f
caps.latest.revision: 8
author: "shirhatti"
ms.author: "robmcm"
manager: "wpickett"
---
# IFtpHomeDirectoryProvider Interface (Native)
Provides an interface to implement returning the physical path for a user's home directory.  
  
## Syntax  
  
```cpp#  
interface IFtpHomeDirectoryProvider : IUknown  
```  
  
## Methods  
 The following table lists the methods exposed by the `IFtpHomeDirectoryProvider` interface.  
  
|||  
|-|-|  
|Name|Definition|  
|[IFtpHomeDirectoryProvider::GetUserHomeDirectoryData Method](../../../reference/ftp/native-code/iftphomedirectoryprovider-getuserhomedirectorydata-method.md)|Returns the physical path of the home directory for a user.|  
  
## Example  
 The following code example illustrates using the `IFtpHomeDirectoryProvider` interface to create a custom home directory module for the FTP service that returns a specific home directory.  
  
```  
public:  
   STDMETHOD(GetUserHomeDirectoryData)(  
      LPWSTR pszSessionId,  
      LPWSTR pszSiteName,  
      LPWSTR pszUserName,  
      LPWSTR * ppszHomeDirectoryData)  
   {  
      // Note: You would add your own custom logic here.  
      HRESULT hr = S_OK;  
      WCHAR wszPath[MAX_PATH] = L"";  
  
      // Calculate the user's home directory based on their user name.  
      hr = StringCchPrintf(wszPath,_countof(wszPath),  
         L"\\\\?\\C:\\ftpusers\\%s",pszUserName);  
      // Return an error if a failure occurs.  
      if (FAILED(hr))  
      {  
         return hr;  
      }  
  
      // Allocate a block of memory for the user's home directory.  
      LPWSTR wszHomeDirectoryData =  
          (LPWSTR)CoTaskMemAlloc(_countof(wszPath) * sizeof(WCHAR));  
      // Return an error if a failure occurs.  
      if (wszHomeDirectoryData == NULL)  
      {  
         return E_OUTOFMEMORY;  
      }  
  
      // Copy the user's home directory into the memory block.  
      hr = StringCchCopy(wszHomeDirectoryData,  
         _countof(wszPath), wszPath);  
      // Return an error if a failure occurs.  
      if (FAILED(hr))  
      {  
      return hr;  
      }  
  
      // Return the user's home directory.  
       (*ppszHomeDirectoryData) = wszHomeDirectoryData;  
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