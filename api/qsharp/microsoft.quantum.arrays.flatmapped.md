---
uid: Microsoft.Quantum.Arrays.FlatMapped
title: De functie FlatMapped
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: FlatMapped
qsharp.summary: Given an array and a function that maps an array element to some output array, returns the concatenated output arrays for each array element.
ms.openlocfilehash: bee7002c5a1e80cee7907ff9cb4ebaaedf8e9923
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848644"
---
# <a name="flatmapped-function"></a>De functie FlatMapped

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Op basis van een matrix en een functie waarmee een matrix element wordt toegewezen aan een bepaalde uitvoer matrix, worden de samengevoegde uitvoer matrices voor elk matrix element geretourneerd.

```qsharp
function FlatMapped<'TInput, 'TOutput> (mapper : ('TInput -> 'TOutput[]), array : 'TInput[]) : 'TOutput[]
```


## <a name="input"></a>Invoer

### <a name="mapper--tinput---toutput"></a>Mapper: ' TInput-> ' TOutput []

Een functie van `'TInput` naar `'TOutput[]` die wordt gebruikt voor het toewijzen van matrix elementen.


### <a name="array--tinput"></a>matrix: ' TInput []

Een matrix met elementen.



## <a name="output--toutput"></a>Uitvoer: ' TOutput []

Een matrix van `'TOutput[]` Dit is de samen voeging van alle matrices die worden gegenereerd door de toewijzings functie.

## <a name="type-parameters"></a>Type parameters

### <a name="tinput"></a>'TInput

Het type `array` elementen.
### <a name="toutput"></a>'TOutput

De `mapper` functie retourneert matrices van dit type.

## <a name="example"></a>Voorbeeld

```qsharp
let Numbers = SequenceI(1, _); // generates numbers starting from 1
let values = FlatMapped(Numbers, [1, 2, 3]);
// values = [1, 1, 2, 1, 2, 3]
```