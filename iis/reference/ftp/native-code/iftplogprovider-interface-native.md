---
title: "IFtpLogProvider Interface (Native) | Microsoft Docs"
ms.custom: ""
ms.date: "09/06/2017"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 164e8ebe-cae0-4e23-af04-34ef3f43954b
caps.latest.revision: 9
author: "shirhatti"
ms.author: "robmcm"
manager: "wpickett"
---
# IFtpLogProvider Interface (Native)
Provides an interface for logging FTP activity.  
  
## Syntax  
  
```cpp#  
interface IFtpLogProvider : IUknown  
```  
  
## Methods  
 The following table lists the methods exposed by the `IFtpLogProvider` interface.  
  
|||  
|-|-|  
|Name|Definition|  
|[IFtpLogProvider::Log Method](../../../reference/ftp/native-code/iftplogprovider-log-method.md)|Performs logging activity for the `IFtpLogProvider` interface.|  
  
## Example  
 The following code example illustrates how to use the `IFtpLogProvider` interface to create a custom logging module for the FTP service.  
  
```  
public:  
   STDMETHOD(Log)(LOGGING_PARAMETERS * pLoggingParameters)  
   {  
      // Note: You would add your own custom logic here.  
      HRESULT hr = S_OK;  
      DWORD dwResult;  
      HANDLE hFile;  
      char szLogEntry[256]="";  
      const DWORD FILE_WRITE_TO_END_OF_FILE = 0xffffffff;  
  
      OVERLAPPED Overlapped = { 0 };  
      Overlapped.Offset = FILE_WRITE_TO_END_OF_FILE;  
      Overlapped.OffsetHigh = -1;  
  
      // Retrieve the current date and time for the log entry.  
      SYSTEMTIME CurrentTime;  
      GetSystemTime(&CurrentTime);  
  
      // Open the log file for output.  
      hFile = CreateFile(  
         L"\\\\?\\C:\\logfiles\\myftpsite\\myftplog.log",  
         GENERIC_WRITE,  
         FILE_SHARE_READ,  
         NULL,  
         OPEN_ALWAYS,  
         FILE_ATTRIBUTE_NORMAL | FILE_FLAG_WRITE_THROUGH,  
         NULL);  
  
      // Return an error if a failure occurs.  
      if (hFile == INVALID_HANDLE_VALUE)  
      {  
         hr = HRESULT_FROM_WIN32(GetLastError());  
         goto EXIT;  
      }  
  
      // Format the log entry.  
      hr = StringCchPrintfA(  
         szLogEntry,256,  
         "%04d-%02d-%02d\t%02d:%02d:%02d\t%S\t%d\r\n",  
         CurrentTime.wYear,CurrentTime.wMonth,CurrentTime.wDay,  
         CurrentTime.wHour,CurrentTime.wMinute,CurrentTime.wSecond,  
         pLoggingParameters->pszCommand,  
         pLoggingParameters->FtpStatus);  
  
      // Test for error.  
      if (FAILED(hr))  
      {  
         // Return the error if a failure occurs.  
         hr = HRESULT_FROM_WIN32(GetLastError());  
         goto EXIT;  
      }  
  
      // Write the log entry to the log file.  
      if(!WriteFile(hFile, szLogEntry,  
         strlen(szLogEntry), &dwResult, &Overlapped))        
      {  
         // Return an error if a failure occurs.  
         hr = HRESULT_FROM_WIN32(GetLastError());  
         goto EXIT;  
      }  
  
EXIT:  
      // Close the log file if it is open.  
      if(CloseHandle(hFile)==0)  
      {  
         // Return an error if a failure occurs.  
         hr = HRESULT_FROM_WIN32(GetLastError());  
      }  
      return hr;  
   }  
```  
  
## Requirements  
  
|||  
|-|-|  
|Type|Description|  
|Client|-   [!INCLUDE[iis75](../../../reference/admin/includes/iis75-md.md)] on                                          [!INCLUDE[win7](../../../reference/admin/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../../reference/admin/includes/iis80-md.md)] on                                          [!INCLUDE[win8](../../../reference/admin/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../../reference/admin/includes/iis100-md.md)] on                                          [!INCLUDE[win10](../../../reference/admin/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis75](../../../reference/admin/includes/iis75-md.md)] on                                          [!INCLUDE[winsrv2008r2](../../../reference/admin/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../../reference/admin/includes/iis80-md.md)] on                                          [!INCLUDE[winsrv2012](../../../reference/admin/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../../reference/admin/includes/iis85-md.md)] on                                          [!INCLUDE[winsrv2012r2](../../../reference/admin/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../../reference/admin/includes/iis100-md.md)] on                                          [!INCLUDE[winsrv2016](../../../reference/admin/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../../reference/admin/includes/iis70-md.md)],                                          [!INCLUDE[iis75](../../../reference/admin/includes/iis75-md.md)],                                          [!INCLUDE[iis80](../../../reference/admin/includes/iis80-md.md)],                                          [!INCLUDE[iis85](../../../reference/admin/includes/iis85-md.md)],                                          [!INCLUDE[iis100](../../../reference/admin/includes/iis100-md.md)]|  
|Reference|ftpext.tlb|  
  
## See Also  
 [LOGGING_PARAMETERS Structure](../../../reference/ftp/native-code/logging-parameters-structure.md)