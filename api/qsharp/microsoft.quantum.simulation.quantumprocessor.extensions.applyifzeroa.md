---
uid: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions.ApplyIfZeroA
title: Bewerking ApplyIfZeroA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation.QuantumProcessor.Extensions
qsharp.name: ApplyIfZeroA
qsharp.summary: ''
ms.openlocfilehash: 812b7a830d963b4bb73c32ba1c136e506789e997
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854206"
---
# <a name="applyifzeroa-operation"></a><span data-ttu-id="f6900-102">Bewerking ApplyIfZeroA</span><span class="sxs-lookup"><span data-stu-id="f6900-102">ApplyIfZeroA operation</span></span>

<span data-ttu-id="f6900-103">Naam ruimte: [micro soft. Quantum. simulatie. QuantumProcessor. Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span><span class="sxs-lookup"><span data-stu-id="f6900-103">Namespace: [Microsoft.Quantum.Simulation.QuantumProcessor.Extensions](xref:Microsoft.Quantum.Simulation.QuantumProcessor.Extensions)</span></span>

<span data-ttu-id="f6900-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="f6900-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>




```qsharp
operation ApplyIfZeroA<'T> (measurementResult : Result, (onResultZeroOp : ('T => Unit is Adj), zeroArg : 'T)) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="f6900-105">Invoer</span><span class="sxs-lookup"><span data-stu-id="f6900-105">Input</span></span>

### <a name="measurementresult--__invalidresult__"></a><span data-ttu-id="f6900-106">measurementResult: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="f6900-106">measurementResult : __invalid<Result>__</span></span>




### <a name="onresultzeroop--t--unit--is-adj"></a><span data-ttu-id="f6900-107">onResultZeroOp: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="f6900-107">onResultZeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>




### <a name="zeroarg--t"></a><span data-ttu-id="f6900-108">zeroArg: 'T</span><span class="sxs-lookup"><span data-stu-id="f6900-108">zeroArg : 'T</span></span>





## <a name="output--unit"></a><span data-ttu-id="f6900-109">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f6900-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f6900-110">Type parameters</span><span class="sxs-lookup"><span data-stu-id="f6900-110">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f6900-111">T</span><span class="sxs-lookup"><span data-stu-id="f6900-111">'T</span></span>

