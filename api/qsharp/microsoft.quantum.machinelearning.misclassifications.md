---
uid: Microsoft.Quantum.MachineLearning.Misclassifications
title: Functie voor een niet-geclassificeerde classificatie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Misclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns indices for where each set of labels differs.
ms.openlocfilehash: 3913395fbd9f7cf96732c17ca0c726289e5087ed
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853928"
---
# <a name="misclassifications-function"></a><span data-ttu-id="b0e8e-102">Functie voor een niet-geclassificeerde classificatie</span><span class="sxs-lookup"><span data-stu-id="b0e8e-102">Misclassifications function</span></span>

<span data-ttu-id="b0e8e-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="b0e8e-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="b0e8e-104">Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="b0e8e-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="b0e8e-105">Op basis van een set van uitgestelde labels en een reeks juiste labels retourneert de indices voor waar elke set labels verschilt.</span><span class="sxs-lookup"><span data-stu-id="b0e8e-105">Given a set of inferred labels and a set of correct labels, returns indices for where each set of labels differs.</span></span>

```qsharp
function Misclassifications (inferredLabels : Int[], actualLabels : Int[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="b0e8e-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="b0e8e-106">Input</span></span>

### <a name="inferredlabels--int"></a><span data-ttu-id="b0e8e-107">inferredLabels: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="b0e8e-107">inferredLabels : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="b0e8e-108">De labels die zijn uitgesteld voor een bepaalde training of validatieset.</span><span class="sxs-lookup"><span data-stu-id="b0e8e-108">The labels inferred for a given training or validation set.</span></span>


### <a name="actuallabels--int"></a><span data-ttu-id="b0e8e-109">actualLabels: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="b0e8e-109">actualLabels : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="b0e8e-110">De werkelijke labels voor een bepaalde training of validatieset.</span><span class="sxs-lookup"><span data-stu-id="b0e8e-110">The true labels for a given training or validation set.</span></span>



## <a name="output--int"></a><span data-ttu-id="b0e8e-111">Output: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="b0e8e-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="b0e8e-112">Een matrix met indices `idx` `inferredLabels[idx] != actualLabels[idx]` .</span><span class="sxs-lookup"><span data-stu-id="b0e8e-112">An array of indices `idx` such that `inferredLabels[idx] != actualLabels[idx]`.</span></span>

## <a name="example"></a><span data-ttu-id="b0e8e-113">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="b0e8e-113">Example</span></span>

```qsharp
let misclassifications = Misclassifications([0, 1, 0, 0], [0, 1, 1, 0]);
Message($"{misclassifications}"); // Will print [2].
```