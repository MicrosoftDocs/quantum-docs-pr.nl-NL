---
uid: Microsoft.Quantum.MachineLearning.NMisclassifications
title: De functie NMisclassifications
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: NMisclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns the number of indices at which each set of labels differ.
ms.openlocfilehash: 30d049ba54630cd2f5f350280bad7f587599f459
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196307"
---
# <a name="nmisclassifications-function"></a>De functie NMisclassifications

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Op basis van een set van uitgestelde labels en een reeks juiste labels retourneert het aantal indexen waarbij elke set labels verschilt.

```qsharp
function NMisclassifications (proposed : Int[], actual : Int[]) : Int
```


## <a name="input"></a>Invoer

### <a name="proposed--int"></a>voorgesteld: [int](xref:microsoft.quantum.lang-ref.int)[]




### <a name="actual--int"></a>werkelijk: [int](xref:microsoft.quantum.lang-ref.int)[]





## <a name="output--int"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal indexen `idx` zoals dat `inferredLabels[idx] != actualLabels[idx]` .