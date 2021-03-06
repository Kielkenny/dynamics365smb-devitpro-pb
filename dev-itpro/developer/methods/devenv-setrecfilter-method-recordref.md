---
title: "SETRECFILTER Method (RecordRef)"
ms.custom: na
ms.date: 10/01/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: dynamics365-business-central
ms.assetid: 8c5d6a10-c8e9-492e-9f66-bbf07895d230
caps.latest.revision: 12
redirect_url: /dynamics365/business-central/dev-itpro/developer/methods-auto/library
---

 

# SETRECFILTER Method (RecordRef)
Sets a filter on a record that is referred to by a RecordRef.  

## Syntax  

```  

RecordRef.SETRECFILTER  
```  

#### Parameters  
 *RecordRef*  
 Type: RecordRef  

 The RecordRef used to identify the record on which you want to place a filter.  

## Remarks  
 This method works the same as the [SETRECFILTER Method \(Record\)](devenv-SETRECFILTER-Method-Record.md).  

## Example  
 The following example opens the Customer table as a RecordRef variable that is named MyRecordRef. The SETRECFILTER method sets the values in the current key of the current record as a record filter. The [GETFILTERS Method \(RecordRef\)](devenv-GETFILTERS-Method-RecordRef.md) retrieves the filters that have been set and displays them in a message box. No. is displayed because the filter is set on the No. field, which is the current key. This example requires that you create the following global variables and text constant.  

|Variable name|DataType|  
|-------------------|--------------|  
|MyRecordRef|RecordRef|  
|varFilters|Test|  

|Text constant name|ENU value|  
|------------------------|---------------|  
|Text000|The filter is set on the %1 field.|  

```  

MyRecordRef.OPEN(DATABASE::Customer);  
MyRecordRef.SETRECFILTER;  
varFilters := MyRecordRef.GETFILTERS;  
MESSAGE(Text000, varFilters);  
```  

## See Also  
 [RecordRef Data Type](../datatypes/devenv-RecordRef-Data-Type.md)
