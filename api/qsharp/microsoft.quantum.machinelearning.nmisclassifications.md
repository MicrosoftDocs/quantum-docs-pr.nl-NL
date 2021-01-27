---
uid: Microsoft.Quantum.MachineLearning.NMisclassifications
title: De functie NMisclassifications
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: NMisclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns the number of indices at which each set of labels differ.
ms.openlocfilehash: adc7042d6108c7ec72d13340633824d3eaf5e18e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853905"
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

## <a name="example"></a>Voorbeeld

```qsharp
let nMisclassifications = NMisclassifications([1, 1, 0, 0], [0, 1, 1, 0]);
Message($"{nMisclassifications}"); // Will print 2.
```