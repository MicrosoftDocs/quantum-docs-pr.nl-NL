---
uid: Microsoft.Quantum.Simulation.ApplyBlockEncodingByLCU
title: Bewerking ApplyBlockEncodingByLCU
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: ApplyBlockEncodingByLCU
qsharp.summary: Implementation of `BlockEncodingByLCU`.
ms.openlocfilehash: 8ce6eb16b1dc5a83dd3a9559592c20d6b7b999b6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225479"
---
# <a name="applyblockencodingbylcu-operation"></a><span data-ttu-id="d62d6-102">Bewerking ApplyBlockEncodingByLCU</span><span class="sxs-lookup"><span data-stu-id="d62d6-102">ApplyBlockEncodingByLCU operation</span></span>

<span data-ttu-id="d62d6-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="d62d6-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="d62d6-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d62d6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d62d6-105">Implementatie van `BlockEncodingByLCU` .</span><span class="sxs-lookup"><span data-stu-id="d62d6-105">Implementation of `BlockEncodingByLCU`.</span></span>

```qsharp
operation ApplyBlockEncodingByLCU<'T, 'S> (statePreparation : ('T => Unit is Adj + Ctl), selector : (('T, 'S) => Unit is Adj + Ctl), auxiliary : 'T, system : 'S) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="d62d6-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="d62d6-106">Input</span></span>

### <a name="statepreparation--t--unit--is-adj--ctl"></a><span data-ttu-id="d62d6-107">statePreparation: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="d62d6-107">statePreparation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="selector--ts--unit--is-adj--ctl"></a><span data-ttu-id="d62d6-108">kiezer: ('T) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="d62d6-108">selector : ('T,'S) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="auxiliary--t"></a><span data-ttu-id="d62d6-109">hulp: 'T</span><span class="sxs-lookup"><span data-stu-id="d62d6-109">auxiliary : 'T</span></span>




### <a name="system--s"></a><span data-ttu-id="d62d6-110">systeem:</span><span class="sxs-lookup"><span data-stu-id="d62d6-110">system : 'S</span></span>





## <a name="output--unit"></a><span data-ttu-id="d62d6-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d62d6-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d62d6-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="d62d6-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d62d6-113">T</span><span class="sxs-lookup"><span data-stu-id="d62d6-113">'T</span></span>


### <a name="s"></a><span data-ttu-id="d62d6-114">Maatschappij</span><span class="sxs-lookup"><span data-stu-id="d62d6-114">'S</span></span>

