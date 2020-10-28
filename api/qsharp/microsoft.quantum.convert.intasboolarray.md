---
uid: Microsoft.Quantum.Convert.IntAsBoolArray
title: De functie IntAsBoolArray
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: IntAsBoolArray
qsharp.summary: Produces a binary representation of a positive integer, using the little-endian representation for the returned array.
ms.openlocfilehash: 9783a49a77bdc39ffe8c7725196eb620f4cd0100
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702962"
---
# <a name="intasboolarray-function"></a>De functie IntAsBoolArray

Naam ruimte: [micro soft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Pakket [](https://nuget.org/packages/)


Produceert een binaire weer gave van een positief geheel getal, met behulp van de weer gave van de little-endian voor de geretourneerde matrix.

```qsharp
function IntAsBoolArray (number : Int, bits : Int) : Bool[]
```


## <a name="input"></a>Invoer

### <a name="number--int"></a>getal: [int](xref:microsoft.quantum.lang-ref.int)

Een positief geheel getal dat moet worden geconverteerd naar een matrix met Boole-waarden.


### <a name="bits--int"></a>bits: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal bits in de binaire weer gave van `number` .



## <a name="output--bool"></a>Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]

Een matrix met Boole-waarden die aangeeft `number` .

## <a name="remarks"></a>Opmerkingen

De invoer `bits` moet tussen 0 en 63.
De invoer `number` moet liggen tussen 0 en $2 ^ {\texttt{bits}}-$1.