---
uid: Microsoft.Quantum.MachineLearning.InferredLabel
title: De functie InferredLabel
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabel
qsharp.summary: Given a of classification probability and a bias, returns the label inferred from that probability.
ms.openlocfilehash: 46b24c283a01e6ac1c959ee4a6899591ee708ff7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848425"
---
# <a name="inferredlabel-function"></a><span data-ttu-id="24e10-102">De functie InferredLabel</span><span class="sxs-lookup"><span data-stu-id="24e10-102">InferredLabel function</span></span>

<span data-ttu-id="24e10-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="24e10-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="24e10-104">Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="24e10-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="24e10-105">Als gevolg van een classificatie waarschijnlijkheid en een bias, retourneert het label afgeleid van die kans.</span><span class="sxs-lookup"><span data-stu-id="24e10-105">Given a of classification probability and a bias, returns the label inferred from that probability.</span></span>

```qsharp
function InferredLabel (bias : Double, probability : Double) : Int
```


## <a name="input"></a><span data-ttu-id="24e10-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="24e10-106">Input</span></span>

### <a name="bias--double"></a><span data-ttu-id="24e10-107">afwijking: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="24e10-107">bias : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="24e10-108">De afwijking tussen twee klassen, meestal het resultaat van het trainen van een classificatie.</span><span class="sxs-lookup"><span data-stu-id="24e10-108">The bias between two classes, typically the result of training a classifier.</span></span>


### <a name="probability--double"></a><span data-ttu-id="24e10-109">waarschijnlijkheid: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="24e10-109">probability : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="24e10-110">Een classificatie waarschijnlijkheid voor een bepaald voor beeld, wat vaak het resultaat is van het schatten van de classificatie frequentie.</span><span class="sxs-lookup"><span data-stu-id="24e10-110">A classification probabilities for a particular sample, typically resulting from estimating its classification frequency.</span></span>



## <a name="output--int"></a><span data-ttu-id="24e10-111">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="24e10-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="24e10-112">Het label is afgeleid van de gegeven classificatie waarschijnlijkheid.</span><span class="sxs-lookup"><span data-stu-id="24e10-112">The label inferred from the given classification probability.</span></span>