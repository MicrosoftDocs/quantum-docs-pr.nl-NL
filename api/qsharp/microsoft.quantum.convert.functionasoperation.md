---
uid: Microsoft.Quantum.Convert.FunctionAsOperation
title: De functie FunctionAsOperation
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: FunctionAsOperation
qsharp.summary: Converts functions to operations.
ms.openlocfilehash: cf4f8c97bf38b3a64eb952d0a502bc21c29c579c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98833828"
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