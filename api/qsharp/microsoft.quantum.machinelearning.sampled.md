---
uid: Microsoft.Quantum.MachineLearning.Sampled
title: Voorbeeld functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Sampled
qsharp.summary: Samples a given array, using the given schedule.
ms.openlocfilehash: ddff72bbed6f20e8e0ceb3bfe3fc50a3da0bd2a9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211624"
---
# <a name="sampled-function"></a><span data-ttu-id="637c6-102">Voorbeeld functie</span><span class="sxs-lookup"><span data-stu-id="637c6-102">Sampled function</span></span>

<span data-ttu-id="637c6-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="637c6-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="637c6-104">Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="637c6-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="637c6-105">Voor beelden van een bepaalde matrix, met behulp van het opgegeven schema.</span><span class="sxs-lookup"><span data-stu-id="637c6-105">Samples a given array, using the given schedule.</span></span>

```qsharp
function Sampled<'T> (schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, values : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="637c6-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="637c6-106">Input</span></span>

### <a name="schedule--samplingschedule"></a><span data-ttu-id="637c6-107">planning: [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="637c6-107">schedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="637c6-108">Een schema dat moet worden gebruikt in sampling waarden.</span><span class="sxs-lookup"><span data-stu-id="637c6-108">A schedule to use in sampling values.</span></span>


### <a name="values--t"></a><span data-ttu-id="637c6-109">waarden: ' []</span><span class="sxs-lookup"><span data-stu-id="637c6-109">values : 'T[]</span></span>

<span data-ttu-id="637c6-110">Een matrix met waarden waarvan u een steek proef wilt maken.</span><span class="sxs-lookup"><span data-stu-id="637c6-110">An array of values to be sampled.</span></span>



## <a name="output--t"></a><span data-ttu-id="637c6-111">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="637c6-111">Output : 'T[]</span></span>

<span data-ttu-id="637c6-112">Een matrix met elementen van waarden, volgens het opgegeven schema.</span><span class="sxs-lookup"><span data-stu-id="637c6-112">An array of elements from values, following the given schedule.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="637c6-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="637c6-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="637c6-114">T</span><span class="sxs-lookup"><span data-stu-id="637c6-114">'T</span></span>

