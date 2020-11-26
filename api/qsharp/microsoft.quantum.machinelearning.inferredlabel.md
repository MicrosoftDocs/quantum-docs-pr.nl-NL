---
uid: Microsoft.Quantum.MachineLearning.InferredLabel
title: De functie InferredLabel
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabel
qsharp.summary: Given a of classification probability and a bias, returns the label inferred from that probability.
ms.openlocfilehash: b64bb1ec52d2456ee1b627b920890223d173533b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211777"
---
# <a name="inferredlabel-function"></a>De functie InferredLabel

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Als gevolg van een classificatie waarschijnlijkheid en een bias, retourneert het label afgeleid van die kans.

```qsharp
function InferredLabel (bias : Double, probability : Double) : Int
```


## <a name="input"></a>Invoer

### <a name="bias--double"></a>afwijking: [dubbel](xref:microsoft.quantum.lang-ref.double)

De afwijking tussen twee klassen, meestal het resultaat van het trainen van een classificatie.


### <a name="probability--double"></a>waarschijnlijkheid: [dubbel](xref:microsoft.quantum.lang-ref.double)

Een classificatie waarschijnlijkheid voor een bepaald voor beeld, wat vaak het resultaat is van het schatten van de classificatie frequentie.



## <a name="output--int"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)

Het label is afgeleid van de gegeven classificatie waarschijnlijkheid.