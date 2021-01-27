---
uid: Microsoft.Quantum.Random.MaybeChooseElement
title: Bewerking MaybeChooseElement
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: MaybeChooseElement
qsharp.summary: Given an array of data and an a distribution over its indices, attempts to choose an element at random.
ms.openlocfilehash: 86a69110fc92a2b6238cc757c09185c9fbcdb035
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856119"
---
# <a name="maybechooseelement-operation"></a><span data-ttu-id="51267-102">Bewerking MaybeChooseElement</span><span class="sxs-lookup"><span data-stu-id="51267-102">MaybeChooseElement operation</span></span>

<span data-ttu-id="51267-103">Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="51267-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="51267-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="51267-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="51267-105">Op basis van een matrix met gegevens en een distributie over de indices probeert een wille keurig element te kiezen.</span><span class="sxs-lookup"><span data-stu-id="51267-105">Given an array of data and an a distribution over its indices, attempts to choose an element at random.</span></span>

```qsharp
operation MaybeChooseElement<'T> (data : 'T[], indexDistribution : Microsoft.Quantum.Random.DiscreteDistribution) : (Bool, 'T)
```


## <a name="input"></a><span data-ttu-id="51267-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="51267-106">Input</span></span>

### <a name="data--t"></a><span data-ttu-id="51267-107">gegevens: ' []</span><span class="sxs-lookup"><span data-stu-id="51267-107">data : 'T[]</span></span>

<span data-ttu-id="51267-108">De matrix waaruit een element moet worden gekozen.</span><span class="sxs-lookup"><span data-stu-id="51267-108">The array from which an element should be chosen.</span></span>


### <a name="indexdistribution--discretedistribution"></a><span data-ttu-id="51267-109">indexDistribution: [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="51267-109">indexDistribution : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="51267-110">Een distributie over de indices van `data` .</span><span class="sxs-lookup"><span data-stu-id="51267-110">A distribution over the indices of `data`.</span></span>



## <a name="output--boolt"></a><span data-ttu-id="51267-111">Uitvoer: ([BOOL](xref:microsoft.quantum.lang-ref.bool), 't)</span><span class="sxs-lookup"><span data-stu-id="51267-111">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="51267-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="51267-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="51267-113">T</span><span class="sxs-lookup"><span data-stu-id="51267-113">'T</span></span>



## <a name="example"></a><span data-ttu-id="51267-114">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="51267-114">Example</span></span>

<span data-ttu-id="51267-115">De volgende letter Q # fragment kiest een wille keurig element uit een matrix:</span><span class="sxs-lookup"><span data-stu-id="51267-115">The following Q# snippet chooses an element at random from an array:</span></span>

```qsharp
let (succeeded, element) = MaybeChooseElement(
    data,
    DiscreteUniformDistribution(0, Length(data) - 1)
);
Fact(succeeded, "Index chosen by MaybeChooseElement was not valid.");
```