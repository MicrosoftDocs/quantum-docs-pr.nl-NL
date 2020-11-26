---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfOne
title: Bewerking ApplyIfOne
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfOne
qsharp.summary: ''
ms.openlocfilehash: f8f4f3b05d3986d94e6f1be380d6c83151d87f17
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230664"
---
# <a name="applyifone-operation"></a><span data-ttu-id="984ac-102">Bewerking ApplyIfOne</span><span class="sxs-lookup"><span data-stu-id="984ac-102">ApplyIfOne operation</span></span>

<span data-ttu-id="984ac-103">Naam ruimte: [micro soft. Quantum. simulatie. QuantumProcessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="984ac-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="984ac-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="984ac-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyIfOne<'T> (measurementResult : Result, (onResultOneOp : ('T => Unit), oneArg : 'T)) : Unit
```


## <a name="input"></a><span data-ttu-id="984ac-105">Invoer</span><span class="sxs-lookup"><span data-stu-id="984ac-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="984ac-106">measurementResult: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="984ac-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultoneop--t--unit"></a><span data-ttu-id="984ac-107">onResultOneOp: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="984ac-107">onResultOneOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 




### <a name="onearg--t"></a><span data-ttu-id="984ac-108">oneArg: 'T</span><span class="sxs-lookup"><span data-stu-id="984ac-108">oneArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="984ac-109">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="984ac-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="984ac-110">Type parameters</span><span class="sxs-lookup"><span data-stu-id="984ac-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="984ac-111">T</span><span class="sxs-lookup"><span data-stu-id="984ac-111">'T</span></span>

