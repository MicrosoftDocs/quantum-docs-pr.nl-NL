---
uid: Microsoft.Quantum.Math.ContinuedFractionConvergentL
title: De functie ContinuedFractionConvergentL
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ContinuedFractionConvergentL
qsharp.summary: Finds the continued fraction convergent closest to `fraction` with the denominator less or equal to `denominatorBound`
ms.openlocfilehash: a02b38fedb5b0025f04e7bba86f2f998493206b3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708575"
---
# <a name="continuedfractionconvergentl-function"></a>De functie ContinuedFractionConvergentL

Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)

Pakket [](https://nuget.org/packages/)


Hiermee wordt gezocht naar de voortgezette fractie convergent die het dichtst bij `fraction` met de noemer kleiner of gelijk is aan `denominatorBound`

```qsharp
function ContinuedFractionConvergentL (fraction : Microsoft.Quantum.Math.BigFraction, denominatorBound : BigInt) : Microsoft.Quantum.Math.BigFraction
```


## <a name="input"></a>Invoer

### <a name="fraction--bigfraction"></a>Fractie: [BigFraction](xref:Microsoft.Quantum.Math.BigFraction)




### <a name="denominatorbound--bigint"></a>denominatorBound: [BigInt](xref:microsoft.quantum.lang-ref.bigint)





## <a name="output--bigfraction"></a>Uitvoer: [BigFraction](xref:Microsoft.Quantum.Math.BigFraction)

Achterliggende fractie die het dichtst bij `fraction` met de noemer kleiner of gelijk aan `denominatorBound`