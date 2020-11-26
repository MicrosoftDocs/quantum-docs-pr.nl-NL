---
uid: Microsoft.Quantum.Arrays.IsPermutation
title: De functie IsPermutation
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsPermutation
qsharp.summary: Outputs true if and only if a given array represents a permutation.
ms.openlocfilehash: 144f683818b5d75de5b075328365d3e994de29d1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220923"
---
# <a name="ispermutation-function"></a>De functie IsPermutation

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Uitvoer waar als en alleen als een bepaalde matrix een permutatie vertegenwoordigt.

```qsharp
function IsPermutation (permuation : Int[]) : Bool
```


## <a name="description"></a>Beschrijving

Met een matrix `array` van lengte `n` retourneert waar als en alleen als elke integer `0` `n - 1` precies één keer in wordt weer gegeven `array` , zodat deze `array` kan worden geïnterpreteerd als een permutatie van `n` elementen.

## <a name="input"></a>Invoer

### <a name="permuation--int"></a>permuation: [int](xref:microsoft.quantum.lang-ref.int)[]

Een matrix die een permutatie kan of mag bevatten.



## <a name="output--bool"></a>Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)



## <a name="remarks"></a>Opmerkingen

Een matrix met een lengte van nul is een permutatie.