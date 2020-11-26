---
uid: Microsoft.Quantum.Arrays._SwapOrderToPermuteArray
title: Functie _SwapOrderToPermuteArray
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: _SwapOrderToPermuteArray
qsharp.summary: Returns the order elements in an array need to be swapped to produce an ordered array. Assumes swaps occur in place.
ms.openlocfilehash: 9df2ec00d91c1124fae960efd15d576b15b0223c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221705"
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

## <a name="remarks"></a>Opmerkingen

## <a name="psuedocode"></a>Psuedocode

voor (index in 0.. length (Nieuwebestelling)-1) {while Nieuwebestelling [index]! = index {switch Nieuwebestelling [index] met Nieuwebestelling [Nieuwebestelling [index]]}}