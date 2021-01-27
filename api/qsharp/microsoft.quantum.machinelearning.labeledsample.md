---
uid: Microsoft.Quantum.MachineLearning.LabeledSample
title: Door de gebruiker gedefinieerd LabeledSample-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: LabeledSample
qsharp.summary: A sample, labeled with a class to which that sample belongs.
ms.openlocfilehash: b357aae20b5bddb968ce1906fed3c1001efbfde7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846967"
---
# <a name="labeledsample-user-defined-type"></a><span data-ttu-id="f5b38-102">Door de gebruiker gedefinieerd LabeledSample-type</span><span class="sxs-lookup"><span data-stu-id="f5b38-102">LabeledSample user defined type</span></span>

<span data-ttu-id="f5b38-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="f5b38-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="f5b38-104">Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="f5b38-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="f5b38-105">Een voor beeld, voorzien van een klasse waarvan het voor beeld deel uitmaakt.</span><span class="sxs-lookup"><span data-stu-id="f5b38-105">A sample, labeled with a class to which that sample belongs.</span></span>

```qsharp

newtype LabeledSample = (Features : Double[], Label : Int);
```



## <a name="named-items"></a><span data-ttu-id="f5b38-106">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="f5b38-106">Named Items</span></span>

### <a name="features--double"></a><span data-ttu-id="f5b38-107">Functies: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="f5b38-107">Features : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="f5b38-108">Een vector van functies voor het gegeven voor beeld.</span><span class="sxs-lookup"><span data-stu-id="f5b38-108">A vector of features for the given sample.</span></span>
### <a name="label--int"></a><span data-ttu-id="f5b38-109">Label: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f5b38-109">Label : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f5b38-110">Een geheel getal voor de klasse waarvan dit voor beeld deel uitmaakt.</span><span class="sxs-lookup"><span data-stu-id="f5b38-110">An integer label for the class to which this sample belongs.</span></span>