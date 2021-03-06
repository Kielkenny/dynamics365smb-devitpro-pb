---
author: edupont04
title: "RESTOREARCHIVEDATA Method"
ms.custom: na
ms.date: 10/01/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: dynamics365-business-central
ms.author: edupont
redirect_url: /dynamics365/business-central/dev-itpro/developer/methods-auto/library
---

 

# RESTOREARCHIVEDATA Method
Restores archived data for a specified table of an extension during installation.

## Syntax  

```  
[Ok :=] RESTOREARCHIVEDATA (TableNo[, RunTriggers])  
```  

#### Parameters

*TableNo*  
Type: Integer  

Specifies the ID of the extension table whose archive data you want to restore.  

*RunTriggers*  
Type: Boolean  

Specifies whether to run the table and field triggers to run when restoring the data to the table.  

If the parameter is **true**, triggers will be run; if **false** or omitted, the triggers will not be run.  

## Return Value  
Type: Boolean  

**true**, if the archived data was restored for the specified table; otherwise **false**.  

If you omit this optional return value and if archived data cannot be restored for the specified table, then a run-time error occurs. If you include a return value, then it is assumed that you will handle any errors and no run-time error occurs, even though the archived data is not restored.

## Remarks
You use this method as part of the upgrade code for an extension, where it is called from the `OnNavAppUpgradePerDatabase()` or `OnNavAppUpgradePerCompany()` system methods. When an extension is uninstalled, the data in application tables of the extension is automatically stored into a set of special tables so that the data is still preserved. With the RESTOREARCHIVEDATA method, you can restore the archived data to the application table of the new version of an extension when it is installed. 

