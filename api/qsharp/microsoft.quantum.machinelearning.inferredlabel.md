---
uid: Microsoft.Quantum.MachineLearning.InferredLabel
title: De functie InferredLabel
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabel
qsharp.summary: Given a of classification probability and a bias, returns the label inferred from that probability.
ms.openlocfilehash: 46b24c283a01e6ac1c959ee4a6899591ee708ff7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848425"
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