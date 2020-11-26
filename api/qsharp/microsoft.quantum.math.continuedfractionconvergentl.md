---
uid: Microsoft.Quantum.Math.ContinuedFractionConvergentL
title: De functie ContinuedFractionConvergentL
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ContinuedFractionConvergentL
qsharp.summary: Finds the continued fraction convergent closest to `fraction` with the denominator less or equal to `denominatorBound`
ms.openlocfilehash: c10fcbbe63d3d4c7d6c56196768c1062be1ca350
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210927"
---
# <a name="continuedfractionconvergentl-function"></a>De functie ContinuedFractionConvergentL

Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt gezocht naar de voortgezette fractie convergent die het dichtst bij `fraction` met de noemer kleiner of gelijk is aan `denominatorBound`

```qsharp
function ContinuedFractionConvergentL (fraction : Microsoft.Quantum.Math.BigFraction, denominatorBound : BigInt) : Microsoft.Quantum.Math.BigFraction
```


## <a name="input"></a>Invoer

### <a name="fraction--bigfraction"></a>Fractie: [BigFraction](xref:Microsoft.Quantum.Math.BigFraction)




### <a name="denominatorbound--bigint"></a>denominatorBound: [BigInt](xref:microsoft.quantum.lang-ref.bigint)





## <a name="output--bigfraction"></a>Uitvoer: [BigFraction](xref:Microsoft.Quantum.Math.BigFraction)

Achterliggende fractie die het dichtst bij `fraction` met de noemer kleiner of gelijk aan `denominatorBound`