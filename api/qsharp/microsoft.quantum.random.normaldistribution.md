---
uid: Microsoft.Quantum.Random.NormalDistribution
title: De functie NormalDistribution
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: NormalDistribution
qsharp.summary: Returns a normal distribution with a given mean and variance.
ms.openlocfilehash: 733a2763dca6d75f81d538f63c3084331a8e1d51
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98814186"
---
# <a name="normaldistribution-function"></a>De functie NormalDistribution

Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Retourneert een normale verdeling met een gegeven gemiddelde en variantie.

```qsharp
function NormalDistribution (mean : Double, variance : Double) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a>Invoer

### <a name="mean--double"></a>gemiddelde: [dubbele](xref:microsoft.quantum.lang-ref.double)




### <a name="variance--double"></a>afwijking: [dubbel](xref:microsoft.quantum.lang-ref.double)





## <a name="output--continuousdistribution"></a>Uitvoer: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)



## <a name="example"></a>Voorbeeld

In het volgende voor beeld worden tien voor beelden van de normale distributie getekend met gemiddelde 2 en de standaard afwijking 0,1:

```qsharp
let samples = DrawMany(
    (NormalDistribution(2.0, PowD(0.1, 2.0)))::Sample,
    10, ()
);
```

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. wille keurig. StandardNormalDistribution](xref:Microsoft.Quantum.Random.StandardNormalDistribution)