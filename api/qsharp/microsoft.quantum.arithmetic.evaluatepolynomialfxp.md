---
uid: Microsoft.Quantum.Arithmetic.EvaluatePolynomialFxP
title: Bewerking EvaluatePolynomialFxP
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: EvaluatePolynomialFxP
qsharp.summary: Evaluates a polynomial in a fixed-point representation.
ms.openlocfilehash: d88f9002f4ce39b6a16091837c76168fb3a2f086
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843213"
---
# <a name="evaluatepolynomialfxp-operation"></a>Bewerking EvaluatePolynomialFxP

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket: [micro soft. Quantum. numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Evalueert een polynoom in een vaste-komma weergave.

```qsharp
operation EvaluatePolynomialFxP (coefficients : Double[], fpx : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="coefficients--double"></a>coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]

Coëfficiënten van de polynoom als een dubbele matrix, dat wil zeggen de matrix $ [a_0, a_1,..., a_d] $ voor de polynomiale $P (x) = a_0 + a_1 x + \cdots + a_d x ^ d $.


### <a name="fpx--fixedpoint"></a>FPX: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Invoer nummer van vaste komma waarvoor de polynoom moet worden geëvalueerd.


### <a name="result--fixedpoint"></a>resultaat: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Het vaste-komma nummer van de uitvoer dat $P (x) $ bevat. Moet in eerste instantie de status $ \ket {0} $ hebben.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

