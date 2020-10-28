---
uid: Microsoft.Quantum.Arrays.Enumerated
title: Opgesomde functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Enumerated
qsharp.summary: Given an array, returns a new array containing elements of the original array along with the indices of each element.
ms.openlocfilehash: 0a591025a4eef79e08b47527c0bdb556f5645334
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706068"
---
# <a name="enumerated-function"></a>Opgesomde functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket [](https://nuget.org/packages/)


Op basis van een matrix retourneert een nieuwe matrix met elementen van de oorspronkelijke matrix, samen met de indices van elk element.

```qsharp
function Enumerated<'TElement> (array : 'TElement[]) : (Int, 'TElement)[]
```


## <a name="input"></a>Invoer

### <a name="array--telement"></a>matrix: ' TEle []

Een matrix waarvan de elementen moeten worden geïnventariseerd.



## <a name="output--inttelement"></a>Uitvoer: ([int](xref:microsoft.quantum.lang-ref.int), ' tele) []

Een nieuwe matrix met elementen van de oorspronkelijke matrix samen met de indices.

## <a name="type-parameters"></a>Type parameters

### <a name="telement"></a>-TEle

Het type elementen van de matrix.