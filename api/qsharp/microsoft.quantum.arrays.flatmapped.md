---
uid: Microsoft.Quantum.Arrays.FlatMapped
title: De functie FlatMapped
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: FlatMapped
qsharp.summary: Given an array and a function that maps an array element to some output array, returns the concatenated output arrays for each array element.
ms.openlocfilehash: e851e8503b3afcb4572f09fe39079247518c22c4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221246"
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