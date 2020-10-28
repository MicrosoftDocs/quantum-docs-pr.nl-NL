---
uid: Microsoft.Quantum.MachineLearning.Misclassifications
title: Functie voor een niet-geclassificeerde classificatie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Misclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns indices for where each set of labels differs.
ms.openlocfilehash: 500c2910f7c5616c88ff6c70ab3cc16680e199fb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708472"
---
# <a name="misclassifications-function"></a><span data-ttu-id="edbc9-102">Functie voor een niet-geclassificeerde classificatie</span><span class="sxs-lookup"><span data-stu-id="edbc9-102">Misclassifications function</span></span>

<span data-ttu-id="edbc9-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="edbc9-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="edbc9-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="edbc9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="edbc9-105">Op basis van een set van uitgestelde labels en een reeks juiste labels retourneert de indices voor waar elke set labels verschilt.</span><span class="sxs-lookup"><span data-stu-id="edbc9-105">Given a set of inferred labels and a set of correct labels, returns indices for where each set of labels differs.</span></span>

```qsharp
function Misclassifications (inferredLabels : Int[], actualLabels : Int[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="edbc9-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="edbc9-106">Input</span></span>

### <a name="inferredlabels--int"></a><span data-ttu-id="edbc9-107">inferredLabels: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="edbc9-107">inferredLabels : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="edbc9-108">De labels die zijn uitgesteld voor een bepaalde training of validatieset.</span><span class="sxs-lookup"><span data-stu-id="edbc9-108">The labels inferred for a given training or validation set.</span></span>


### <a name="actuallabels--int"></a><span data-ttu-id="edbc9-109">actualLabels: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="edbc9-109">actualLabels : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="edbc9-110">De werkelijke labels voor een bepaalde training of validatieset.</span><span class="sxs-lookup"><span data-stu-id="edbc9-110">The true labels for a given training or validation set.</span></span>



## <a name="output--int"></a><span data-ttu-id="edbc9-111">Output: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="edbc9-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="edbc9-112">Een matrix met indices `idx` `inferredLabels[idx] != actualLabels[idx]` .</span><span class="sxs-lookup"><span data-stu-id="edbc9-112">An array of indices `idx` such that `inferredLabels[idx] != actualLabels[idx]`.</span></span>