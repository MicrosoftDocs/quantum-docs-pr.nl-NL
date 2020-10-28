---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyConditionallyCA
title: Bewerking ApplyConditionallyCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyConditionallyCA
qsharp.summary: ''
ms.openlocfilehash: e456ed5d8f7f17a914401473948c89c020174903
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706645"
---
# <a name="applyconditionallyca-operation"></a><span data-ttu-id="6061a-102">Bewerking ApplyConditionallyCA</span><span class="sxs-lookup"><span data-stu-id="6061a-102">ApplyConditionallyCA operation</span></span>

<span data-ttu-id="6061a-103">Naam ruimte: [micro soft. Quantum. simulatie. QuantumProcessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="6061a-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="6061a-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6061a-104">Package: [](https://nuget.org/packages/)</span></span>




```qsharp
operation ApplyConditionallyCA<'T, 'U> (measurementResults : Result[], resultsValues : Result[], (onEqualOp : ('T => Unit is Ctl + Adj), equalArg : 'T), (onNonEqualOp : ('U => Unit is Ctl + Adj), nonEqualArg : 'U)) : Unit
```


## <a name="input"></a><span data-ttu-id="6061a-105">Invoer</span><span class="sxs-lookup"><span data-stu-id="6061a-105">Input</span></span>

### <a name="measurementresults--__invalidresult__"></a><span data-ttu-id="6061a-106">measurementResults: __ongeldige <Result>__ []</span><span class="sxs-lookup"><span data-stu-id="6061a-106">measurementResults : __invalid<Result>__ []</span></span>




### <a name="resultsvalues--__invalidresult__"></a><span data-ttu-id="6061a-107">resultsValues: __ongeldige <Result>__ []</span><span class="sxs-lookup"><span data-stu-id="6061a-107">resultsValues : __invalid<Result>__ []</span></span>




### <a name="onequalop--t--unit-ctl--adj"></a><span data-ttu-id="6061a-108">onEqualOp: 'T => CTL- [eenheid](xref:microsoft.quantum.lang-ref.unit) en correctie</span><span class="sxs-lookup"><span data-stu-id="6061a-108">onEqualOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>




### <a name="equalarg--t"></a><span data-ttu-id="6061a-109">equalArg: 'T</span><span class="sxs-lookup"><span data-stu-id="6061a-109">equalArg : 'T</span></span>




### <a name="onnonequalop--u--unit-ctl--adj"></a><span data-ttu-id="6061a-110">onNonEqualOp: ' U = CTL van>- [eenheid](xref:microsoft.quantum.lang-ref.unit) + correctie</span><span class="sxs-lookup"><span data-stu-id="6061a-110">onNonEqualOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>




### <a name="nonequalarg--u"></a><span data-ttu-id="6061a-111">nonEqualArg: ' U</span><span class="sxs-lookup"><span data-stu-id="6061a-111">nonEqualArg : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="6061a-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6061a-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="6061a-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="6061a-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6061a-114">T</span><span class="sxs-lookup"><span data-stu-id="6061a-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="6061a-115">' U</span><span class="sxs-lookup"><span data-stu-id="6061a-115">'U</span></span>

