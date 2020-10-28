---
uid: Microsoft.Quantum.MachineLearning.Sampled
title: Voorbeeld functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Sampled
qsharp.summary: Samples a given array, using the given schedule.
ms.openlocfilehash: 9f9f91bc50861c5b31a76e28050189d13efda71e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707975"
---
# <a name="sampled-function"></a><span data-ttu-id="69fee-102">Voorbeeld functie</span><span class="sxs-lookup"><span data-stu-id="69fee-102">Sampled function</span></span>

<span data-ttu-id="69fee-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="69fee-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="69fee-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="69fee-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="69fee-105">Voor beelden van een bepaalde matrix, met behulp van het opgegeven schema.</span><span class="sxs-lookup"><span data-stu-id="69fee-105">Samples a given array, using the given schedule.</span></span>

```qsharp
function Sampled<'T> (schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, values : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="69fee-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="69fee-106">Input</span></span>

### <a name="schedule--samplingschedule"></a><span data-ttu-id="69fee-107">planning: [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="69fee-107">schedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="69fee-108">Een schema dat moet worden gebruikt in sampling waarden.</span><span class="sxs-lookup"><span data-stu-id="69fee-108">A schedule to use in sampling values.</span></span>


### <a name="values--t"></a><span data-ttu-id="69fee-109">waarden: ' []</span><span class="sxs-lookup"><span data-stu-id="69fee-109">values : 'T[]</span></span>

<span data-ttu-id="69fee-110">Een matrix met waarden waarvan u een steek proef wilt maken.</span><span class="sxs-lookup"><span data-stu-id="69fee-110">An array of values to be sampled.</span></span>



## <a name="output--t"></a><span data-ttu-id="69fee-111">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="69fee-111">Output : 'T[]</span></span>

<span data-ttu-id="69fee-112">Een matrix met elementen van waarden, volgens het opgegeven schema.</span><span class="sxs-lookup"><span data-stu-id="69fee-112">An array of elements from values, following the given schedule.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="69fee-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="69fee-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="69fee-114">T</span><span class="sxs-lookup"><span data-stu-id="69fee-114">'T</span></span>

