---
uid: Microsoft.Quantum.Arrays.SquareArrayFact
title: De functie SquareArrayFact
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SquareArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a square shape
ms.openlocfilehash: 3529718f0c903266d21fd593c11c0149dae0fa2c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220192"
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

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. arrays. RectangularArrayFact](xref:Microsoft.Quantum.Arrays.RectangularArrayFact)