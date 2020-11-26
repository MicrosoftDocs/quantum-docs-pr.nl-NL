---
uid: Microsoft.Quantum.Arithmetic.CompareGreaterThanFxP
title: Bewerking CompareGreaterThanFxP
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGreaterThanFxP
qsharp.summary: Compares two fixed-point numbers stored in quantum registers, and controls a flip on the result.
ms.openlocfilehash: 1e9afc7645f62b932fa8ebc3d33e21a2a5182361
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223524"
---
# <a name="comparegreaterthanfxp-operation"></a><span data-ttu-id="dfef1-102">Bewerking CompareGreaterThanFxP</span><span class="sxs-lookup"><span data-stu-id="dfef1-102">CompareGreaterThanFxP operation</span></span>

<span data-ttu-id="dfef1-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="dfef1-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="dfef1-104">Pakket: [micro soft. Quantum. numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="dfef1-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="dfef1-105">Vergelijkt twee vaste-komma nummers die zijn opgeslagen in de Quantum registers en beheert een flip op het resultaat.</span><span class="sxs-lookup"><span data-stu-id="dfef1-105">Compares two fixed-point numbers stored in quantum registers, and controls a flip on the result.</span></span>

```qsharp
operation CompareGreaterThanFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint, result : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="dfef1-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="dfef1-106">Input</span></span>

### <a name="fp1--fixedpoint"></a><span data-ttu-id="dfef1-107">FP1: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="dfef1-107">fp1 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="dfef1-108">Eerste getal voor de vaste komma dat moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="dfef1-108">First fixed-point number to be compared.</span></span>


### <a name="fp2--fixedpoint"></a><span data-ttu-id="dfef1-109">FP2: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="dfef1-109">fp2 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="dfef1-110">Tweede getal met vaste komma dat moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="dfef1-110">Second fixed-point number to be compared.</span></span>


### <a name="result--qubit"></a><span data-ttu-id="dfef1-111">resultaat: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="dfef1-111">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="dfef1-112">Resultaat van de vergelijking.</span><span class="sxs-lookup"><span data-stu-id="dfef1-112">Result of the comparison.</span></span> <span data-ttu-id="dfef1-113">Wordt als weer spie gelen `fp1 > fp2` .</span><span class="sxs-lookup"><span data-stu-id="dfef1-113">Will be flipped if `fp1 > fp2`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="dfef1-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="dfef1-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="dfef1-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="dfef1-115">Remarks</span></span>

<span data-ttu-id="dfef1-116">De huidige implementatie vereist dat de twee vaste-komma nummers dezelfde punt positie en hetzelfde aantal qubits hebben.</span><span class="sxs-lookup"><span data-stu-id="dfef1-116">The current implementation requires the two fixed-point numbers to have the same point position and the same number of qubits.</span></span>