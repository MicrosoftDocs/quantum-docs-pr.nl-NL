---
uid: Microsoft.Quantum.MachineLearning.InferredLabels
title: De functie InferredLabels
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabels
qsharp.summary: Given an array of classification probabilities and a bias, returns the label inferred from each probability.
ms.openlocfilehash: 874d1a2f7cc6d67567e0d2baa70b0d26b639a029
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707999"
---
# <a name="inferredlabels-function"></a>De functie InferredLabels

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket [](https://nuget.org/packages/)


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