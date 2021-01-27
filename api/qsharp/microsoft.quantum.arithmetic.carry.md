---
uid: Microsoft.Quantum.Arithmetic.Carry
title: Bewerking uitvoeren
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: Carry
qsharp.summary: Implements a reversible carry gate. Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2` and the carry-out is xored to the qubit `carryOut`.
ms.openlocfilehash: dfb08a9a9c805c0b611ab993c9b1eb949810a7da
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843358"
---
# <a name="carry-operation"></a><span data-ttu-id="95df5-102">Bewerking uitvoeren</span><span class="sxs-lookup"><span data-stu-id="95df5-102">Carry operation</span></span>

<span data-ttu-id="95df5-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="95df5-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="95df5-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="95df5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="95df5-105">Implementeert een geomkeerbaare transport poort.</span><span class="sxs-lookup"><span data-stu-id="95df5-105">Implements a reversible carry gate.</span></span> <span data-ttu-id="95df5-106">Een door Voer in Qubit `carryIn` en twee summand bits die zijn gecodeerd in `summand1` en `summand2` , berekent de Bitsgewijze XOR van en `carryIn` `summand1` `summand2` in de Qubit en de uitwerkings wijze `summand2` xored naar de Qubit `carryOut` .</span><span class="sxs-lookup"><span data-stu-id="95df5-106">Given a carry-in bit encoded in qubit `carryIn` and two summand bits encoded in `summand1` and `summand2`, computes the bitwise xor of `carryIn`, `summand1` and `summand2` in the qubit `summand2` and the carry-out is xored to the qubit `carryOut`.</span></span>

```qsharp
operation Carry (carryIn : Qubit, summand1 : Qubit, summand2 : Qubit, carryOut : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="95df5-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="95df5-107">Input</span></span>

### <a name="carryin--qubit"></a><span data-ttu-id="95df5-108">carryIn: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="95df5-108">carryIn : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="95df5-109">Qubit uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="95df5-109">Carry-in qubit.</span></span>


### <a name="summand1--qubit"></a><span data-ttu-id="95df5-110">summand1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="95df5-110">summand1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="95df5-111">Eerste summand Qubit.</span><span class="sxs-lookup"><span data-stu-id="95df5-111">First summand qubit.</span></span>


### <a name="summand2--qubit"></a><span data-ttu-id="95df5-112">summand2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="95df5-112">summand2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="95df5-113">Tweede summand Qubit wordt vervangen door de laagste bit van de som van `summand1` en `summand2` .</span><span class="sxs-lookup"><span data-stu-id="95df5-113">Second summand qubit, is replaced with the lower bit of the sum of `summand1` and `summand2`.</span></span>


### <a name="carryout--qubit"></a><span data-ttu-id="95df5-114">carryOut: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="95df5-114">carryOut : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="95df5-115">De Qubit wordt xored met de hogere bit van de som.</span><span class="sxs-lookup"><span data-stu-id="95df5-115">Carry-out qubit, will be xored with the higher bit of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="95df5-116">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="95df5-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

