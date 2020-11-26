---
uid: Microsoft.Quantum.Random.MaybeChooseElement
title: Bewerking MaybeChooseElement
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: MaybeChooseElement
qsharp.summary: Given an array of data and an a distribution over its indices, attempts to choose an element at random.
ms.openlocfilehash: 1a69c8d5a6ae022ceda9269e17434b740809b107
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192856"
---
# <a name="maybechooseelement-operation"></a><span data-ttu-id="088cc-102">Bewerking MaybeChooseElement</span><span class="sxs-lookup"><span data-stu-id="088cc-102">MaybeChooseElement operation</span></span>

<span data-ttu-id="088cc-103">Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="088cc-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="088cc-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="088cc-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="088cc-105">Op basis van een matrix met gegevens en een distributie over de indices probeert een wille keurig element te kiezen.</span><span class="sxs-lookup"><span data-stu-id="088cc-105">Given an array of data and an a distribution over its indices, attempts to choose an element at random.</span></span>

```qsharp
operation MaybeChooseElement<'T> (data : 'T[], indexDistribution : Microsoft.Quantum.Random.DiscreteDistribution) : (Bool, 'T)
```


## <a name="input"></a><span data-ttu-id="088cc-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="088cc-106">Input</span></span>

### <a name="data--t"></a><span data-ttu-id="088cc-107">gegevens: ' []</span><span class="sxs-lookup"><span data-stu-id="088cc-107">data : 'T[]</span></span>

<span data-ttu-id="088cc-108">De matrix waaruit een element moet worden gekozen.</span><span class="sxs-lookup"><span data-stu-id="088cc-108">The array from which an element should be chosen.</span></span>


### <a name="indexdistribution--discretedistribution"></a><span data-ttu-id="088cc-109">indexDistribution: [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="088cc-109">indexDistribution : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="088cc-110">Een distributie over de indices van `data` .</span><span class="sxs-lookup"><span data-stu-id="088cc-110">A distribution over the indices of `data`.</span></span>



## <a name="output--boolt"></a><span data-ttu-id="088cc-111">Uitvoer: ([BOOL](xref:microsoft.quantum.lang-ref.bool), 't)</span><span class="sxs-lookup"><span data-stu-id="088cc-111">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="088cc-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="088cc-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="088cc-113">T</span><span class="sxs-lookup"><span data-stu-id="088cc-113">'T</span></span>

