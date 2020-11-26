---
uid: Microsoft.Quantum.MachineLearning.Misclassifications
title: Functie voor een niet-geclassificeerde classificatie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Misclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns indices for where each set of labels differs.
ms.openlocfilehash: e13a9b9b65931678d5d87878e81fa172329a28ea
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211675"
---
# <a name="misclassifications-function"></a>Functie voor een niet-geclassificeerde classificatie

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Op basis van een set van uitgestelde labels en een reeks juiste labels retourneert de indices voor waar elke set labels verschilt.

```qsharp
function Misclassifications (inferredLabels : Int[], actualLabels : Int[]) : Int[]
```


## <a name="input"></a>Invoer

### <a name="inferredlabels--int"></a>inferredLabels: [int](xref:microsoft.quantum.lang-ref.int)[]

De labels die zijn uitgesteld voor een bepaalde training of validatieset.


### <a name="actuallabels--int"></a>actualLabels: [int](xref:microsoft.quantum.lang-ref.int)[]

De werkelijke labels voor een bepaalde training of validatieset.



## <a name="output--int"></a>Output: [int](xref:microsoft.quantum.lang-ref.int)[]

Een matrix met indices `idx` `inferredLabels[idx] != actualLabels[idx]` .