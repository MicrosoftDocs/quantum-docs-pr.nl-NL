---
uid: Microsoft.Quantum.MachineLearning.ValidationResults
title: Door de gebruiker gedefinieerd ValidationResults-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ValidationResults
qsharp.summary: The results from having validated a classifier against a set of samples.
ms.openlocfilehash: 42bfab7fd1f9372d9394f2eaf2d698b39b4307e1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211488"
---
# <a name="validationresults-user-defined-type"></a><span data-ttu-id="8ca30-102">Door de gebruiker gedefinieerd ValidationResults-type</span><span class="sxs-lookup"><span data-stu-id="8ca30-102">ValidationResults user defined type</span></span>

<span data-ttu-id="8ca30-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="8ca30-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="8ca30-104">Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="8ca30-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="8ca30-105">De resultaten van het valideren van een classificatie op basis van een reeks voor beelden.</span><span class="sxs-lookup"><span data-stu-id="8ca30-105">The results from having validated a classifier against a set of samples.</span></span>

```qsharp

newtype ValidationResults = (NMisclassifications : Int, NValidationSamples : Int);
```



## <a name="named-items"></a><span data-ttu-id="8ca30-106">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="8ca30-106">Named Items</span></span>

### <a name="nmisclassifications--int"></a><span data-ttu-id="8ca30-107">NMisclassifications: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8ca30-107">NMisclassifications : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8ca30-108">Het aantal misclassificaties dat tijdens de validatie wordt waargenomen.</span><span class="sxs-lookup"><span data-stu-id="8ca30-108">The number of misclassifications observed during validation.</span></span>
### <a name="nvalidationsamples--int"></a><span data-ttu-id="8ca30-109">NValidationSamples: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8ca30-109">NValidationSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

