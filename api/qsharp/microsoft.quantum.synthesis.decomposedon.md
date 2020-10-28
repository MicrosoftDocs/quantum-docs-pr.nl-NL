---
uid: Microsoft.Quantum.Synthesis.DecomposedOn
title: De functie DecomposedOn
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecomposedOn
qsharp.summary: Decomposes a permutation on a variable
ms.openlocfilehash: b033723a50fb85e77c9d4baec1f94231327e9b25
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709174"
---
# <a name="decomposedon-function"></a>De functie DecomposedOn

Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)

Pakket [](https://nuget.org/packages/)


Ontleedt een permutatie op een variabele

```qsharp
function DecomposedOn (perm : Int[], index : Int) : ((Int[], Int[]), Int[])
```


## <a name="description"></a>Beschrijving

Met een permutatie $ \pi $ ( `perm` ) en een index $i $ ( `index` ), deze methode retourneert drie permutaties $ ((\ pi_l, \ pi_r), \pi ') $ zo dat de installatie kopieën van $ \ pi_l $ en $ \ pi_r $ geen bits in hun eigen elementen wijzigen op andere indexen dan $i $ en installatie kopieën van $ \pi $ in hun eigen elementen.

## <a name="input"></a>Invoer

### <a name="perm--int"></a>macht: [int](xref:microsoft.quantum.lang-ref.int)[]




### <a name="index--int"></a>index: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--intintint"></a>Output: (([int](xref:microsoft.quantum.lang-ref.int)[],[int](xref:microsoft.quantum.lang-ref.int)[]),[int](xref:microsoft.quantum.lang-ref.int)[])

