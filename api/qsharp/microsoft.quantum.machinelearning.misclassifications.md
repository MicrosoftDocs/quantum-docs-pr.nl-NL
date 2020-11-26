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
# <a name="misclassifications-function"></a><span data-ttu-id="419a6-102">Functie voor een niet-geclassificeerde classificatie</span><span class="sxs-lookup"><span data-stu-id="419a6-102">Misclassifications function</span></span>

<span data-ttu-id="419a6-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="419a6-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="419a6-104">Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="419a6-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="419a6-105">Op basis van een set van uitgestelde labels en een reeks juiste labels retourneert de indices voor waar elke set labels verschilt.</span><span class="sxs-lookup"><span data-stu-id="419a6-105">Given a set of inferred labels and a set of correct labels, returns indices for where each set of labels differs.</span></span>

```qsharp
function Misclassifications (inferredLabels : Int[], actualLabels : Int[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="419a6-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="419a6-106">Input</span></span>

### <a name="inferredlabels--int"></a><span data-ttu-id="419a6-107">inferredLabels: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="419a6-107">inferredLabels : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="419a6-108">De labels die zijn uitgesteld voor een bepaalde training of validatieset.</span><span class="sxs-lookup"><span data-stu-id="419a6-108">The labels inferred for a given training or validation set.</span></span>


### <a name="actuallabels--int"></a><span data-ttu-id="419a6-109">actualLabels: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="419a6-109">actualLabels : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="419a6-110">De werkelijke labels voor een bepaalde training of validatieset.</span><span class="sxs-lookup"><span data-stu-id="419a6-110">The true labels for a given training or validation set.</span></span>



## <a name="output--int"></a><span data-ttu-id="419a6-111">Output: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="419a6-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="419a6-112">Een matrix met indices `idx` `inferredLabels[idx] != actualLabels[idx]` .</span><span class="sxs-lookup"><span data-stu-id="419a6-112">An array of indices `idx` such that `inferredLabels[idx] != actualLabels[idx]`.</span></span>