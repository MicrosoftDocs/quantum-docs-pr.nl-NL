---
uid: Microsoft.Quantum.Random.DrawCategorical
title: Bewerking DrawCategorical
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawCategorical
qsharp.summary: Draws a random sample from a categorical distribution specified by a list of probablities.
ms.openlocfilehash: fdc5ae3a9341cb11e8fda129bdd030289b6c99c2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706717"
---
# <a name="drawcategorical-operation"></a>Bewerking DrawCategorical

Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)

Pakket [](https://nuget.org/packages/)


Hiermee wordt een wille keurig voor beeld getekend vanuit een categorische-distributie die is opgegeven door een lijst met probablities.

```qsharp
operation DrawCategorical (probs : Double[]) : Int
```


## <a name="description"></a>Beschrijving

De kans dat een specifieke index wordt geselecteerd, is evenredig met de waarde van het matrix element bij die index.
Matrix elementen die gelijk zijn aan nul, worden genegeerd en hun indices worden nooit geretourneerd. Als een matrix element kleiner dan nul is, of als er geen matrix element groter is dan nul, mislukt de bewerking.

## <a name="input"></a>Invoer

### <a name="probs--double"></a>tests: [dubbele](xref:microsoft.quantum.lang-ref.double)[]

Een matrix met drijvende-komma getallen die in verhouding staan tot de kans dat elke index wordt geselecteerd.



## <a name="output--int"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)

Een geheel getal $i $ met kans $ \Pr (i) = p_i/\ sum_i p_i $, waarbij $p _i $ het $i $ TH-element van is `probs` .

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. wille keurig. CategoricalDistribution](xref:Microsoft.Quantum.Random.CategoricalDistribution)