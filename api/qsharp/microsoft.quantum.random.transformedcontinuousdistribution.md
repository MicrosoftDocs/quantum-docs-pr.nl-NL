---
uid: Microsoft.Quantum.Random.TransformedContinuousDistribution
title: De functie TransformedContinuousDistribution
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: TransformedContinuousDistribution
qsharp.summary: Given a continuous distribution, returns a new distribution that transforms the original by a given function.
ms.openlocfilehash: b317eaaa0ff0180ea5d240464c96d1c6b59c9c70
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226261"
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