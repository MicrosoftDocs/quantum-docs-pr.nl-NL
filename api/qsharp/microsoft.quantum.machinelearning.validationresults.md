---
uid: Microsoft.Quantum.MachineLearning.ValidationResults
title: Door de gebruiker gedefinieerd ValidationResults-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ValidationResults
qsharp.summary: The results from having validated a classifier against a set of samples.
ms.openlocfilehash: 1e54a5a086035f5f8d36d777badb306156d99600
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706813"
---
# <a name="validationresults-user-defined-type"></a><span data-ttu-id="6fbec-102">Door de gebruiker gedefinieerd ValidationResults-type</span><span class="sxs-lookup"><span data-stu-id="6fbec-102">ValidationResults user defined type</span></span>

<span data-ttu-id="6fbec-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="6fbec-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="6fbec-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6fbec-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6fbec-105">De resultaten van het valideren van een classificatie op basis van een reeks voor beelden.</span><span class="sxs-lookup"><span data-stu-id="6fbec-105">The results from having validated a classifier against a set of samples.</span></span>

```qsharp

newtype ValidationResults = (NMisclassifications : Int, NValidationSamples : Int);
```



## <a name="named-items"></a><span data-ttu-id="6fbec-106">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="6fbec-106">Named Items</span></span>

### <a name="nmisclassifications--int"></a><span data-ttu-id="6fbec-107">NMisclassifications: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6fbec-107">NMisclassifications : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6fbec-108">Het aantal misclassificaties dat tijdens de validatie wordt waargenomen.</span><span class="sxs-lookup"><span data-stu-id="6fbec-108">The number of misclassifications observed during validation.</span></span>
### <a name="nvalidationsamples--int"></a><span data-ttu-id="6fbec-109">NValidationSamples: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6fbec-109">NValidationSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

