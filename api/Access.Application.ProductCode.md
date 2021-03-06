---
title: Application.ProductCode property (Access)
keywords: vbaac10.chm12584
f1_keywords:
- vbaac10.chm12584
ms.prod: access
api_name:
- Access.Application.ProductCode
ms.assetid: b4e374ec-b52f-e73d-174e-bb07f40ab029
ms.date: 06/08/2017
localization_priority: Normal
---


# Application.ProductCode property (Access)

You can use the  **ProductCode** property to determine the Access globally unique identifier (GUID). Read-only **String**.


## Syntax

_expression_. `ProductCode`

_expression_ A variable that represents an [Application](Access.Application.md) object.


## Example

The following example displays a message indicating the GUID for Microsoft Access for the user's computer.


```vb
MsgBox "The GUID for Microsoft Access on this computer is " & Application.ProductCode & "."
```


## See also


[Application Object](Access.Application.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]