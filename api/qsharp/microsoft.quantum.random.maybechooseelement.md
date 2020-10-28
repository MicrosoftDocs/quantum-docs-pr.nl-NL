---
uid: Microsoft.Quantum.Random.MaybeChooseElement
title: Bewerking MaybeChooseElement
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: MaybeChooseElement
qsharp.summary: Given an array of data and an a distribution over its indices, attempts to choose an element at random.
ms.openlocfilehash: 12640d9dc3aad301146eff7bcbbaae33d3ccd420
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707866"
---
# <a name="maybechooseelement-operation"></a><span data-ttu-id="bfc55-102">Bewerking MaybeChooseElement</span><span class="sxs-lookup"><span data-stu-id="bfc55-102">MaybeChooseElement operation</span></span>

<span data-ttu-id="bfc55-103">Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="bfc55-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="bfc55-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bfc55-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bfc55-105">Op basis van een matrix met gegevens en een distributie over de indices probeert een wille keurig element te kiezen.</span><span class="sxs-lookup"><span data-stu-id="bfc55-105">Given an array of data and an a distribution over its indices, attempts to choose an element at random.</span></span>

```qsharp
operation MaybeChooseElement<'T> (data : 'T[], indexDistribution : Microsoft.Quantum.Random.DiscreteDistribution) : (Bool, 'T)
```


## <a name="input"></a><span data-ttu-id="bfc55-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="bfc55-106">Input</span></span>

### <a name="data--t"></a><span data-ttu-id="bfc55-107">gegevens: ' []</span><span class="sxs-lookup"><span data-stu-id="bfc55-107">data : 'T[]</span></span>

<span data-ttu-id="bfc55-108">De matrix waaruit een element moet worden gekozen.</span><span class="sxs-lookup"><span data-stu-id="bfc55-108">The array from which an element should be chosen.</span></span>


### <a name="indexdistribution--discretedistribution"></a><span data-ttu-id="bfc55-109">indexDistribution: [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="bfc55-109">indexDistribution : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="bfc55-110">Een distributie over de indices van `data` .</span><span class="sxs-lookup"><span data-stu-id="bfc55-110">A distribution over the indices of `data`.</span></span>



## <a name="output--boolt"></a><span data-ttu-id="bfc55-111">Uitvoer: ([BOOL](xref:microsoft.quantum.lang-ref.bool), 't)</span><span class="sxs-lookup"><span data-stu-id="bfc55-111">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="bfc55-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="bfc55-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="bfc55-113">T</span><span class="sxs-lookup"><span data-stu-id="bfc55-113">'T</span></span>

