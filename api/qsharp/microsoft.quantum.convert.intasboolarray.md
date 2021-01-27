---
uid: Microsoft.Quantum.Convert.IntAsBoolArray
title: De functie IntAsBoolArray
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: IntAsBoolArray
qsharp.summary: Produces a binary representation of a non-negative integer, using the little-endian representation for the returned array.
ms.openlocfilehash: 8b3d230605cc756a5da01e45e47f91c5b8e9f541
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98833307"
---
# <a name="intasboolarray-function"></a>De functie IntAsBoolArray

Naam ruimte: [micro soft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Produceert een binaire weer gave van een niet-negatief geheel getal, met behulp van de weer gave van de little-endian voor de geretourneerde matrix.

```qsharp
function IntAsBoolArray (number : Int, bits : Int) : Bool[]
```


## <a name="input"></a>Invoer

### <a name="number--int"></a>getal: [int](xref:microsoft.quantum.lang-ref.int)

Een niet-negatief geheel getal dat moet worden geconverteerd naar een matrix met Boole-waarden.


### <a name="bits--int"></a>bits: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal bits in de binaire weer gave van `number` .



## <a name="output--bool"></a>Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]

Een matrix met Boole-waarden die aangeeft `number` .

## <a name="remarks"></a>Opmerkingen

De invoer `bits` moet tussen 0 en 63.
De invoer `number` moet liggen tussen 0 en $2 ^ {\texttt{bits}}-$1.