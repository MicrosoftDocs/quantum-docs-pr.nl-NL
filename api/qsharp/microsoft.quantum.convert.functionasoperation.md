---
uid: Microsoft.Quantum.Convert.FunctionAsOperation
title: De functie FunctionAsOperation
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: FunctionAsOperation
qsharp.summary: Converts functions to operations.
ms.openlocfilehash: 90e9f0c922a77fbb6d6faf8945d4f5d1c8ff33b7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702986"
---
# <a name="functionasoperation-function"></a>De functie FunctionAsOperation

Naam ruimte: [micro soft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Pakket [](https://nuget.org/packages/)


Hiermee worden functies geconverteerd naar bewerkingen.

```qsharp
function FunctionAsOperation<'Input, 'Output> (fn : ('Input -> 'Output)) : ('Input => 'Output)
```


## <a name="description"></a>Beschrijving

Een bewerking die de functie aanroept, wordt door gegeven aan een functie.

## <a name="input"></a>Invoer

### <a name="fn--input---output"></a>FN: de uitvoer van invoer >

Een functie die moet worden geconverteerd naar een bewerking.



## <a name="output--input--output"></a>Output: ' input => ' uitvoer 

Een bewerking `op` die `op(input)` identiek is aan `fn(input)` voor alle `input` .

## <a name="type-parameters"></a>Type parameters

### <a name="input"></a>' Invoer

Invoer type van de functie die moet worden geconverteerd.
### <a name="output"></a>' Uitvoer

Het uitvoer type van de functie die moet worden geconverteerd.

## <a name="remarks"></a>Opmerkingen

Dit is vooral nuttig voor het door geven van functies aan functies of bewerkingen waarbij een bewerking als invoer wordt verwacht.