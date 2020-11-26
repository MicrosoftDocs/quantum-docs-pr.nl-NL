---
uid: Microsoft.Quantum.Arrays.Unzipped
title: Uitgepakte functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unzipped
qsharp.summary: Given an array of 2-tuples, returns a tuple of two arrays, each containing the elements of the tuples of the input array.
ms.openlocfilehash: aee1d48c9e0a1f104040bc56c78fdbb8bc4d34ba
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219954"
---
# <a name="unzipped-function"></a>Uitgepakte functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Op basis van een matrix van 2-Tuples retourneert een tuple van twee matrices, elk met de elementen van de Tuples van de invoer matrix.

```qsharp
function Unzipped<'T, 'U> (arr : ('T, 'U)[]) : ('T[], 'U[])
```


## <a name="input"></a>Invoer

### <a name="arr--tu"></a>ARR: ('T, ' U) []

Een matrix met 2-Tuples



## <a name="output--tu"></a>Uitvoer: ('T [], ' U [])

Twee matrices, de eerste die alle eerste elementen van de ingevoerde Tuples bevat, de tweede matrix met alle tweede elementen van de ingevoerde Tuples.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van het eerste element in elke tupel
### <a name="u"></a>' U

Het type van het tweede element in elke tupel

## <a name="see-also"></a>Zie ook

- [Microsoft.Quantum.Arrays.ZipPED](xref:Microsoft.Quantum.Arrays.Zipped)