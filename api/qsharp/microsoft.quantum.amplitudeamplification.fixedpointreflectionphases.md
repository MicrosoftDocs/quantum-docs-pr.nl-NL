---
uid: Microsoft.Quantum.AmplitudeAmplification.FixedPointReflectionPhases
title: De functie FixedPointReflectionPhases
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: FixedPointReflectionPhases
qsharp.summary: Computes partial reflection phases for fixed-point amplitude amplification.
ms.openlocfilehash: 6ab2a8c6cb0b390f96aa13ece5d5b89c196a6107
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707734"
---
# <a name="fixedpointreflectionphases-function"></a><span data-ttu-id="23563-102">De functie FixedPointReflectionPhases</span><span class="sxs-lookup"><span data-stu-id="23563-102">FixedPointReflectionPhases function</span></span>

<span data-ttu-id="23563-103">Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="23563-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="23563-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="23563-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="23563-105">Berekent gedeeltelijke reflectie fasen voor een amplitude versterking met een vaste komma.</span><span class="sxs-lookup"><span data-stu-id="23563-105">Computes partial reflection phases for fixed-point amplitude amplification.</span></span>

```qsharp
function FixedPointReflectionPhases (nQueries : Int, successMin : Double) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a><span data-ttu-id="23563-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="23563-106">Input</span></span>

### <a name="nqueries--int"></a><span data-ttu-id="23563-107">nQueries: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="23563-107">nQueries : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="23563-108">Aantal query's naar de status voorbereiding Oracle.</span><span class="sxs-lookup"><span data-stu-id="23563-108">Number of queries to the state preparation oracle.</span></span> <span data-ttu-id="23563-109">Moet een oneven geheel getal zijn.</span><span class="sxs-lookup"><span data-stu-id="23563-109">Must be an odd integer.</span></span>


### <a name="successmin--double"></a><span data-ttu-id="23563-110">successMin: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="23563-110">successMin : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="23563-111">Doel minimale succes volle kans.</span><span class="sxs-lookup"><span data-stu-id="23563-111">Target minimum success probability.</span></span>



## <a name="output--reflectionphases"></a><span data-ttu-id="23563-112">Uitvoer: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="23563-112">Output : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="23563-113">Matrix van fasen die kunnen worden gebruikt in de implementatie van een Quantum ring-algoritme met een vaste punt.</span><span class="sxs-lookup"><span data-stu-id="23563-113">Array of phases that can be used in fixed-point amplitude amplification quantum algorithm implementation.</span></span>

## <a name="references"></a><span data-ttu-id="23563-114">Naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="23563-114">References</span></span>

<span data-ttu-id="23563-115">We gebruiken de fasen in ' amplitude versterking met een optimaal aantal Query's '</span><span class="sxs-lookup"><span data-stu-id="23563-115">We use the phases in "Fixed-Point Amplitude Amplification with an Optimal Number of Queries"</span></span>

- <span data-ttu-id="23563-116">[YoderLowChuang2014](https://arxiv.org/abs/1409.3305) Zie ook ' methodologie van samengestelde Quantum Gates '</span><span class="sxs-lookup"><span data-stu-id="23563-116">[YoderLowChuang2014](https://arxiv.org/abs/1409.3305) See also "Methodology of composite quantum gates"</span></span>
- <span data-ttu-id="23563-117">[LowYoderChuang2016](https://arxiv.org/abs/1603.03996) voor fasen in de `RotationPhases` indeling.</span><span class="sxs-lookup"><span data-stu-id="23563-117">[LowYoderChuang2016](https://arxiv.org/abs/1603.03996) for phases in the `RotationPhases` format.</span></span>