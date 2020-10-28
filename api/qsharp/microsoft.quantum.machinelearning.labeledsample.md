---
uid: Microsoft.Quantum.MachineLearning.LabeledSample
title: Door de gebruiker gedefinieerd LabeledSample-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: LabeledSample
qsharp.summary: A sample, labeled with a class to which that sample belongs.
ms.openlocfilehash: 8b4afa1eaf7ca69938b2606163cd1ec17a1ad80f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702051"
---
# <a name="labeledsample-user-defined-type"></a><span data-ttu-id="58ecb-102">Door de gebruiker gedefinieerd LabeledSample-type</span><span class="sxs-lookup"><span data-stu-id="58ecb-102">LabeledSample user defined type</span></span>

<span data-ttu-id="58ecb-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="58ecb-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="58ecb-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="58ecb-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="58ecb-105">Een voor beeld, voorzien van een klasse waarvan het voor beeld deel uitmaakt.</span><span class="sxs-lookup"><span data-stu-id="58ecb-105">A sample, labeled with a class to which that sample belongs.</span></span>

```qsharp

newtype LabeledSample = (Features : Double[], Label : Int);
```



## <a name="named-items"></a><span data-ttu-id="58ecb-106">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="58ecb-106">Named Items</span></span>

### <a name="features--double"></a><span data-ttu-id="58ecb-107">Functies: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="58ecb-107">Features : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="58ecb-108">Een vector van functies voor het gegeven voor beeld.</span><span class="sxs-lookup"><span data-stu-id="58ecb-108">A vector of features for the given sample.</span></span>
### <a name="label--int"></a><span data-ttu-id="58ecb-109">Label: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="58ecb-109">Label : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="58ecb-110">Een geheel getal voor de klasse waarvan dit voor beeld deel uitmaakt.</span><span class="sxs-lookup"><span data-stu-id="58ecb-110">An integer label for the class to which this sample belongs.</span></span>