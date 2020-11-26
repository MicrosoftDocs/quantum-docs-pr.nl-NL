---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyConditionallyIntrinsicCA
title: Bewerking ApplyConditionallyIntrinsicCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyConditionallyIntrinsicCA
qsharp.summary: ''
ms.openlocfilehash: 2dd7a9b6e281c62470defa64685dc58872694468
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230188"
---
# <a name="applyconditionallyintrinsicca-operation"></a><span data-ttu-id="c61b5-102">Bewerking ApplyConditionallyIntrinsicCA</span><span class="sxs-lookup"><span data-stu-id="c61b5-102">ApplyConditionallyIntrinsicCA operation</span></span>

<span data-ttu-id="c61b5-103">Naam ruimte: [micro soft. Quantum. simulatie. QuantumProcessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="c61b5-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="c61b5-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="c61b5-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyConditionallyIntrinsicCA (measurementResults : Result[], resultsValues : Result[], onEqualOp : (Unit => Unit is Ctl + Adj), onNonEqualOp : (Unit => Unit is Ctl + Adj)) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="c61b5-105">Invoer</span><span class="sxs-lookup"><span data-stu-id="c61b5-105">Input</span></span>

### <a name="measurementresults--__invalidresult__"></a><span data-ttu-id="c61b5-106">measurementResults: __ongeldige <Result>__[]</span><span class="sxs-lookup"><span data-stu-id="c61b5-106">measurementResults : __invalid<Result>__[]</span></span>




### <a name="resultsvalues--__invalidresult__"></a><span data-ttu-id="c61b5-107">resultsValues: __ongeldige <Result>__[]</span><span class="sxs-lookup"><span data-stu-id="c61b5-107">resultsValues : __invalid<Result>__[]</span></span>




### <a name="onequalop--unit--unit--is-adj--ctl"></a><span data-ttu-id="c61b5-108">onEqualOp: [eenheids](xref:microsoft.quantum.lang-ref.unit) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="c61b5-108">onEqualOp : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="onnonequalop--unit--unit--is-adj--ctl"></a><span data-ttu-id="c61b5-109">onNonEqualOp: [eenheids](xref:microsoft.quantum.lang-ref.unit) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="c61b5-109">onNonEqualOp : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>





## <a name="output--unit"></a><span data-ttu-id="c61b5-110">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c61b5-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

