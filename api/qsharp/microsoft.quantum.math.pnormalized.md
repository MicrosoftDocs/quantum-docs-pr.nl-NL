---
uid: Microsoft.Quantum.Math.PNormalized
title: De functie PNormalized
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNormalized
qsharp.summary: >-
  Normalizes a vector of `Double`s in the `L(p)` norm.

  That is, given an array $x$ of type `Double[]`, this returns an array where all elements are divided by the $p$-norm $\|x\|_p$.
ms.openlocfilehash: 196bdab67528aa8672a010ac3830459e27276ce9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227519"
---
# <a name="pnormalized-function"></a>De functie PNormalized

Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Normaliseert een vector van `Double` s in de `L(p)` norm.

Op basis van een matrix $x $ van type, wordt hiermee `Double[]` een matrix geretourneerd waarin alle elementen worden gedeeld door de $p $-norm $ \| x \| _p $.

```qsharp
function PNormalized (p : Double, array : Double[]) : Double[]
```


## <a name="input"></a>Invoer

### <a name="p--double"></a>p: [dubbel](xref:microsoft.quantum.lang-ref.double)

De exponent $p $ in de $p $-norm.


### <a name="array--double"></a>matrix: [dubbel](xref:microsoft.quantum.lang-ref.double)[]





## <a name="output--double"></a>Uitvoer: [dubbele](xref:microsoft.quantum.lang-ref.double)[]

De matrix $x $ genormaliseerd door de $p $-norm $ \| x \| _p $.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. math. PNorm](xref:Microsoft.Quantum.Math.PNorm)