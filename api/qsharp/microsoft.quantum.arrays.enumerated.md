---
uid: Microsoft.Quantum.Arrays.Enumerated
title: Opgesomde functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Enumerated
qsharp.summary: Given an array, returns a new array containing elements of the original array along with the indices of each element.
ms.openlocfilehash: 94e8fdb7288bc43ed84d10a3292819b455a2be31
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221416"
---
# <a name="enumerated-function"></a>Opgesomde functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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