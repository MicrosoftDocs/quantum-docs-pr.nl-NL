---
uid: Microsoft.Quantum.Math.ArgComplex
title: De functie ArgComplex
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ArgComplex
qsharp.summary: Returns the phase of a complex number of type `Complex`.
ms.openlocfilehash: 259296f397207cde4a7d6dfe6cfb1a18e8055216
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211097"
---
# <a name="argcomplex-function"></a>De functie ArgComplex

Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert de fase van een complex type getal `Complex` .

```qsharp
function ArgComplex (input : Microsoft.Quantum.Math.Complex) : Double
```


## <a name="input"></a>Invoer

### <a name="input--complex"></a>invoer: [complex](xref:Microsoft.Quantum.Math.Complex)

Complex getal $c = x + i y $.



## <a name="output--double"></a>Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)

Fase $ \text{Arg} [c] = \text{ArcTan} (y, x) \in (-\pi, \pi] $.