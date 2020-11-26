---
uid: Microsoft.Quantum.Arithmetic.ComputeReciprocalFxP
title: Bewerking ComputeReciprocalFxP
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ComputeReciprocalFxP
qsharp.summary: Computes $1/x$ for a fixed-point number $x$.
ms.openlocfilehash: 3ca050d6ce9daaa10e14c2f12dd571398cf436b0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223388"
---
# <a name="computereciprocalfxp-operation"></a><span data-ttu-id="2bac9-102">Bewerking ComputeReciprocalFxP</span><span class="sxs-lookup"><span data-stu-id="2bac9-102">ComputeReciprocalFxP operation</span></span>

<span data-ttu-id="2bac9-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="2bac9-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="2bac9-104">Pakket: [micro soft. Quantum. numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="2bac9-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="2bac9-105">Berekent $1/x $ voor een getal met vaste komma $x $.</span><span class="sxs-lookup"><span data-stu-id="2bac9-105">Computes $1/x$ for a fixed-point number $x$.</span></span>

```qsharp
operation ComputeReciprocalFxP (x : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="2bac9-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="2bac9-106">Input</span></span>

### <a name="x--fixedpoint"></a><span data-ttu-id="2bac9-107">x: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="2bac9-107">x : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="2bac9-108">Nummer van vaste komma dat moet worden omgekeerd.</span><span class="sxs-lookup"><span data-stu-id="2bac9-108">Fixed-point number to be inverted.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="2bac9-109">resultaat: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="2bac9-109">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="2bac9-110">Getal met vaste komma dat het resultaat zal bevatten.</span><span class="sxs-lookup"><span data-stu-id="2bac9-110">Fixed-point number that will hold the result.</span></span> <span data-ttu-id="2bac9-111">Moet worden geïnitialiseerd op $ \ket{0.0} $.</span><span class="sxs-lookup"><span data-stu-id="2bac9-111">Must be initialized to $\ket{0.0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2bac9-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2bac9-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

