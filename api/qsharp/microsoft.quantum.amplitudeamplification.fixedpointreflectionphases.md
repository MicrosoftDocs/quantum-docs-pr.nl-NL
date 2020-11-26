---
uid: Microsoft.Quantum.AmplitudeAmplification.FixedPointReflectionPhases
title: De functie FixedPointReflectionPhases
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: FixedPointReflectionPhases
qsharp.summary: Computes partial reflection phases for fixed-point amplitude amplification.
ms.openlocfilehash: 8cc1073447f5fae87ece38db64dcc312f6208899
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191445"
---
# <a name="fixedpointreflectionphases-function"></a><span data-ttu-id="c7738-102">De functie FixedPointReflectionPhases</span><span class="sxs-lookup"><span data-stu-id="c7738-102">FixedPointReflectionPhases function</span></span>

<span data-ttu-id="c7738-103">Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="c7738-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="c7738-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c7738-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c7738-105">Berekent gedeeltelijke reflectie fasen voor een amplitude versterking met een vaste komma.</span><span class="sxs-lookup"><span data-stu-id="c7738-105">Computes partial reflection phases for fixed-point amplitude amplification.</span></span>

```qsharp
function FixedPointReflectionPhases (nQueries : Int, successMin : Double) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a><span data-ttu-id="c7738-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="c7738-106">Input</span></span>

### <a name="nqueries--int"></a><span data-ttu-id="c7738-107">nQueries: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c7738-107">nQueries : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c7738-108">Aantal query's naar de status voorbereiding Oracle.</span><span class="sxs-lookup"><span data-stu-id="c7738-108">Number of queries to the state preparation oracle.</span></span> <span data-ttu-id="c7738-109">Moet een oneven geheel getal zijn.</span><span class="sxs-lookup"><span data-stu-id="c7738-109">Must be an odd integer.</span></span>


### <a name="successmin--double"></a><span data-ttu-id="c7738-110">successMin: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c7738-110">successMin : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c7738-111">Doel minimale succes volle kans.</span><span class="sxs-lookup"><span data-stu-id="c7738-111">Target minimum success probability.</span></span>



## <a name="output--reflectionphases"></a><span data-ttu-id="c7738-112">Uitvoer: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="c7738-112">Output : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="c7738-113">Matrix van fasen die kunnen worden gebruikt in de implementatie van een Quantum ring-algoritme met een vaste punt.</span><span class="sxs-lookup"><span data-stu-id="c7738-113">Array of phases that can be used in fixed-point amplitude amplification quantum algorithm implementation.</span></span>

## <a name="references"></a><span data-ttu-id="c7738-114">Referenties</span><span class="sxs-lookup"><span data-stu-id="c7738-114">References</span></span>

<span data-ttu-id="c7738-115">We gebruiken de fasen in ' amplitude versterking met een optimaal aantal Query's '</span><span class="sxs-lookup"><span data-stu-id="c7738-115">We use the phases in "Fixed-Point Amplitude Amplification with an Optimal Number of Queries"</span></span>

- <span data-ttu-id="c7738-116">[YoderLowChuang2014](https://arxiv.org/abs/1409.3305) Zie ook ' methodologie van samengestelde Quantum Gates '</span><span class="sxs-lookup"><span data-stu-id="c7738-116">[YoderLowChuang2014](https://arxiv.org/abs/1409.3305) See also "Methodology of composite quantum gates"</span></span>
- <span data-ttu-id="c7738-117">[LowYoderChuang2016](https://arxiv.org/abs/1603.03996) voor fasen in de `RotationPhases` indeling.</span><span class="sxs-lookup"><span data-stu-id="c7738-117">[LowYoderChuang2016](https://arxiv.org/abs/1603.03996) for phases in the `RotationPhases` format.</span></span>