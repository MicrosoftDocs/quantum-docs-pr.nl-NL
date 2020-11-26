---
uid: Microsoft.Quantum.Random.CategoricalDistribution
title: De functie CategoricalDistribution
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: CategoricalDistribution
qsharp.summary: Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.
ms.openlocfilehash: 2e3d9b17939d5a9a5bc5e7d89a843e0ff5a848ba
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210247"
---
# <a name="categoricaldistribution-function"></a>De functie CategoricalDistribution

Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Retourneert een discrete categorische-distributie, waarbij de kans voor elk van een eindige lijst met gegeven uitkomsten expliciet is opgegeven.

```qsharp
function CategoricalDistribution (probs : Double[]) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a>Invoer

### <a name="probs--double"></a>tests: [dubbele](xref:microsoft.quantum.lang-ref.double)[]

De kansen voor elk resultaat van de categorische-distributie.
Deze waarschijnlijkheden mogen niet worden genormaliseerd, maar moeten allemaal niet-negatief zijn.



## <a name="output--discretedistribution"></a>Uitvoer: [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)

De index `i` met de waarschijnlijkheid `probs[i] / sum` , waarbij `sum` de som van de `probs` gegeven door is `Fold(PlusD, 0.0, probs)` .