---
uid: Microsoft.Quantum.Arrays.FlatMapped
title: De functie FlatMapped
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: FlatMapped
qsharp.summary: Given an array and a function that maps an array element to some output array, returns the concatenated output arrays for each array element.
ms.openlocfilehash: 3e75c7703471a2986812df660c2f9328f1536d22
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706029"
---
# <a name="flatmapped-function"></a>De functie FlatMapped

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket [](https://nuget.org/packages/)


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