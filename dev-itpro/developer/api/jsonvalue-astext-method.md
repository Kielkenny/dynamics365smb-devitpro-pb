---
title: "AsText Method"
ms.author: solsen
ms.custom: na
ms.date: 10/01/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: "dynamics365-business-central"
ms.assetid: 620f0e32-eadc-43e9-8f6e-8fc0b12c3aaf
caps.latest.revision: 9
manager: edupont
author: SusanneWindfeldPedersen
redirect_url: /dynamics365/business-central/dev-itpro/developer/methods-auto/library
---

 

# AsText Method

Converts the value in a JsonValue to a Text data type.

```
Text := JsonValue.AsText
```

## Parameters
*JsonValue*  
&emsp;Type: [JsonValue](jsonvalue-class.md)

## Return Value
&emsp;Type: [Text](../datatypes/devenv-text-data-type.md)

## Remarks
The operation will fail with a run-time error if the JsonValue contains NULL or UNDEFINED.

## See Also
[Getting Started with AL](../devenv-get-started.md)  
[Developing Extensions](../devenv-dev-overview.md)
