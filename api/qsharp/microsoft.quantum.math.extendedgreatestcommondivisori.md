---
uid: Microsoft.Quantum.Math.ExtendedGreatestCommonDivisorI
title: De functie ExtendedGreatestCommonDivisorI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExtendedGreatestCommonDivisorI
qsharp.summary: Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: 8cb21ae5052ae6c5a8aed8be71d6bd3d32034272
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708532"
---
# <a name="extendedgreatestcommondivisori-function"></a>De functie ExtendedGreatestCommonDivisorI

Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)

Pakket [](https://nuget.org/packages/)


Hiermee wordt een tuple $ (u, v) $ zodanig berekend dat $u \cdot a + v \cdot b = \operatorname{GCD} (a, b) $, waarbij $ \operatorname{GCD} $ $a $ grootste gemene deler van $a $ en $b $ is. De GCD is altijd positief.

```qsharp
function ExtendedGreatestCommonDivisorI (a : Int, b : Int) : (Int, Int)
```


## <a name="input"></a>Invoer

### <a name="a--int"></a>a: [int](xref:microsoft.quantum.lang-ref.int)

het eerste getal waarvan de uitgebreide grootste algemene deler wordt berekend


### <a name="b--int"></a>b: [int](xref:microsoft.quantum.lang-ref.int)

het tweede getal waarvan de uitgebreide grootste algemene deler wordt berekend



## <a name="output--intint"></a>Uitvoer: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))

Tuple $ (u, v) $ met de eigenschap $u \cdot a + v \cdot b = \operatorname{GCD} (a, b) $.

## <a name="references"></a>Naslaginformatie

- Deze implementatie is gebaseerd op https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm