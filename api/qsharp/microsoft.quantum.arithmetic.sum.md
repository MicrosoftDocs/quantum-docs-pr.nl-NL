---
uid: Microsoft.Quantum.Arithmetic.Sum
title: Sum-bewerking
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: Sum
qsharp.summary: Implements a reversible sum gate. Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2`.
ms.openlocfilehash: 7758e29c9f08f4d05253defbe5a43a5316289522
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221790"
---
# <a name="sum-operation"></a><span data-ttu-id="95590-102">Sum-bewerking</span><span class="sxs-lookup"><span data-stu-id="95590-102">Sum operation</span></span>

<span data-ttu-id="95590-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="95590-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="95590-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="95590-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="95590-105">Implementeert een onomkeerbaare Sum-poort.</span><span class="sxs-lookup"><span data-stu-id="95590-105">Implements a reversible sum gate.</span></span> <span data-ttu-id="95590-106">Een door Voer in Qubit `carryIn` en twee summand bits `summand1` die zijn gecodeerd in en `summand2` , berekent de Bitsgewijze XOR van en `carryIn` `summand1` `summand2` in de Qubit `summand2` .</span><span class="sxs-lookup"><span data-stu-id="95590-106">Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2`.</span></span>

```qsharp
operation Sum (carryIn : Qubit, summand1 : Qubit, summand2 : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="95590-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="95590-107">Input</span></span>

### <a name="carryin--qubit"></a><span data-ttu-id="95590-108">carryIn: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="95590-108">carryIn : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="95590-109">Qubit uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="95590-109">Carry-in qubit.</span></span>


### <a name="summand1--qubit"></a><span data-ttu-id="95590-110">summand1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="95590-110">summand1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="95590-111">Eerste summand Qubit.</span><span class="sxs-lookup"><span data-stu-id="95590-111">First summand qubit.</span></span>


### <a name="summand2--qubit"></a><span data-ttu-id="95590-112">summand2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="95590-112">summand2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="95590-113">Tweede summand Qubit wordt vervangen door de laagste bit van de som van `summand1` en `summand2` .</span><span class="sxs-lookup"><span data-stu-id="95590-113">Second summand qubit, is replaced with the lower bit of the sum of `summand1` and `summand2`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="95590-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="95590-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="95590-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="95590-115">Remarks</span></span>

<span data-ttu-id="95590-116">In tegens telling tot de `Carry` bewerking, wordt de verwerkings bit niet berekend.</span><span class="sxs-lookup"><span data-stu-id="95590-116">In contrast to the `Carry` operation, this does not compute the carry-out bit.</span></span>