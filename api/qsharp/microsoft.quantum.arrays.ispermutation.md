---
uid: Microsoft.Quantum.Arrays.IsPermutation
title: De functie IsPermutation
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsPermutation
qsharp.summary: Outputs true if and only if a given array represents a permutation.
ms.openlocfilehash: 7e563650f33b0292e1e41f629829a2d3b9e5fd28
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848099"
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



## <a name="example"></a>Voorbeeld

Met de volgende Q #-code wordt het bericht ' alle diagnostische gegevens zijn voltooid ' afgedrukt:

```qsharp
Fact(IsPermutation([2, 0, 1], "");
Contradiction(IsPermutation([5, 0, 1], "[5, 0, 1] isn't a permutation");
Message("All diagnostics completed successfully.");
```

## <a name="remarks"></a>Opmerkingen

Een matrix met een lengte van nul is een permutatie.