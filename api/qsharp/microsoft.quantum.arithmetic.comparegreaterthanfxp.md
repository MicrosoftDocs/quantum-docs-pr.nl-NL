---
uid: Microsoft.Quantum.Arithmetic.CompareGreaterThanFxP
title: Bewerking CompareGreaterThanFxP
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGreaterThanFxP
qsharp.summary: Compares two fixed-point numbers stored in quantum registers, and controls a flip on the result.
ms.openlocfilehash: f49c713c8a1e8a6451f2c54fa59a72f00bfbb4c4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843326"
---
# <a name="comparegreaterthanfxp-operation"></a><span data-ttu-id="82e6c-102">Bewerking CompareGreaterThanFxP</span><span class="sxs-lookup"><span data-stu-id="82e6c-102">CompareGreaterThanFxP operation</span></span>

<span data-ttu-id="82e6c-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="82e6c-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="82e6c-104">Pakket: [micro soft. Quantum. numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="82e6c-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="82e6c-105">Vergelijkt twee vaste-komma nummers die zijn opgeslagen in de Quantum registers en beheert een flip op het resultaat.</span><span class="sxs-lookup"><span data-stu-id="82e6c-105">Compares two fixed-point numbers stored in quantum registers, and controls a flip on the result.</span></span>

```qsharp
operation CompareGreaterThanFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint, result : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="82e6c-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="82e6c-106">Input</span></span>

### <a name="fp1--fixedpoint"></a><span data-ttu-id="82e6c-107">FP1: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="82e6c-107">fp1 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="82e6c-108">Eerste getal voor de vaste komma dat moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="82e6c-108">First fixed-point number to be compared.</span></span>


### <a name="fp2--fixedpoint"></a><span data-ttu-id="82e6c-109">FP2: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="82e6c-109">fp2 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="82e6c-110">Tweede getal met vaste komma dat moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="82e6c-110">Second fixed-point number to be compared.</span></span>


### <a name="result--qubit"></a><span data-ttu-id="82e6c-111">resultaat: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="82e6c-111">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="82e6c-112">Resultaat van de vergelijking.</span><span class="sxs-lookup"><span data-stu-id="82e6c-112">Result of the comparison.</span></span> <span data-ttu-id="82e6c-113">Wordt als weer spie gelen `fp1 > fp2` .</span><span class="sxs-lookup"><span data-stu-id="82e6c-113">Will be flipped if `fp1 > fp2`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="82e6c-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="82e6c-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="82e6c-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="82e6c-115">Remarks</span></span>

<span data-ttu-id="82e6c-116">De huidige implementatie vereist dat de twee vaste-komma nummers dezelfde punt positie en hetzelfde aantal qubits hebben.</span><span class="sxs-lookup"><span data-stu-id="82e6c-116">The current implementation requires the two fixed-point numbers to have the same point position and the same number of qubits.</span></span>