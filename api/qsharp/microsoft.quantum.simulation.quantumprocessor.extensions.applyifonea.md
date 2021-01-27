---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfOneA
title: Bewerking ApplyIfOneA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfOneA
qsharp.summary: ''
ms.openlocfilehash: 63ce44300f6e50cb91294b62611275e3e8942655
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855615"
---
# <a name="applyifonea-operation"></a><span data-ttu-id="9ed56-102">Bewerking ApplyIfOneA</span><span class="sxs-lookup"><span data-stu-id="9ed56-102">ApplyIfOneA operation</span></span>

<span data-ttu-id="9ed56-103">Naam ruimte: [micro soft. Quantum. simulatie. QuantumProcessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="9ed56-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="9ed56-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="9ed56-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyIfOneA<'T> (measurementResult : Result, (onResultOneOp : ('T => Unit is Adj), oneArg : 'T)) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="9ed56-105">Invoer</span><span class="sxs-lookup"><span data-stu-id="9ed56-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="9ed56-106">measurementResult: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="9ed56-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultoneop--t--unit--is-adj"></a><span data-ttu-id="9ed56-107">onResultOneOp: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="9ed56-107">onResultOneOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>




### <a name="onearg--t"></a><span data-ttu-id="9ed56-108">oneArg: 'T</span><span class="sxs-lookup"><span data-stu-id="9ed56-108">oneArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="9ed56-109">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9ed56-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="9ed56-110">Type parameters</span><span class="sxs-lookup"><span data-stu-id="9ed56-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9ed56-111">T</span><span class="sxs-lookup"><span data-stu-id="9ed56-111">'T</span></span>

