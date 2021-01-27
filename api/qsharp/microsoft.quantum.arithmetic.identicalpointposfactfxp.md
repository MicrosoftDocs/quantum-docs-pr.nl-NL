---
uid: Microsoft.Quantum.Arithmetic.IdenticalPointPosFactFxP
title: De functie IdenticalPointPosFactFxP
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IdenticalPointPosFactFxP
qsharp.summary: Assert that all fixed-point numbers in the provided array have identical point positions when counting from the least- significant bit. I.e., number of bits minus point position must be constant for all fixed-point numbers in the array.
ms.openlocfilehash: 7212f918e1d0ee86b12b85caa6e0c27bc2cebe58
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846622"
---
# <a name="identicalpointposfactfxp-function"></a>De functie IdenticalPointPosFactFxP

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket: [micro soft. Quantum. numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


U moet bevestigen dat alle vaste-komma getallen in de gegeven matrix identieke punt posities hebben wanneer ze van de minst significante bit worden geteld. Dat wil zeggen dat het aantal bits min-punt positie moet constant zijn voor alle vaste-komma getallen in de matrix.

```qsharp
function IdenticalPointPosFactFxP (fixedPoints : Microsoft.Quantum.Arithmetic.FixedPoint[]) : Unit
```


## <a name="input"></a>Invoer

### <a name="fixedpoints--fixedpoint"></a>fixedPoints: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)[]

Matrix van Quantum vaste-komma getallen die worden gecontroleerd op compatibiliteit (met behulp van beweringen).



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

