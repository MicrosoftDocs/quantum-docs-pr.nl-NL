---
uid: Microsoft.Quantum.Arrays.Swapped
title: Verwissel bare functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Swapped
qsharp.summary: Applies a swap of two elements in an array.
ms.openlocfilehash: fa5b37b4caf5d8f19ed05075ddd7bc4217036bfb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705748"
---
# <a name="swapped-function"></a>Verwissel bare functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket [](https://nuget.org/packages/)


Past een swap van twee elementen in een matrix toe.

```qsharp
function Swapped<'T> (firstIndex : Int, secondIndex : Int, arr : 'T[]) : 'T[]
```


## <a name="input"></a>Invoer

### <a name="firstindex--int"></a>firstIndex: [int](xref:microsoft.quantum.lang-ref.int)

Index van het eerste element dat moet worden omgewisseld.


### <a name="secondindex--int"></a>secondIndex: [int](xref:microsoft.quantum.lang-ref.int)

Index van het tweede element dat moet worden omgewisseld.


### <a name="arr--t"></a>ARR: 'T []

Matrix met elementen die moeten worden omgewisseld.



## <a name="output--t"></a>Uitvoer: ' []

De matrix met de in-place wisseling toegepast.

## <a name="example"></a>Voorbeeld

```qsharp
// The following returns [0, 3, 2, 1, 4]
Swapped(1, 3, [0, 1, 2, 3, 4]);
```

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

