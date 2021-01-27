---
uid: Microsoft.Quantum.Random.TransformedContinuousDistribution
title: De functie TransformedContinuousDistribution
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: TransformedContinuousDistribution
qsharp.summary: Given a continuous distribution, returns a new distribution that transforms the original by a given function.
ms.openlocfilehash: 353442a4245a9e20bb1e4c46d2e8a84d4c9534b0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857774"
---
# <a name="transformedcontinuousdistribution-function"></a>De functie TransformedContinuousDistribution

Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Op basis van een continue distributie retourneert een nieuwe distributie waarmee het origineel door een bepaalde functie wordt getransformeerd.

```qsharp
function TransformedContinuousDistribution (transform : (Double -> Double), distribution : Microsoft.Quantum.Random.ContinuousDistribution) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a>Invoer

### <a name="transform--double---double"></a>transformeren: [dubbele](xref:microsoft.quantum.lang-ref.double) -> [dubbele precisie](xref:microsoft.quantum.lang-ref.double)

Een functie waarmee de variates van de oorspronkelijke distributie wordt getransformeerd naar de getransformeerde distributie.


### <a name="distribution--continuousdistribution"></a>distributie: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)

De oorspronkelijke verdeling die moet worden getransformeerd.



## <a name="output--continuousdistribution"></a>Uitvoer: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)

Een nieuwe distributie gerelateerd aan `distribution` de trans formatie die wordt gegeven door `transform` .

## <a name="example"></a>Voorbeeld

De volgende twee distributies zijn identiek:

```qsharp
let dist1 = ContinuousUniformDistribution(1.0, 2.0);
let dist2 = TransformedContinuousDistribution(
    PlusD(1.0, _),
    ContinuousUniformDistribution(0.0, 1.0)
);
```