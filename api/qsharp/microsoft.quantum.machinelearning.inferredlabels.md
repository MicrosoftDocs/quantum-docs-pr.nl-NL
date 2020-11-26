---
uid: Microsoft.Quantum.MachineLearning.InferredLabels
title: De functie InferredLabels
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabels
qsharp.summary: Given an array of classification probabilities and a bias, returns the label inferred from each probability.
ms.openlocfilehash: 668ab89ed45c49d33ce50ff5d892f4d57246c12a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196358"
---
# <a name="inferredlabels-function"></a>De functie InferredLabels

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Op basis van een matrix met classificatie kansen en een bias, retourneert het label dat wordt afgeleid van elke waarschijnlijkheid.

```qsharp
function InferredLabels (bias : Double, probabilities : Double[]) : Int[]
```


## <a name="input"></a>Invoer

### <a name="bias--double"></a>afwijking: [dubbel](xref:microsoft.quantum.lang-ref.double)

De afwijking tussen twee klassen, meestal het resultaat van het trainen van een classificatie.


### <a name="probabilities--double"></a>kansen: [dubbel](xref:microsoft.quantum.lang-ref.double)[]

Een matrix met classificatie kansen voor een aantal steek proeven, meestal het resultaat van het schatten van classificatie frequenties.



## <a name="output--int"></a>Output: [int](xref:microsoft.quantum.lang-ref.int)[]

Het label is afgeleid van elke classificatie waarschijnlijkheid.