---
uid: Microsoft.Quantum.Random.DrawRandomInt
title: Bewerking DrawRandomInt
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomInt
qsharp.summary: Draws a random integer in a given inclusive range.
ms.openlocfilehash: f7b6cb75f761e4c45295245ed4bd4fb82c592809
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192907"
---
# <a name="drawrandomint-operation"></a>Bewerking DrawRandomInt

Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Hiermee wordt een wille keurig geheel getal in een opgegeven, inclusief bereik getekend.

```qsharp
operation DrawRandomInt (min : Int, max : Int) : Int
```


## <a name="input"></a>Invoer

### <a name="min--int"></a>min: [int](xref:microsoft.quantum.lang-ref.int)

Het kleinste gehele getal dat moet worden getekend.


### <a name="max--int"></a>Max.: [int](xref:microsoft.quantum.lang-ref.int)

Het grootste gehele getal dat moet worden getekend.



## <a name="output--int"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)

Een geheel getal in het inclusieve bereik van `min` tot `max` en met een uniforme kans.

## <a name="remarks"></a>Opmerkingen

Mislukt als `max <= min` .

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. DiscreteUniformDistribution](xref:Microsoft.Quantum.DiscreteUniformDistribution)