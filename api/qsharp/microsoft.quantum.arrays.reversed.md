---
uid: Microsoft.Quantum.Arrays.Reversed
title: Omgekeerde functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Reversed
qsharp.summary: Create an array that contains the same elements as an input array but in Reversed order.
ms.openlocfilehash: 270f15c1d10b4397e258c750876095efc2b8e951
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220430"
---
# <a name="reversed-function"></a>Omgekeerde functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Maak een matrix die dezelfde elementen bevat als een invoer matrix, maar in omgekeerde volg orde.

```qsharp
function Reversed<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a>Invoer

### <a name="array--t"></a>matrix: 'T []

Een matrix waarvan de elementen in omgekeerde volg orde moeten worden gekopieerd.



## <a name="output--t"></a>Uitvoer: ' []

Een matrix met de elementen `array[Length(array) - 1]` .. `array[0]`.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van de matrix elementen.