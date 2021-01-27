---
uid: Microsoft.Quantum.Random.DrawRandomDouble
title: Bewerking DrawRandomDouble
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomDouble
qsharp.summary: Draws a random real number in a given inclusive interval.
ms.openlocfilehash: 792e9c714b761b48618aec2091e167a359c2b522
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847614"
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

## <a name="example"></a>Voorbeeld

Met de volgende Q # fragment wordt wille keurig een hoek getekend tussen $0 $ en $2 \pi $:

```qsharp
let angle = DrawRandomDouble(0.0, 2.0 * PI());
```

## <a name="remarks"></a>Opmerkingen

Mislukt als `max <= min` .

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. ContinuousUniformDistribution](xref:Microsoft.Quantum.ContinuousUniformDistribution)