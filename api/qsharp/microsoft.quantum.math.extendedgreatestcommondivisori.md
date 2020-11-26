---
uid: Microsoft.Quantum.Math.ExtendedGreatestCommonDivisorI
title: De functie ExtendedGreatestCommonDivisorI
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExtendedGreatestCommonDivisorI
qsharp.summary: Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: 365e91e84add0d57d5a3cf203bbf23d96979b251
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96195523"
---
# <a name="extendedgreatestcommondivisori-function"></a>De functie ExtendedGreatestCommonDivisorI

Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

## <a name="references"></a>Referenties

- Deze implementatie is gebaseerd op https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm