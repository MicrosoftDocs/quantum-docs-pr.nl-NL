---
uid: Microsoft.Quantum.Arrays.RectangularArrayFact
title: De functie RectangularArrayFact
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: RectangularArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a rectangular shape
ms.openlocfilehash: b8ef7d52f7f815ca3e21ded1236e775a381646cb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220413"
---
# <a name="rectangulararrayfact-function"></a>De functie RectangularArrayFact

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Vertegenwoordigt een voor waarde die een 2-dimensionale matrix heeft met een rechthoekige vorm

```qsharp
function RectangularArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a>Beschrijving

Deze functie beweringt dat elke rij in een matrix dezelfde lengte heeft.

## <a name="input"></a>Invoer

### <a name="array--t"></a>matrix: ' [] []

Een 2-dimensionale matrix van elementen


### <a name="message--string"></a>bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)

Een bericht dat moet worden afgedrukt als de matrix geen rechthoekige matrix is



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van elk element van `array` .

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. arrays. SquareArrayFact](xref:Microsoft.Quantum.Arrays.SquareArrayFact)