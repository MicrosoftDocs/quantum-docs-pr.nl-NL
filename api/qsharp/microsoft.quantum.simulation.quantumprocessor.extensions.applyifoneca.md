---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfOneCA
title: Bewerking ApplyIfOneCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfOneCA
qsharp.summary: ''
ms.openlocfilehash: 8dd2d501d4598b1de69daa87f7a0941262b7d435
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858909"
---
# <a name="applyifoneca-operation"></a><span data-ttu-id="4778d-102">Bewerking ApplyIfOneCA</span><span class="sxs-lookup"><span data-stu-id="4778d-102">ApplyIfOneCA operation</span></span>

<span data-ttu-id="4778d-103">Naam ruimte: [micro soft. Quantum. simulatie. QuantumProcessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="4778d-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="4778d-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="4778d-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyIfOneCA<'T> (measurementResult : Result, (onResultOneOp : ('T => Unit is Ctl + Adj), oneArg : 'T)) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="4778d-105">Invoer</span><span class="sxs-lookup"><span data-stu-id="4778d-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="4778d-106">measurementResult: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="4778d-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultoneop--t--unit--is-adj--ctl"></a><span data-ttu-id="4778d-107">onResultOneOp: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="4778d-107">onResultOneOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>




### <a name="onearg--t"></a><span data-ttu-id="4778d-108">oneArg: 'T</span><span class="sxs-lookup"><span data-stu-id="4778d-108">oneArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="4778d-109">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4778d-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="4778d-110">Type parameters</span><span class="sxs-lookup"><span data-stu-id="4778d-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4778d-111">T</span><span class="sxs-lookup"><span data-stu-id="4778d-111">'T</span></span>

