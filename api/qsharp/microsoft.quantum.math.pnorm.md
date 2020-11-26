---
uid: Microsoft.Quantum.Math.PNorm
title: De functie PNorm
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNorm
qsharp.summary: >-
  Returns the `L(p)` norm of a vector of `Double`s.

  That is, given an array $x$ of type `Double[]`, this returns the $p$-norm $\|x\|\_p= (\sum_{j}|x_j|^{p})^{1/p}$.
ms.openlocfilehash: 3fe029bd893fc4d11aaf351f7ea566256cac5a9e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194726"
---
# <a name="pnorm-function"></a>De functie PNorm

Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert de `L(p)` norm van een vector van `Double` s.

Op basis van een matrix $x $ van het type `Double[]` , retourneert dit de $p $-norm $ \| x \| \_ p = (\ sum_ {j} | x_j | ^ {p}) ^ {1/p} $.

```qsharp
function PNorm (p : Double, array : Double[]) : Double
```


## <a name="input"></a>Invoer

### <a name="p--double"></a>p: [dubbel](xref:microsoft.quantum.lang-ref.double)

De exponent $p $ in de $p $-norm.


### <a name="array--double"></a>matrix: [dubbel](xref:microsoft.quantum.lang-ref.double)[]





## <a name="output--double"></a>Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)

De $p $-norm $ \| x \| _p $.