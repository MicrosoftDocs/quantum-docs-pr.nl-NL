---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfElseRC
title: Bewerking ApplyIfElseRC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfElseRC
qsharp.summary: ''
ms.openlocfilehash: 97536f2071918bec7129d8157e8750a5c310767f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855636"
---
# <a name="applyifelserc-operation"></a><span data-ttu-id="64f60-102">Bewerking ApplyIfElseRC</span><span class="sxs-lookup"><span data-stu-id="64f60-102">ApplyIfElseRC operation</span></span>

<span data-ttu-id="64f60-103">Naam ruimte: [micro soft. Quantum. simulatie. QuantumProcessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="64f60-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="64f60-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="64f60-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyIfElseRC<'T, 'U> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Ctl), zeroArg : 'T), (onResultOneOp : ('U => Unit is Ctl), oneArg : 'U)) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="64f60-105">Invoer</span><span class="sxs-lookup"><span data-stu-id="64f60-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="64f60-106">measurementResult: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="64f60-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit--is-ctl"></a><span data-ttu-id="64f60-107">onResultZeroOp: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="64f60-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>




### <a name="zeroarg--t"></a><span data-ttu-id="64f60-108">zeroArg: 'T</span><span class="sxs-lookup"><span data-stu-id="64f60-108">zeroArg : 'T</span></span>




### <a name="onresultoneop--u--unit--is-ctl"></a><span data-ttu-id="64f60-109">onResultOneOp: ' U => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="64f60-109">onResultOneOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>




### <a name="onearg--u"></a><span data-ttu-id="64f60-110">oneArg: ' U</span><span class="sxs-lookup"><span data-stu-id="64f60-110">oneArg : 'U</span></span>





## <a name="output--unit"></a><span data-ttu-id="64f60-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="64f60-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="64f60-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="64f60-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="64f60-113">T</span><span class="sxs-lookup"><span data-stu-id="64f60-113">'T</span></span>


### <a name="u"></a><span data-ttu-id="64f60-114">' U</span><span class="sxs-lookup"><span data-stu-id="64f60-114">'U</span></span>

