---
uid: Microsoft.Quantum.Intrinsic.RFrac
title: Bewerking RFrac
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: RFrac
qsharp.summary: >-
  Applies a rotation about the given Pauli axis by an angle specified as a dyadic fraction.

  \begin{align} R_{\mu}(n, k) \mathrel{:=} e^{i \pi n \sigma_{\mu} / 2^k}, \end{align} where $\mu \in \{I, X, Y, Z\}$.

  > [!WARNING] > This operation uses the **opposite** sign convention from > @"microsoft.quantum.intrinsic.r".
ms.openlocfilehash: 9fe6aee6c7bb9e52538eae5d2caa2a6025cb85d8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708442"
---
# <a name="rfrac-operation"></a><span data-ttu-id="46867-102">Bewerking RFrac</span><span class="sxs-lookup"><span data-stu-id="46867-102">RFrac operation</span></span>

<span data-ttu-id="46867-103">Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="46867-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="46867-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="46867-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="46867-105">Past een rotatie over de opgegeven Pauli-as toe met een hoek die is opgegeven als een dyadic Fractie.</span><span class="sxs-lookup"><span data-stu-id="46867-105">Applies a rotation about the given Pauli axis by an angle specified as a dyadic fraction.</span></span>

<span data-ttu-id="46867-106">\begin{align} R_ {\mu} (n, k) \mathrel{: =} e ^ {i \pi n \ sigma_ {\mu}/2 ^ k}, \end{align} waarbij $ \mu \in \{ i, X, Y, Z \} $.</span><span class="sxs-lookup"><span data-stu-id="46867-106">\begin{align} R_{\mu}(n, k) \mathrel{:=} e^{i \pi n \sigma_{\mu} / 2^k}, \end{align} where $\mu \in \{I, X, Y, Z\}$.</span></span>

> [!WARNING]
> <span data-ttu-id="46867-107">Deze bewerking maakt gebruik van de **tegenovergestelde** Onderteken Conventie van @"microsoft.quantum.intrinsic.r" .</span><span class="sxs-lookup"><span data-stu-id="46867-107">This operation uses the **opposite** sign convention from @"microsoft.quantum.intrinsic.r".</span></span>

```qsharp
operation RFrac (pauli : Pauli, numerator : Int, power : Int, qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="46867-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="46867-108">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="46867-109">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="46867-109">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="46867-110">Pauli-operator die moet worden exponentiated om de draaiing te vormen.</span><span class="sxs-lookup"><span data-stu-id="46867-110">Pauli operator to be exponentiated to form the rotation.</span></span>


### <a name="numerator--int"></a><span data-ttu-id="46867-111">teller: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="46867-111">numerator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="46867-112">De teller in de dyadic-weer gave van de hoek waarmee de Qubit moet worden gedraaid.</span><span class="sxs-lookup"><span data-stu-id="46867-112">Numerator in the dyadic fraction representation of the angle by which the qubit is to be rotated.</span></span>


### <a name="power--int"></a><span data-ttu-id="46867-113">energie: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="46867-113">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="46867-114">Kracht van twee opgeven van de noemer van de hoek waarmee de Qubit moet worden gedraaid.</span><span class="sxs-lookup"><span data-stu-id="46867-114">Power of two specifying the denominator of the angle by which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="46867-115">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="46867-115">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="46867-116">Qubit waarop de Gate moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="46867-116">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="46867-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="46867-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="46867-118">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="46867-118">Remarks</span></span>

<span data-ttu-id="46867-119">Gelijk aan:</span><span class="sxs-lookup"><span data-stu-id="46867-119">Equivalent to:</span></span>

```qsharp
// PI() is a Q# function that returns an approximation of π.
R(pauli, -PI() * IntAsDouble(numerator) / IntAsDouble(2 ^ (power - 1)), qubit);
```