---
uid: Microsoft.Quantum.Intrinsic.R1Frac
title: Bewerking R1Frac
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: R1Frac
qsharp.summary: >-
  Applies a rotation about the $\ket{1}$ state by an angle specified as a dyadic fraction.

  \begin{align} R_1(n, k) \mathrel{:=} \operatorname{diag}(1, e^{i \pi k / 2^n}). \end{align}

  > [!WARNING] > This operation uses the **opposite** sign convention from > @"microsoft.quantum.intrinsic.r", and does not include the > factor of $1/ 2$ included by @"microsoft.quantum.intrinsic.r1".
ms.openlocfilehash: bfa6cd60eebd05feec8cfa2bf71e09dc0d02843a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707132"
---
# <a name="r1frac-operation"></a><span data-ttu-id="2e470-102">Bewerking R1Frac</span><span class="sxs-lookup"><span data-stu-id="2e470-102">R1Frac operation</span></span>

<span data-ttu-id="2e470-103">Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="2e470-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="2e470-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2e470-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2e470-105">Past een rotatie over de $ \ket {1} $-status toe met een hoek die is opgegeven als een dyadic-Fractie.</span><span class="sxs-lookup"><span data-stu-id="2e470-105">Applies a rotation about the $\ket{1}$ state by an angle specified as a dyadic fraction.</span></span>

<span data-ttu-id="2e470-106">\begin{align} R_1 (n, k) \mathrel{: =} \operatorname{diag} (1, e ^ {i \pi k/2 ^ n}).</span><span class="sxs-lookup"><span data-stu-id="2e470-106">\begin{align} R_1(n, k) \mathrel{:=} \operatorname{diag}(1, e^{i \pi k / 2^n}).</span></span>
<span data-ttu-id="2e470-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="2e470-107">\end{align}</span></span>

> [!WARNING]
> <span data-ttu-id="2e470-108">Deze bewerking maakt gebruik van de **tegenovergestelde** teken Conventie van en bevat @"microsoft.quantum.intrinsic.r" niet de factor $1/2 $, opgenomen door @"microsoft.quantum.intrinsic.r1" .</span><span class="sxs-lookup"><span data-stu-id="2e470-108">This operation uses the **opposite** sign convention from @"microsoft.quantum.intrinsic.r", and does not include the factor of $1/ 2$ included by @"microsoft.quantum.intrinsic.r1".</span></span>

```qsharp
operation R1Frac (numerator : Int, power : Int, qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="2e470-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="2e470-109">Input</span></span>

### <a name="numerator--int"></a><span data-ttu-id="2e470-110">teller: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2e470-110">numerator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2e470-111">De teller in de dyadic-weer gave van de hoek waarmee de Qubit moet worden gedraaid.</span><span class="sxs-lookup"><span data-stu-id="2e470-111">Numerator in the dyadic fraction representation of the angle by which the qubit is to be rotated.</span></span>


### <a name="power--int"></a><span data-ttu-id="2e470-112">energie: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2e470-112">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2e470-113">Kracht van twee opgeven van de noemer van de hoek waarmee de Qubit moet worden gedraaid.</span><span class="sxs-lookup"><span data-stu-id="2e470-113">Power of two specifying the denominator of the angle by which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="2e470-114">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="2e470-114">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="2e470-115">Qubit waarop de Gate moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="2e470-115">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2e470-116">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2e470-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="2e470-117">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="2e470-117">Remarks</span></span>

<span data-ttu-id="2e470-118">Gelijk aan:</span><span class="sxs-lookup"><span data-stu-id="2e470-118">Equivalent to:</span></span>

```qsharp
RFrac(PauliZ, -numerator, denominator + 1, qubit);
RFrac(PauliI, numerator, denominator + 1, qubit);
```