---
uid: Microsoft.Quantum.Arrays._SwapOrderToPermuteArray
title: Functie _SwapOrderToPermuteArray
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: _SwapOrderToPermuteArray
qsharp.summary: Returns the order elements in an array need to be swapped to produce an ordered array. Assumes swaps occur in place.
ms.openlocfilehash: ff8e4e23dde7d69f93054a275548ded49d5b0bfb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846296"
---
# <a name="_swapordertopermutearray-function"></a>Functie _SwapOrderToPermuteArray

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert de order elementen in een matrix moeten worden omgewisseld om een geordende matrix te maken.
Er wordt van uitgegaan dat er swaps plaatsvinden.

```qsharp
function _SwapOrderToPermuteArray (newOrder : Int[]) : (Int, Int)[]
```


## <a name="input"></a>Invoer

### <a name="neworder--int"></a>Nieuwebestelling: [int](xref:microsoft.quantum.lang-ref.int)[]

Matrix met de permutatie van de indices van de nieuwe matrix. Er moeten $n $-elementen zijn, die elk een uniek geheel getal zijn van $0 $ tot $n-$1.



## <a name="output--intint"></a>Uitvoer: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []

De tuple vertegenwoordigt de twee indexen die moeten worden omgewisseld. De wissels beginnen bij de laagste index.

## <a name="example"></a>Voorbeeld

```qsharp
// The following returns [(0, 5),(0, 4),(0, 1),(0, 3)];
let swapOrder = _SwapOrderToPermuteArray([5, 3, 2, 0, 1, 4]);
```

## <a name="remarks"></a>Opmerkingen

## <a name="psuedocode"></a>Psuedocode

voor (index in 0.. length (Nieuwebestelling)-1) {while Nieuwebestelling [index]! = index {switch Nieuwebestelling [index] met Nieuwebestelling [Nieuwebestelling [index]]}}