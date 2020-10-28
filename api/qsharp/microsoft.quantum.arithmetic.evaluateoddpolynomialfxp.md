---
uid: Microsoft.Quantum.Arithmetic.EvaluateOddPolynomialFxP
title: Bewerking EvaluateOddPolynomialFxP
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluateOddPolynomialFxP
qsharp.summary: Evaluates an odd polynomial in a fixed-point representation.
ms.openlocfilehash: d52da4092f16d43ab9d08b03f798a4d6789c7348
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707325"
---
# <a name="evaluateoddpolynomialfxp-operation"></a>Bewerking EvaluateOddPolynomialFxP

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket [](https://nuget.org/packages/)


Evalueert een oneven polynoom in een vaste-komma weergave.

```qsharp
operation EvaluateOddPolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit
```


## <a name="input"></a>Invoer

### <a name="coefficients--double"></a>coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]

Coëfficiënten van de oneven polynoom als een dubbele matrix, dat wil zeggen de matrix $ [a_0, a_1,..., a_k] $ voor de oneven polynoom $P (x) = a_0 x + a_1 x ^ 3 + \cdots + a_k x ^ {2.000 + 1} $.


### <a name="fpx--fixedpoint"></a>FPX: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Invoer nummer van vaste komma waarvoor de polynoom moet worden geëvalueerd.


### <a name="result--fixedpoint"></a>resultaat: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Uitvoer met een vast punt dat P (x) zal bevatten. Moet in eerste instantie de status $ \ket {0} $ hebben.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

