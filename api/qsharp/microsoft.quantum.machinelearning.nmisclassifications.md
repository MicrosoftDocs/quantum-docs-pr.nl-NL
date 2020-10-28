---
uid: Microsoft.Quantum.MachineLearning.NMisclassifications
title: De functie NMisclassifications
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: NMisclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns the number of indices at which each set of labels differ.
ms.openlocfilehash: 9e356d68233519978e007e5a2999ca1be8cb7f83
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701367"
---
# <a name="nmisclassifications-function"></a>De functie NMisclassifications

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket [](https://nuget.org/packages/)


Op basis van een set van uitgestelde labels en een reeks juiste labels retourneert het aantal indexen waarbij elke set labels verschilt.

```qsharp
function NMisclassifications (proposed : Int[], actual : Int[]) : Int
```


## <a name="input"></a>Invoer

### <a name="proposed--int"></a>voorgesteld: [int](xref:microsoft.quantum.lang-ref.int)[]




### <a name="actual--int"></a>werkelijk: [int](xref:microsoft.quantum.lang-ref.int)[]





## <a name="output--int"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal indexen `idx` zoals dat `inferredLabels[idx] != actualLabels[idx]` .