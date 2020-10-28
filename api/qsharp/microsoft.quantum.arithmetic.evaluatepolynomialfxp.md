---
uid: Microsoft.Quantum.Arithmetic.EvaluatePolynomialFxP
title: Bewerking EvaluatePolynomialFxP
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluatePolynomialFxP
qsharp.summary: Evaluates a polynomial in a fixed-point representation.
ms.openlocfilehash: 3903bf69d5b0a6e57530f2c6a44e1d351c8a605f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707317"
---
# <a name="evaluatepolynomialfxp-operation"></a>Bewerking EvaluatePolynomialFxP

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket [](https://nuget.org/packages/)


Evalueert een polynoom in een vaste-komma weergave.

```qsharp
operation EvaluatePolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit
```


## <a name="input"></a>Invoer

### <a name="coefficients--double"></a>coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]

Coëfficiënten van de polynoom als een dubbele matrix, dat wil zeggen de matrix $ [a_0, a_1,..., a_d] $ voor de polynomiale $P (x) = a_0 + a_1 x + \cdots + a_d x ^ d $.


### <a name="fpx--fixedpoint"></a>FPX: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Invoer nummer van vaste komma waarvoor de polynoom moet worden geëvalueerd.


### <a name="result--fixedpoint"></a>resultaat: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Het vaste-komma nummer van de uitvoer dat $P (x) $ bevat. Moet in eerste instantie de status $ \ket {0} $ hebben.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

