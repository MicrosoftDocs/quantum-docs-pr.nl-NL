---
uid: Microsoft.Quantum.Arrays.Rest
title: Rest-functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Rest
qsharp.summary: Creates an array that is equal to an input array except that the first array element is dropped.
ms.openlocfilehash: 4dd10b6e8839fd906ca9c2e36c89c626d5772149
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220385"
---
# <a name="rest-function"></a>Rest-functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Maakt een matrix die gelijk is aan een invoer matrix, behalve dat het eerste matrix element wordt verwijderd.

```qsharp
function Rest<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a>Invoer

### <a name="array--t"></a>matrix: 'T []

Een matrix waarvan de seconde tot laatste elementen de uitvoer matrix vormen.



## <a name="output--t"></a>Uitvoer: ' []

Een matrix met de elementen `array[1..Length(array) - 1]` .

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van de matrix elementen.