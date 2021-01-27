---
uid: Microsoft.Quantum.Arrays.SquareArrayFact
title: De functie SquareArrayFact
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SquareArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a square shape
ms.openlocfilehash: a154e5becba4dae762596a3fc1b268855520fa1b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850966"
---
# <a name="squarearrayfact-function"></a>De functie SquareArrayFact

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Vertegenwoordigt een voor waarde dat een tweedimensionale matrix een vier Kante vorm heeft

```qsharp
function SquareArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a>Beschrijving

Deze functie beweringt dat elke rij in een matrix net zoveel elementen bevat als er rijen (elementen) in de matrix zijn.

## <a name="input"></a>Invoer

### <a name="array--t"></a>matrix: ' [] []

Een 2-dimensionale matrix van elementen


### <a name="message--string"></a>bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)

Een bericht dat moet worden afgedrukt als de matrix geen vier Kante matrix is



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van elk element van `array` .

## <a name="example"></a>Voorbeeld

```qsharp
SquareArrayFact([[1, 2], [3, 4]], "Array is not a square");       // okay
SquareArrayFact([[1, 2, 3], [4, 5, 6]], "Array is not a square"); // will fail
SquareArrayFact([[1, 2], [3, 4, 5]], "Array is not a square");    // will fail
```

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. arrays. RectangularArrayFact](xref:Microsoft.Quantum.Arrays.RectangularArrayFact)