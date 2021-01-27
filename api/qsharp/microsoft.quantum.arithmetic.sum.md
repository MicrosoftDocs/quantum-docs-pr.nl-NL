---
uid: Microsoft.Quantum.Arithmetic.Sum
title: Sum-bewerking
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: Sum
qsharp.summary: Implements a reversible sum gate. Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2`.
ms.openlocfilehash: e659c77a876e10df75f28ca1798fb0335e1bfb22
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847759"
---
# <a name="sum-operation"></a><span data-ttu-id="8f6a2-102">Sum-bewerking</span><span class="sxs-lookup"><span data-stu-id="8f6a2-102">Sum operation</span></span>

<span data-ttu-id="8f6a2-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="8f6a2-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="8f6a2-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8f6a2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8f6a2-105">Implementeert een onomkeerbaare Sum-poort.</span><span class="sxs-lookup"><span data-stu-id="8f6a2-105">Implements a reversible sum gate.</span></span> <span data-ttu-id="8f6a2-106">Een door Voer in Qubit `carryIn` en twee summand bits `summand1` die zijn gecodeerd in en `summand2` , berekent de Bitsgewijze XOR van en `carryIn` `summand1` `summand2` in de Qubit `summand2` .</span><span class="sxs-lookup"><span data-stu-id="8f6a2-106">Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2`.</span></span>

```qsharp
operation Sum (carryIn : Qubit, summand1 : Qubit, summand2 : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="8f6a2-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="8f6a2-107">Input</span></span>

### <a name="carryin--qubit"></a><span data-ttu-id="8f6a2-108">carryIn: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="8f6a2-108">carryIn : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="8f6a2-109">Qubit uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="8f6a2-109">Carry-in qubit.</span></span>


### <a name="summand1--qubit"></a><span data-ttu-id="8f6a2-110">summand1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="8f6a2-110">summand1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="8f6a2-111">Eerste summand Qubit.</span><span class="sxs-lookup"><span data-stu-id="8f6a2-111">First summand qubit.</span></span>


### <a name="summand2--qubit"></a><span data-ttu-id="8f6a2-112">summand2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="8f6a2-112">summand2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="8f6a2-113">Tweede summand Qubit wordt vervangen door de laagste bit van de som van `summand1` en `summand2` .</span><span class="sxs-lookup"><span data-stu-id="8f6a2-113">Second summand qubit, is replaced with the lower bit of the sum of `summand1` and `summand2`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8f6a2-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8f6a2-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="8f6a2-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="8f6a2-115">Remarks</span></span>

<span data-ttu-id="8f6a2-116">In tegens telling tot de `Carry` bewerking, wordt de verwerkings bit niet berekend.</span><span class="sxs-lookup"><span data-stu-id="8f6a2-116">In contrast to the `Carry` operation, this does not compute the carry-out bit.</span></span>