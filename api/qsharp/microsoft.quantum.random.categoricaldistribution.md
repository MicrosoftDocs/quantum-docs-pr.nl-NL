---
uid: Microsoft.Quantum.Random.CategoricalDistribution
title: De functie CategoricalDistribution
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: CategoricalDistribution
qsharp.summary: Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.
ms.openlocfilehash: 756e9e95cac5554ab8f885dab7c47ac1b174c0f3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708143"
---
# <a name="categoricaldistribution-function"></a>De functie CategoricalDistribution

Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)

Pakket [](https://nuget.org/packages/)


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