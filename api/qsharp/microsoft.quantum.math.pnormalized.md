---
uid: Microsoft.Quantum.Math.PNormalized
title: De functie PNormalized
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNormalized
qsharp.summary: >-
  Normalizes a vector of `Double`s in the `L(p)` norm.

  That is, given an array $x$ of type `Double[]`, this returns an array where all elements are divided by the $p$-norm $\|x\|_p$.
ms.openlocfilehash: ea6a88d07d3b246f666b793f0b10ab6598ea4ff6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854837"
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