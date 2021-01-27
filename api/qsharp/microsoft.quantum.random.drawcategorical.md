---
uid: Microsoft.Quantum.Random.DrawCategorical
title: Bewerking DrawCategorical
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawCategorical
qsharp.summary: Draws a random sample from a categorical distribution specified by a list of probablities.
ms.openlocfilehash: a9fe1b08e80abc65a5c4b803f0cb8a5e7a62759c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851154"
---
# <a name="drawcategorical-operation"></a>Bewerking DrawCategorical

Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


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