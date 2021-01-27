---
uid: Microsoft.Quantum.Random.TransformedContinuousDistribution
title: De functie TransformedContinuousDistribution
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: TransformedContinuousDistribution
qsharp.summary: Given a continuous distribution, returns a new distribution that transforms the original by a given function.
ms.openlocfilehash: 353442a4245a9e20bb1e4c46d2e8a84d4c9534b0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857774"
---
# <a name="transformedcontinuousdistribution-function"></a><span data-ttu-id="0b6f7-102">De functie TransformedContinuousDistribution</span><span class="sxs-lookup"><span data-stu-id="0b6f7-102">TransformedContinuousDistribution function</span></span>

<span data-ttu-id="0b6f7-103">Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="0b6f7-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="0b6f7-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="0b6f7-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="0b6f7-105">Op basis van een continue distributie retourneert een nieuwe distributie waarmee het origineel door een bepaalde functie wordt getransformeerd.</span><span class="sxs-lookup"><span data-stu-id="0b6f7-105">Given a continuous distribution, returns a new distribution that transforms the original by a given function.</span></span>

```qsharp
function TransformedContinuousDistribution (transform : (Double -> Double), distribution : Microsoft.Quantum.Random.ContinuousDistribution) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a><span data-ttu-id="0b6f7-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="0b6f7-106">Input</span></span>

### <a name="transform--double---double"></a><span data-ttu-id="0b6f7-107">transformeren: [dubbele](xref:microsoft.quantum.lang-ref.double) -> [dubbele precisie](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="0b6f7-107">transform : [Double](xref:microsoft.quantum.lang-ref.double) -> [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="0b6f7-108">Een functie waarmee de variates van de oorspronkelijke distributie wordt getransformeerd naar de getransformeerde distributie.</span><span class="sxs-lookup"><span data-stu-id="0b6f7-108">A function that transforms variates of the original distribution to the transformed distribution.</span></span>


### <a name="distribution--continuousdistribution"></a><span data-ttu-id="0b6f7-109">distributie: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="0b6f7-109">distribution : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="0b6f7-110">De oorspronkelijke verdeling die moet worden getransformeerd.</span><span class="sxs-lookup"><span data-stu-id="0b6f7-110">The original distribution to be transformed.</span></span>



## <a name="output--continuousdistribution"></a><span data-ttu-id="0b6f7-111">Uitvoer: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="0b6f7-111">Output : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="0b6f7-112">Een nieuwe distributie gerelateerd aan `distribution` de trans formatie die wordt gegeven door `transform` .</span><span class="sxs-lookup"><span data-stu-id="0b6f7-112">A new distribution related to `distribution` by the transformation given by `transform`.</span></span>

## <a name="example"></a><span data-ttu-id="0b6f7-113">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="0b6f7-113">Example</span></span>

<span data-ttu-id="0b6f7-114">De volgende twee distributies zijn identiek:</span><span class="sxs-lookup"><span data-stu-id="0b6f7-114">The following two distributions are identical:</span></span>

```qsharp
let dist1 = ContinuousUniformDistribution(1.0, 2.0);
let dist2 = TransformedContinuousDistribution(
    PlusD(1.0, _),
    ContinuousUniformDistribution(0.0, 1.0)
);
```