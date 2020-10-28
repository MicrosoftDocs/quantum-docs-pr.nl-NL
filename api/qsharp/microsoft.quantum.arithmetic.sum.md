---
uid: Microsoft.Quantum.Arithmetic.Sum
title: Sum-bewerking
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: Sum
qsharp.summary: Implements a reversible sum gate. Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2`.
ms.openlocfilehash: b31d8ab39676ee6723e5fc053eba9e0af3ac2b2f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706197"
---
# <a name="sum-operation"></a><span data-ttu-id="5b0e0-102">Sum-bewerking</span><span class="sxs-lookup"><span data-stu-id="5b0e0-102">Sum operation</span></span>

<span data-ttu-id="5b0e0-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="5b0e0-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="5b0e0-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5b0e0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5b0e0-105">Implementeert een onomkeerbaare Sum-poort.</span><span class="sxs-lookup"><span data-stu-id="5b0e0-105">Implements a reversible sum gate.</span></span> <span data-ttu-id="5b0e0-106">Een door Voer in Qubit `carryIn` en twee summand bits `summand1` die zijn gecodeerd in en `summand2` , berekent de Bitsgewijze XOR van en `carryIn` `summand1` `summand2` in de Qubit `summand2` .</span><span class="sxs-lookup"><span data-stu-id="5b0e0-106">Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2`.</span></span>

```qsharp
operation Sum (carryIn : Qubit, summand1 : Qubit, summand2 : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="5b0e0-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="5b0e0-107">Input</span></span>

### <a name="carryin--qubit"></a><span data-ttu-id="5b0e0-108">carryIn: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="5b0e0-108">carryIn : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="5b0e0-109">Qubit uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="5b0e0-109">Carry-in qubit.</span></span>


### <a name="summand1--qubit"></a><span data-ttu-id="5b0e0-110">summand1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="5b0e0-110">summand1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="5b0e0-111">Eerste summand Qubit.</span><span class="sxs-lookup"><span data-stu-id="5b0e0-111">First summand qubit.</span></span>


### <a name="summand2--qubit"></a><span data-ttu-id="5b0e0-112">summand2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="5b0e0-112">summand2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="5b0e0-113">Tweede summand Qubit wordt vervangen door de laagste bit van de som van `summand1` en `summand2` .</span><span class="sxs-lookup"><span data-stu-id="5b0e0-113">Second summand qubit, is replaced with the lower bit of the sum of `summand1` and `summand2`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5b0e0-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5b0e0-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="5b0e0-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="5b0e0-115">Remarks</span></span>

<span data-ttu-id="5b0e0-116">In tegens telling tot de `Carry` bewerking, wordt de verwerkings bit niet berekend.</span><span class="sxs-lookup"><span data-stu-id="5b0e0-116">In contrast to the `Carry` operation, this does not compute the carry-out bit.</span></span>