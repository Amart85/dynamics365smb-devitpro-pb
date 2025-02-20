---
title: "RecordRef.KeyCount() Method"
description: "Gets the number of keys that exist in the table that is referred to by the RecordRef."
ms.author: solsen
ms.custom: na
ms.date: 07/07/2021
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: reference
author: SusanneWindfeldPedersen
---
[//]: # (START>DO_NOT_EDIT)
[//]: # (IMPORTANT:Do not edit any of the content between here and the END>DO_NOT_EDIT.)
[//]: # (Any modifications should be made in the .xml files in the ModernDev repo.)
# RecordRef.KeyCount() Method
> **Version**: _Available or changed with runtime version 1.0._

Gets the number of keys that exist in the table that is referred to by the RecordRef. Returns an error if no table is selected.


## Syntax
```AL
Count :=   RecordRef.KeyCount()
```
> [!NOTE]
> This method can be invoked using property access syntax.

## Parameters
*RecordRef*  
&emsp;Type: [RecordRef](recordref-data-type.md)  
An instance of the [RecordRef](recordref-data-type.md) data type.  

## Return Value
*Count*  
&emsp;Type: [Integer](../integer/integer-data-type.md)  
The number of keys that have been identified in the table.


[//]: # (IMPORTANT: END>DO_NOT_EDIT)

## Example  
 The following example opens the Customer table \(18\) as a RecordRef variable that is named CustomerRecref. The KeyCount method retrieves the number of keys that are defined in the Customer table. The return value of the method is stored in the KeyCount variable and displayed in a message box. The KeyCount variable contains the number 13 because 13 keys are defined in the Customer table. 
  
```al
var
    CustomerRecref: RecordRef;
    KeyCount: Integer;
    Text000: Label 'The table has %1 keys.';
begin     
    CustomerRecref.Open(18);  
    KeyCount := CustomerRecref.KeyCount;  
    Message(Text000, KeyCount);  
end;
  
```  

## See Also
[RecordRef Data Type](recordref-data-type.md)  
[Get Started with AL](../../devenv-get-started.md)  
[Developing Extensions](../../devenv-dev-overview.md)