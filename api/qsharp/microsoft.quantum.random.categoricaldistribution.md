---
uid: Microsoft.Quantum.Random.CategoricalDistribution
title: De functie CategoricalDistribution
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: CategoricalDistribution
qsharp.summary: Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.
ms.openlocfilehash: 754ada71078bd5446f78885ace31d92dce6bf1a4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842352"
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

## <a name="example"></a>Voorbeeld

Met de volgende Q #-code wordt 0 weer gegeven met een kans van 30% en 1 met een waarschijnlijkheids gewicht van 70%:

```qsharp
let dist = CategoricalDistribution([0.3, 0.7]);
Message($"Got sample: {dist::Sample()}");
```