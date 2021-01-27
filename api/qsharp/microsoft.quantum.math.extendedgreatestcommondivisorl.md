---
uid: Microsoft.Quantum.Math.ExtendedGreatestCommonDivisorL
title: De functie ExtendedGreatestCommonDivisorL
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExtendedGreatestCommonDivisorL
qsharp.summary: Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: 1445f1c3d2a5852459a492fa5e6bfd2a685786d9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857535"
---
# <a name="extendedgreatestcommondivisorl-function"></a>De functie ExtendedGreatestCommonDivisorL

Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een tuple $ (u, v) $ zodanig berekend dat $u \cdot a + v \cdot b = \operatorname{GCD} (a, b) $, waarbij $ \operatorname{GCD} $ $a $ grootste gemene deler van $a $ en $b $ is. De GCD is altijd positief.

```qsharp
function ExtendedGreatestCommonDivisorL (a : BigInt, b : BigInt) : (BigInt, BigInt)
```


## <a name="input"></a>Invoer

### <a name="a--bigint"></a>a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

het eerste getal waarvan de uitgebreide grootste algemene deler wordt berekend


### <a name="b--bigint"></a>b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

het tweede getal waarvan de uitgebreide grootste algemene deler wordt berekend



## <a name="output--bigintbigint"></a>Uitvoer: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[bigint](xref:microsoft.quantum.lang-ref.bigint))

Tuple $ (u, v) $ met de eigenschap $u \cdot a + v \cdot b = \operatorname{GCD} (a, b) $.

## <a name="references"></a>Verwijzingen

- Deze implementatie is gebaseerd op https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm