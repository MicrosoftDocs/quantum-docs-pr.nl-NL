---
uid: Microsoft.Quantum.Arrays.Most
title: De meeste functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Most
qsharp.summary: Creates an array that is equal to an input array except that the last array element is dropped.
ms.openlocfilehash: 81e66e0b64ae8dfc44d163b68370ccadd191c729
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220600"
---
# <a name="most-function"></a>De meeste functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Maakt een matrix die gelijk is aan een invoer matrix, behalve dat het laatste matrix element is verwijderd.

```qsharp
function Most<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a>Invoer

### <a name="array--t"></a>matrix: 'T []

Een matrix waarvan de eerste naar de laatste elementen van de uitvoer matrix moet worden gevormd.



## <a name="output--t"></a>Uitvoer: ' []

Een matrix met de elementen `array[0..Length(array) - 2]` .

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van de matrix elementen.