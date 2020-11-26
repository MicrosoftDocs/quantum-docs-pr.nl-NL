---
uid: Microsoft.Quantum.Convert.FunctionAsOperation
title: De functie FunctionAsOperation
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: FunctionAsOperation
qsharp.summary: Converts functions to operations.
ms.openlocfilehash: 10703818242cf6b3853f08a45bfb9094f397f6c2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224374"
---
# <a name="functionasoperation-function"></a>De functie FunctionAsOperation

Naam ruimte: [micro soft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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