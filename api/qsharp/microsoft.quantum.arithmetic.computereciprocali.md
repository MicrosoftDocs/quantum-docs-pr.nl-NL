---
uid: Microsoft.Quantum.Arithmetic.ComputeReciprocalI
title: Bewerking ComputeReciprocalI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ComputeReciprocalI
qsharp.summary: Computes the reciprocal 1/x for an unsigned integer x using integer division. The result, interpreted as an integer, will be `floor(2^(2*n-1) / x)`.
ms.openlocfilehash: c28027f7a2533885102a54a028bec37eb608f2b4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846723"
---
# <a name="computereciprocali-operation"></a>Bewerking ComputeReciprocalI

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket: [micro soft. Quantum. numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Hiermee wordt de reciproque waarde van 1/x voor een niet-ondertekende integer x berekend op basis van de deling van een geheel getal. Het resultaat, geïnterpreteerd als een geheel getal, is `floor(2^(2*n-1) / x)` .

```qsharp
operation ComputeReciprocalI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="xs--littleendian"></a>XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

n-bits geheel getal zonder teken


### <a name="result--littleendian"></a>resultaat: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

2n-bits uitvoer moet in $ \ket $ in {0} eerste instantie zijn.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

Voor de invoer x = 0 is de uitvoer allemaal.