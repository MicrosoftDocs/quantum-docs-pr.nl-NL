---
uid: Microsoft.Quantum.Arithmetic.MultiplyFxP
title: Bewerking MultiplyFxP
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyFxP
qsharp.summary: Multiplies two fixed-point numbers in quantum registers.
ms.openlocfilehash: 3c9ef9ade660e1f420d85162104d773b96722eeb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222606"
---
# <a name="multiplyfxp-operation"></a><span data-ttu-id="5b5ba-102">Bewerking MultiplyFxP</span><span class="sxs-lookup"><span data-stu-id="5b5ba-102">MultiplyFxP operation</span></span>

<span data-ttu-id="5b5ba-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="5b5ba-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="5b5ba-104">Pakket: [micro soft. Quantum. numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="5b5ba-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="5b5ba-105">Vermenigvuldigt twee vaste-komma getallen in Quantum registers.</span><span class="sxs-lookup"><span data-stu-id="5b5ba-105">Multiplies two fixed-point numbers in quantum registers.</span></span>

```qsharp
operation MultiplyFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="5b5ba-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="5b5ba-106">Input</span></span>

### <a name="fp1--fixedpoint"></a><span data-ttu-id="5b5ba-107">FP1: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="5b5ba-107">fp1 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="5b5ba-108">Eerste getal met vaste komma.</span><span class="sxs-lookup"><span data-stu-id="5b5ba-108">First fixed-point number.</span></span>


### <a name="fp2--fixedpoint"></a><span data-ttu-id="5b5ba-109">FP2: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="5b5ba-109">fp2 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="5b5ba-110">Tweede getal met vaste komma.</span><span class="sxs-lookup"><span data-stu-id="5b5ba-110">Second fixed-point number.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="5b5ba-111">resultaat: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="5b5ba-111">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="5b5ba-112">Het resultaat van een vast punt moet de status $ \ket {0} $ in eerste instantie hebben.</span><span class="sxs-lookup"><span data-stu-id="5b5ba-112">Result fixed-point number, must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5b5ba-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5b5ba-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="5b5ba-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="5b5ba-114">Remarks</span></span>

<span data-ttu-id="5b5ba-115">Voor de huidige implementatie moeten de drie vaste-komma waarden dezelfde punt positie en hetzelfde aantal qubits hebben.</span><span class="sxs-lookup"><span data-stu-id="5b5ba-115">The current implementation requires the three fixed-point numbers to have the same point position and the same number of qubits.</span></span>