---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyConditionallyC
title: Bewerking ApplyConditionallyC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyConditionallyC
qsharp.summary: ''
ms.openlocfilehash: 963a85e0e442592c01a2e70fa0dc02d6048d8be7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229032"
---
# <a name="applyconditionallyc-operation"></a><span data-ttu-id="585f1-102">Bewerking ApplyConditionallyC</span><span class="sxs-lookup"><span data-stu-id="585f1-102">ApplyConditionallyC operation</span></span>

<span data-ttu-id="585f1-103">Naam ruimte: [micro soft. Quantum. simulatie. QuantumProcessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="585f1-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="585f1-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="585f1-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyConditionallyC<'T, 'U> (measurementResults : Result[], resultsValues : Result[], (onEqualOp : ('T => Unit is Ctl), equalArg : 'T), (onNonEqualOp : ('U => Unit is Ctl), nonEqualArg : 'U)) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="585f1-105">Invoer</span><span class="sxs-lookup"><span data-stu-id="585f1-105">Input</span></span>

### <a name="measurementresults--__invalidresult__"></a><span data-ttu-id="585f1-106">measurementResults: __ongeldige <Result>__[]</span><span class="sxs-lookup"><span data-stu-id="585f1-106">measurementResults : __invalid<Result>__[]</span></span>




### <a name="resultsvalues--__invalidresult__"></a><span data-ttu-id="585f1-107">resultsValues: __ongeldige <Result>__[]</span><span class="sxs-lookup"><span data-stu-id="585f1-107">resultsValues : __invalid<Result>__[]</span></span>




### <a name="onequalop--t--unit--is-ctl"></a><span data-ttu-id="585f1-108">onEqualOp: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="585f1-108">onEqualOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>




### <a name="equalarg--t"></a><span data-ttu-id="585f1-109">equalArg: 'T</span><span class="sxs-lookup"><span data-stu-id="585f1-109">equalArg : 'T</span></span>




### <a name="onnonequalop--u--unit--is-ctl"></a><span data-ttu-id="585f1-110">onNonEqualOp: ' U => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="585f1-110">onNonEqualOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>




### <a name="nonequalarg--u"></a><span data-ttu-id="585f1-111">nonEqualArg: ' U</span><span class="sxs-lookup"><span data-stu-id="585f1-111">nonEqualArg : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="585f1-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="585f1-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="585f1-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="585f1-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="585f1-114">T</span><span class="sxs-lookup"><span data-stu-id="585f1-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="585f1-115">' U</span><span class="sxs-lookup"><span data-stu-id="585f1-115">'U</span></span>

