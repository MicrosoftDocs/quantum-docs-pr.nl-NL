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
# <a name="inferredlabel-function"></a><span data-ttu-id="6471b-102">De functie InferredLabel</span><span class="sxs-lookup"><span data-stu-id="6471b-102">InferredLabel function</span></span>

<span data-ttu-id="6471b-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="6471b-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="6471b-104">Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="6471b-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="6471b-105">Als gevolg van een classificatie waarschijnlijkheid en een bias, retourneert het label afgeleid van die kans.</span><span class="sxs-lookup"><span data-stu-id="6471b-105">Given a of classification probability and a bias, returns the label inferred from that probability.</span></span>

```qsharp
function InferredLabel (bias : Double, probability : Double) : Int
```


## <a name="input"></a><span data-ttu-id="6471b-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="6471b-106">Input</span></span>

### <a name="bias--double"></a><span data-ttu-id="6471b-107">afwijking: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="6471b-107">bias : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="6471b-108">De afwijking tussen twee klassen, meestal het resultaat van het trainen van een classificatie.</span><span class="sxs-lookup"><span data-stu-id="6471b-108">The bias between two classes, typically the result of training a classifier.</span></span>


### <a name="probability--double"></a><span data-ttu-id="6471b-109">waarschijnlijkheid: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="6471b-109">probability : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="6471b-110">Een classificatie waarschijnlijkheid voor een bepaald voor beeld, wat vaak het resultaat is van het schatten van de classificatie frequentie.</span><span class="sxs-lookup"><span data-stu-id="6471b-110">A classification probabilities for a particular sample, typically resulting from estimating its classification frequency.</span></span>



## <a name="output--int"></a><span data-ttu-id="6471b-111">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6471b-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6471b-112">Het label is afgeleid van de gegeven classificatie waarschijnlijkheid.</span><span class="sxs-lookup"><span data-stu-id="6471b-112">The label inferred from the given classification probability.</span></span>