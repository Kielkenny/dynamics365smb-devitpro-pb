---
title: "DownloadFromStream Method"
ms.author: solsen
ms.custom: na
ms.date: 11/06/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: "dynamics365-business-central"
author: solsen
---
[//]: # (START>DO_NOT_EDIT)
[//]: # (IMPORTANT:Do not edit any of the content between here and the END>DO_NOT_EDIT.)
[//]: # (Any modifications should be made in the .xml files in the ModernDev repo.)
# DownloadFromStream Method
Sends a file from server computer to the client computer. The client computer is the computer that is running the Windows client or the computer that is running the browser that accesses the web client.

## Syntax
```
[Ok := ]  File.DownloadFromStream(InStream: InStream, DialogTitle: String, ToFolder: String, ToFilter: String, var ToFile: Text)
```
> [!NOTE]  
> This method can be invoked without specifying the data type name.  
## Parameters
*InStream*  
&emsp;Type: [InStream](../instream/instream-data-type.md)  
  
*DialogTitle*  
&emsp;Type: [String](../string/string-data-type.md)  
The title that you want to display in the dialog box for downloading the file. This parameter is not supported by the web client. The title is determined by the end-user's browser.
          
*ToFolder*  
&emsp;Type: [String](../string/string-data-type.md)  
The default folder in which to save the file to be downloaded. The folder name is displayed in the dialog box for downloading the file. The folder can be changed by the user. This parameter is not supported by the web client. By default, files are saved to the default download location that is configured in the end-user's browser.
          
*ToFilter*  
&emsp;Type: [String](../string/string-data-type.md)  
The type of file that can be downloaded to the client computer. The type is displayed in the dialog box for downloading the file. This parameter is not supported by the web client.
          
*ToFile*  
&emsp;Type: [Text](../text/text-data-type.md)  
The name to give the downloaded file. This is the default file name that is shown in the dialog box for downloading the file. This value, can be changed by the user.  


## Return Value
*Ok*  
&emsp;Type: [Boolean](../boolean/boolean-data-type.md)  
**true** if the operation was successful; otherwise **false**.  If you omit this optional return value and the operation does not execute successfully, a runtime error will occur.    


[//]: # (IMPORTANT: END>DO_NOT_EDIT)

## Remarks  

<!-- This method is not fully supported by the [!INCLUDE[d365fin_web_md](../includes/d365fin_web_md.md)] on devices that run Apple iOS, such as iPad.--> 

> [!NOTE]  
> On devices that run Apple iOS, such as iPad, you can only download a file if the Apple iOS device on which you are downloading the file has an application that supports the file type.  

 The business logic runs on the computer that is running [!INCLUDE[d365fin_server_md](../../includes/d365fin_server_md.md)] and not on the client. Files are created on a [!INCLUDE[d365fin_md](../../includes/d365fin_md.md)] service and not locally on the client computer. When you write code, you must consider where files are created.  

 Use [UPLOAD Method \(File\)](../../methods/devenv-upload-method-file.md) and [UPLOADINTOSTREAM Method \(File\)](../../methods/devenv-uploadintostream-method-file.md) to send a file from a client to a [!INCLUDE[d365fin_server_md](../../includes/d365fin_server_md.md)] instance.  

 Use [DOWNLOAD Method \(File\)](../../methods/devenv-download-method-file.md) and [DOWNLOADFROMSTREAM Method \(FILE\)](../../methods/devenv-downloadfromstream-method-file.md) to send a file from a [!INCLUDE[d365fin_server_md](../../includes/d365fin_server_md.md)] instance to a client.  

 We recommend that you use the methods in codeunit 419, File Management, to upload and download files.  

## Example  
 This example requires that you create the following variables.  

|Name|DataType|  
|----------|--------------|  
|TempFile|File|  
|NewStream|InStream|  
|ToFileName|Variant|  

```  
TempFile.CREATETEMPFILE();  
TempFile.WRITE('abc');  
TempFile.CREATEINSTREAM(NewStream);  
ToFileName := 'SampleFile.txt';  
DOWNLOADFROMSTREAM(NewStream,'Export','','All Files (*.*)|*.*',ToFileName)  
```  


## See Also
[File Data Type](file-data-type.md)  
[Getting Started with AL](../../devenv-get-started.md)  
[Developing Extensions](../../devenv-dev-overview.md)