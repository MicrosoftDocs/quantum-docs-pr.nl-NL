---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfZero
title: Bewerking ApplyIfZero
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfZero
qsharp.summary: ''
ms.openlocfilehash: f0c8cfc2292cf30ee3ab86c486e982347086453b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858281"
---
# <a name="applyifzero-operation"></a><span data-ttu-id="3d431-102">Bewerking ApplyIfZero</span><span class="sxs-lookup"><span data-stu-id="3d431-102">ApplyIfZero operation</span></span>

<span data-ttu-id="3d431-103">Naam ruimte: [micro soft. Quantum. simulatie. QuantumProcessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="3d431-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="3d431-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="3d431-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyIfZero<'T> (measurementResult : Result, (onResultZeroOp : ('T => Unit), zeroArg : 'T)) : Unit
```


## <a name="input"></a><span data-ttu-id="3d431-105">Invoer</span><span class="sxs-lookup"><span data-stu-id="3d431-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="3d431-106">measurementResult: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="3d431-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit"></a><span data-ttu-id="3d431-107">onResultZeroOp: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3d431-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 




### <a name="zeroarg--t"></a><span data-ttu-id="3d431-108">zeroArg: 'T</span><span class="sxs-lookup"><span data-stu-id="3d431-108">zeroArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="3d431-109">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3d431-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="3d431-110">Type parameters</span><span class="sxs-lookup"><span data-stu-id="3d431-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3d431-111">T</span><span class="sxs-lookup"><span data-stu-id="3d431-111">'T</span></span>

