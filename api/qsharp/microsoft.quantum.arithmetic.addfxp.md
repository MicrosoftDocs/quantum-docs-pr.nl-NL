---
uid: Microsoft.Quantum.Arithmetic.AddFxP
title: Bewerking AddFxP
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AddFxP
qsharp.summary: Adds two fixed-point numbers stored in quantum registers.
ms.openlocfilehash: 36a5d585a493f0e6f33f74b1686aaa01cca7ac0b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191037"
---
# <a name="addfxp-operation"></a><span data-ttu-id="a63dc-102">Bewerking AddFxP</span><span class="sxs-lookup"><span data-stu-id="a63dc-102">AddFxP operation</span></span>

<span data-ttu-id="a63dc-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="a63dc-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="a63dc-104">Pakket: [micro soft. Quantum. numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="a63dc-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="a63dc-105">Telt twee vaste-komma nummers op die zijn opgeslagen in Quantum registers.</span><span class="sxs-lookup"><span data-stu-id="a63dc-105">Adds two fixed-point numbers stored in quantum registers.</span></span>

```qsharp
operation AddFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="a63dc-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="a63dc-106">Description</span></span>

<span data-ttu-id="a63dc-107">In de Staten $ \ket{f_1} $ en $ \ket{f_2} $, voert de bewerking $ \ket{f_1} \ket{f_2} \mapsto \ket{f_1} \ket{f_1 + f_2} $ uit op twee vaste-punt registreren.</span><span class="sxs-lookup"><span data-stu-id="a63dc-107">Given two fixed-point registers respectively in states $\ket{f_1}$ and $\ket{f_2}$, performs the operation $\ket{f_1} \ket{f_2} \mapsto \ket{f_1} \ket{f_1 + f_2}$.</span></span>

## <a name="input"></a><span data-ttu-id="a63dc-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="a63dc-108">Input</span></span>

### <a name="fp1--fixedpoint"></a><span data-ttu-id="a63dc-109">FP1: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="a63dc-109">fp1 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="a63dc-110">Eerste getal met vaste komma</span><span class="sxs-lookup"><span data-stu-id="a63dc-110">First fixed-point number</span></span>


### <a name="fp2--fixedpoint"></a><span data-ttu-id="a63dc-111">FP2: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="a63dc-111">fp2 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="a63dc-112">Het tweede getal met vaste komma wordt bijgewerkt met de som van de twee invoer waarden.</span><span class="sxs-lookup"><span data-stu-id="a63dc-112">Second fixed-point number, will be updated to contain the sum of the two inputs.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a63dc-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a63dc-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="a63dc-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="a63dc-114">Remarks</span></span>

<span data-ttu-id="a63dc-115">De huidige implementatie vereist dat de twee vaste-komma waarden dezelfde punt positie hebben ten opzichte van de minst significante bit, d.w.z. $n _i $ en $p _i $ gelijk moet zijn.</span><span class="sxs-lookup"><span data-stu-id="a63dc-115">The current implementation requires the two fixed-point numbers to have the same point position counting from the least-significant bit, i.e., $n_i$ and $p_i$ must be equal.</span></span>