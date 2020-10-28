---
uid: Microsoft.Quantum.Arithmetic.IdenticalPointPosFactFxP
title: De functie IdenticalPointPosFactFxP
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IdenticalPointPosFactFxP
qsharp.summary: Assert that all fixed-point numbers in the provided array have identical point positions when counting from the least- significant bit. I.e., number of bits minus point position must be constant for all fixed-point numbers in the array.
ms.openlocfilehash: 0b285ce980ca1abbc3eb20838389a6f49835e742
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707276"
---
# <a name="identicalpointposfactfxp-function"></a>De functie IdenticalPointPosFactFxP

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket [](https://nuget.org/packages/)


U moet bevestigen dat alle vaste-komma getallen in de gegeven matrix identieke punt posities hebben wanneer ze van de minst significante bit worden geteld. Dat wil zeggen dat het aantal bits min-punt positie moet constant zijn voor alle vaste-komma getallen in de matrix.

```qsharp
function IdenticalPointPosFactFxP (fixedPoints : Microsoft.Quantum.Arithmetic.FixedPoint[]) : Unit
```


## <a name="input"></a>Invoer

### <a name="fixedpoints--fixedpoint"></a>fixedPoints: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)[]

Matrix van Quantum vaste-komma getallen die worden gecontroleerd op compatibiliteit (met behulp van beweringen).



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

