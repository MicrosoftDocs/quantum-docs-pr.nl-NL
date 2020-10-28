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
# <a name="inferredlabels-function"></a><span data-ttu-id="b7757-102">De functie InferredLabels</span><span class="sxs-lookup"><span data-stu-id="b7757-102">InferredLabels function</span></span>

<span data-ttu-id="b7757-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="b7757-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="b7757-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b7757-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b7757-105">Op basis van een matrix met classificatie kansen en een bias, retourneert het label dat wordt afgeleid van elke waarschijnlijkheid.</span><span class="sxs-lookup"><span data-stu-id="b7757-105">Given an array of classification probabilities and a bias, returns the label inferred from each probability.</span></span>

```qsharp
function InferredLabels (bias : Double, probabilities : Double[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="b7757-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="b7757-106">Input</span></span>

### <a name="bias--double"></a><span data-ttu-id="b7757-107">afwijking: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b7757-107">bias : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b7757-108">De afwijking tussen twee klassen, meestal het resultaat van het trainen van een classificatie.</span><span class="sxs-lookup"><span data-stu-id="b7757-108">The bias between two classes, typically the result of training a classifier.</span></span>


### <a name="probabilities--double"></a><span data-ttu-id="b7757-109">kansen: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="b7757-109">probabilities : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="b7757-110">Een matrix met classificatie kansen voor een aantal steek proeven, meestal het resultaat van het schatten van classificatie frequenties.</span><span class="sxs-lookup"><span data-stu-id="b7757-110">An array of classification probabilities for a set of samples, typically resulting from estimating classification frequencies.</span></span>



## <a name="output--int"></a><span data-ttu-id="b7757-111">Output: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="b7757-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="b7757-112">Het label is afgeleid van elke classificatie waarschijnlijkheid.</span><span class="sxs-lookup"><span data-stu-id="b7757-112">The label inferred from each classification probability.</span></span>