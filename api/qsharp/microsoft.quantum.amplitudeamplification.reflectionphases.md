---
uid: Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
title: Door de gebruiker gedefinieerd ReflectionPhases-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ReflectionPhases
qsharp.summary: Phases for a sequence of partial reflections in amplitude amplification.
ms.openlocfilehash: 743ece778239c223573a3a8536ae8059cea09d5f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191343"
---
# <a name="reflectionphases-user-defined-type"></a><span data-ttu-id="8629c-102">Door de gebruiker gedefinieerd ReflectionPhases-type</span><span class="sxs-lookup"><span data-stu-id="8629c-102">ReflectionPhases user defined type</span></span>

<span data-ttu-id="8629c-103">Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="8629c-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="8629c-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8629c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8629c-105">Fasen voor een reeks van gedeeltelijke reflecties in amplitude versterking.</span><span class="sxs-lookup"><span data-stu-id="8629c-105">Phases for a sequence of partial reflections in amplitude amplification.</span></span>

```qsharp

newtype ReflectionPhases = (AboutStart : Double[], AboutTarget : Double[]);
```



## <a name="named-items"></a><span data-ttu-id="8629c-106">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="8629c-106">Named Items</span></span>

### <a name="aboutstart--double"></a><span data-ttu-id="8629c-107">AboutStart: [dubbele](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="8629c-107">AboutStart : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="8629c-108">Een matrix met fasen voor reflectie over de begin status.</span><span class="sxs-lookup"><span data-stu-id="8629c-108">An array of phases for reflection about the start state.</span></span>
### <a name="abouttarget--double"></a><span data-ttu-id="8629c-109">AboutTarget: [dubbele](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="8629c-109">AboutTarget : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="8629c-110">Een matrix met fasen voor reflectie over de doel status.</span><span class="sxs-lookup"><span data-stu-id="8629c-110">An array of phases for reflection about the target state.</span></span>

## <a name="remarks"></a><span data-ttu-id="8629c-111">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="8629c-111">Remarks</span></span>

<span data-ttu-id="8629c-112">Beide matrices moeten dezelfde lengte hebben.</span><span class="sxs-lookup"><span data-stu-id="8629c-112">Both arrays must be of equal length.</span></span> <span data-ttu-id="8629c-113">Houd er rekening mee dat in veel gevallen de eerste fase van de begin status en laatste fase over de doel status een globale fase verschuiving introduceert en kan worden ingesteld op $0 $.</span><span class="sxs-lookup"><span data-stu-id="8629c-113">Note that in many cases, the first phase about the start state and last phase about the target state introduces a global phase shift and may be set to $0$.</span></span>