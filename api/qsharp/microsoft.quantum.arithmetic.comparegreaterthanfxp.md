---
uid: Microsoft.Quantum.Arithmetic.CompareGreaterThanFxP
title: Bewerking CompareGreaterThanFxP
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGreaterThanFxP
qsharp.summary: Compares two fixed-point numbers stored in quantum registers, and controls a flip on the result.
ms.openlocfilehash: bd3bcedd7a4a81fc600f7f4b6bdf1d2a797abbd4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707396"
---
# <a name="comparegreaterthanfxp-operation"></a>Bewerking CompareGreaterThanFxP

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket [](https://nuget.org/packages/)


Vergelijkt twee vaste-komma nummers die zijn opgeslagen in de Quantum registers en beheert een flip op het resultaat.

```qsharp
operation CompareGreaterThanFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint, result : Qubit) : Unit
```


## <a name="input"></a>Invoer

### <a name="fp1--fixedpoint"></a>FP1: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Eerste getal voor de vaste komma dat moet worden vergeleken.


### <a name="fp2--fixedpoint"></a>FP2: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Tweede getal met vaste komma dat moet worden vergeleken.


### <a name="result--qubit"></a>resultaat: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Resultaat van de vergelijking. Wordt als weer spie gelen `fp1 > fp2` .



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

De huidige implementatie vereist dat de twee vaste-komma nummers dezelfde punt positie en hetzelfde aantal qubits hebben.