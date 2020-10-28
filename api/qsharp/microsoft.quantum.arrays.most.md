---
uid: Microsoft.Quantum.Arrays.Most
title: De meeste functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Most
qsharp.summary: Creates an array that is equal to an input array except that the last array element is dropped.
ms.openlocfilehash: ca89041a4e70472e9bf7a63ffcacccb35aad527c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705861"
---
# <a name="most-function"></a>De meeste functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket [](https://nuget.org/packages/)


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