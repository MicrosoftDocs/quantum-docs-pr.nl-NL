---
uid: Microsoft.Quantum.Simulation.ApplyBlockEncodingByLCU
title: Bewerking ApplyBlockEncodingByLCU
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: ApplyBlockEncodingByLCU
qsharp.summary: Implementation of `BlockEncodingByLCU`.
ms.openlocfilehash: a9a9e3bbd598453719f49f78392f3a92c9401b36
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852813"
---
# <a name="applyblockencodingbylcu-operation"></a><span data-ttu-id="93d20-102">Bewerking ApplyBlockEncodingByLCU</span><span class="sxs-lookup"><span data-stu-id="93d20-102">ApplyBlockEncodingByLCU operation</span></span>

<span data-ttu-id="93d20-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="93d20-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="93d20-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="93d20-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="93d20-105">Implementatie van `BlockEncodingByLCU` .</span><span class="sxs-lookup"><span data-stu-id="93d20-105">Implementation of `BlockEncodingByLCU`.</span></span>

```qsharp
operation ApplyBlockEncodingByLCU<'T, 'S> (statePreparation : ('T => Unit is Adj + Ctl), selector : (('T, 'S) => Unit is Adj + Ctl), auxiliary : 'T, system : 'S) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="93d20-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="93d20-106">Input</span></span>

### <a name="statepreparation--t--unit--is-adj--ctl"></a><span data-ttu-id="93d20-107">statePreparation: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="93d20-107">statePreparation : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="selector--ts--unit--is-adj--ctl"></a><span data-ttu-id="93d20-108">kiezer: ('T) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="93d20-108">selector : ('T,'S) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="auxiliary--t"></a><span data-ttu-id="93d20-109">hulp: 'T</span><span class="sxs-lookup"><span data-stu-id="93d20-109">auxiliary : 'T</span></span>




### <a name="system--s"></a><span data-ttu-id="93d20-110">systeem:</span><span class="sxs-lookup"><span data-stu-id="93d20-110">system : 'S</span></span>





## <a name="output--unit"></a><span data-ttu-id="93d20-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="93d20-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="93d20-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="93d20-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="93d20-113">T</span><span class="sxs-lookup"><span data-stu-id="93d20-113">'T</span></span>


### <a name="s"></a><span data-ttu-id="93d20-114">Maatschappij</span><span class="sxs-lookup"><span data-stu-id="93d20-114">'S</span></span>

