---
uid: Microsoft.Quantum.Simulation.ApplyBlockEncodingByLCU
title: Bewerking ApplyBlockEncodingByLCU
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: ApplyBlockEncodingByLCU
qsharp.summary: Implementation of `BlockEncodingByLCU`.
ms.openlocfilehash: 1575b93b6c3242e1dffafb330c44cc017a72a8b1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707848"
---
# <a name="applyblockencodingbylcu-operation"></a><span data-ttu-id="05230-102">Bewerking ApplyBlockEncodingByLCU</span><span class="sxs-lookup"><span data-stu-id="05230-102">ApplyBlockEncodingByLCU operation</span></span>

<span data-ttu-id="05230-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="05230-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="05230-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="05230-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="05230-105">Implementatie van `BlockEncodingByLCU` .</span><span class="sxs-lookup"><span data-stu-id="05230-105">Implementation of `BlockEncodingByLCU`.</span></span>

```qsharp
operation ApplyBlockEncodingByLCU<'T, 'S> (statePreparation : ('T => Unit is Adj + Ctl), selector : (('T, 'S) => Unit is Adj + Ctl), auxiliary : 'T, system : 'S) : Unit
```


## <a name="input"></a><span data-ttu-id="05230-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="05230-106">Input</span></span>

### <a name="statepreparation--t--unit-adj--ctl"></a><span data-ttu-id="05230-107">statePreparation: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="05230-107">statePreparation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>




### <a name="selector--ts--unit-adj--ctl"></a><span data-ttu-id="05230-108">kiezer: ('T) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="05230-108">selector : ('T,'S) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>




### <a name="auxiliary--t"></a><span data-ttu-id="05230-109">hulp: 'T</span><span class="sxs-lookup"><span data-stu-id="05230-109">auxiliary : 'T</span></span>




### <a name="system--s"></a><span data-ttu-id="05230-110">systeem:</span><span class="sxs-lookup"><span data-stu-id="05230-110">system : 'S</span></span>





## <a name="output--unit"></a><span data-ttu-id="05230-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="05230-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="05230-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="05230-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="05230-113">T</span><span class="sxs-lookup"><span data-stu-id="05230-113">'T</span></span>


### <a name="s"></a><span data-ttu-id="05230-114">Maatschappij</span><span class="sxs-lookup"><span data-stu-id="05230-114">'S</span></span>

