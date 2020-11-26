---
uid: Microsoft.Quantum.Random.DrawRandomDouble
title: Bewerking DrawRandomDouble
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomDouble
qsharp.summary: Draws a random real number in a given inclusive interval.
ms.openlocfilehash: d62416f4a222716edb9393fe4f43731d0e8aa9d3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192941"
---
# <a name="drawrandomdouble-operation"></a>Bewerking DrawRandomDouble

Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Hiermee wordt een wille keurig reëel getal in een opgegeven inclusief interval getekend.

```qsharp
operation DrawRandomDouble (min : Double, max : Double) : Double
```


## <a name="input"></a>Invoer

### <a name="min--double"></a>min: [dubbele](xref:microsoft.quantum.lang-ref.double)

Het kleinste reële getal dat moet worden getekend.


### <a name="max--double"></a>maximum: [Double](xref:microsoft.quantum.lang-ref.double)

Het grootste reële getal dat moet worden getekend.



## <a name="output--double"></a>Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)

Een wille keurig reëel getal in het inclusieve interval van `min` tot `max` met een uniforme kans.

## <a name="remarks"></a>Opmerkingen

Mislukt als `max <= min` .

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. ContinuousUniformDistribution](xref:Microsoft.Quantum.ContinuousUniformDistribution)