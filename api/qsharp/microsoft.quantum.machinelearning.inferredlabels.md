---
uid: Microsoft.Quantum.MachineLearning.InferredLabels
title: De functie InferredLabels
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabels
qsharp.summary: Given an array of classification probabilities and a bias, returns the label inferred from each probability.
ms.openlocfilehash: 576b4b1f11fc21476bbb019d4b0326981294528c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848393"
---
# <a name="inferredlabels-function"></a><span data-ttu-id="97fec-102">De functie InferredLabels</span><span class="sxs-lookup"><span data-stu-id="97fec-102">InferredLabels function</span></span>

<span data-ttu-id="97fec-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="97fec-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="97fec-104">Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="97fec-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="97fec-105">Op basis van een matrix met classificatie kansen en een bias, retourneert het label dat wordt afgeleid van elke waarschijnlijkheid.</span><span class="sxs-lookup"><span data-stu-id="97fec-105">Given an array of classification probabilities and a bias, returns the label inferred from each probability.</span></span>

```qsharp
function InferredLabels (bias : Double, probabilities : Double[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="97fec-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="97fec-106">Input</span></span>

### <a name="bias--double"></a><span data-ttu-id="97fec-107">afwijking: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="97fec-107">bias : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="97fec-108">De afwijking tussen twee klassen, meestal het resultaat van het trainen van een classificatie.</span><span class="sxs-lookup"><span data-stu-id="97fec-108">The bias between two classes, typically the result of training a classifier.</span></span>


### <a name="probabilities--double"></a><span data-ttu-id="97fec-109">kansen: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="97fec-109">probabilities : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="97fec-110">Een matrix met classificatie kansen voor een aantal steek proeven, meestal het resultaat van het schatten van classificatie frequenties.</span><span class="sxs-lookup"><span data-stu-id="97fec-110">An array of classification probabilities for a set of samples, typically resulting from estimating classification frequencies.</span></span>



## <a name="output--int"></a><span data-ttu-id="97fec-111">Output: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="97fec-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="97fec-112">Het label is afgeleid van elke classificatie waarschijnlijkheid.</span><span class="sxs-lookup"><span data-stu-id="97fec-112">The label inferred from each classification probability.</span></span>