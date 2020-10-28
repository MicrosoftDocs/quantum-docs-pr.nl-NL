---
uid: Microsoft.Quantum.Arithmetic.MultiplyFxP
title: Bewerking MultiplyFxP
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyFxP
qsharp.summary: Multiplies two fixed-point numbers in quantum registers.
ms.openlocfilehash: 18883f3f4c3793b91e248f4bd89f9def640bf254
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706381"
---
# <a name="multiplyfxp-operation"></a><span data-ttu-id="34503-102">Bewerking MultiplyFxP</span><span class="sxs-lookup"><span data-stu-id="34503-102">MultiplyFxP operation</span></span>

<span data-ttu-id="34503-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="34503-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="34503-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="34503-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="34503-105">Vermenigvuldigt twee vaste-komma getallen in Quantum registers.</span><span class="sxs-lookup"><span data-stu-id="34503-105">Multiplies two fixed-point numbers in quantum registers.</span></span>

```qsharp
operation MultiplyFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit
```


## <a name="input"></a><span data-ttu-id="34503-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="34503-106">Input</span></span>

### <a name="fp1--fixedpoint"></a><span data-ttu-id="34503-107">FP1: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="34503-107">fp1 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="34503-108">Eerste getal met vaste komma.</span><span class="sxs-lookup"><span data-stu-id="34503-108">First fixed-point number.</span></span>


### <a name="fp2--fixedpoint"></a><span data-ttu-id="34503-109">FP2: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="34503-109">fp2 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="34503-110">Tweede getal met vaste komma.</span><span class="sxs-lookup"><span data-stu-id="34503-110">Second fixed-point number.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="34503-111">resultaat: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="34503-111">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="34503-112">Het resultaat van een vast punt moet de status $ \ket {0} $ in eerste instantie hebben.</span><span class="sxs-lookup"><span data-stu-id="34503-112">Result fixed-point number, must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="34503-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="34503-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="34503-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="34503-114">Remarks</span></span>

<span data-ttu-id="34503-115">Voor de huidige implementatie moeten de drie vaste-komma waarden dezelfde punt positie en hetzelfde aantal qubits hebben.</span><span class="sxs-lookup"><span data-stu-id="34503-115">The current implementation requires the three fixed-point numbers to have the same point position and the same number of qubits.</span></span>