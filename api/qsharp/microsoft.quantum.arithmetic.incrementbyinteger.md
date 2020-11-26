---
uid: Microsoft.Quantum.Arithmetic.IncrementByInteger
title: Bewerking IncrementByInteger
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementByInteger
qsharp.summary: Increments an unsigned quantum register by a classical integer, using phase rotations.
ms.openlocfilehash: fa5e75e91206aa5f33233c8a54d6e9e7ac2950e3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222963"
---
# <a name="incrementbyinteger-operation"></a><span data-ttu-id="70cdc-102">Bewerking IncrementByInteger</span><span class="sxs-lookup"><span data-stu-id="70cdc-102">IncrementByInteger operation</span></span>

<span data-ttu-id="70cdc-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="70cdc-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="70cdc-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="70cdc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="70cdc-105">Verhoogt een niet-ondertekend Quantum register met een klassiek geheel getal, met behulp van fase rotaties.</span><span class="sxs-lookup"><span data-stu-id="70cdc-105">Increments an unsigned quantum register by a classical integer, using phase rotations.</span></span>

```qsharp
operation IncrementByInteger (increment : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="70cdc-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="70cdc-106">Description</span></span>

<span data-ttu-id="70cdc-107">Stel dat `target` een niet-ondertekend geheel getal $x $ in een code ring van little-endian wordt gecodeerd en `increment` gelijk is aan $a $.</span><span class="sxs-lookup"><span data-stu-id="70cdc-107">Suppose that `target` encodes an unsigned integer $x$ in a little-endian encoding and that `increment` is equal to $a$.</span></span>
<span data-ttu-id="70cdc-108">Deze bewerking implementeert vervolgens de unitary $ \ket{x} \mapsto \ket{x + a} $, waarbij de aanvulling wordt uitgevoerd modulo $2 ^ n $, waarbij $n = \texttt{Length (doel!)} $.</span><span class="sxs-lookup"><span data-stu-id="70cdc-108">Then, this operation implements the unitary $\ket{x} \mapsto \ket{x + a}$, where the addition is performed modulo $2^n$, where $n = \texttt{Length(target!)}$.</span></span>

## <a name="input"></a><span data-ttu-id="70cdc-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="70cdc-109">Input</span></span>

### <a name="increment--int"></a><span data-ttu-id="70cdc-110">interval: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="70cdc-110">increment : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="70cdc-111">Het gehele getal waarmee de `target` wordt verhoogd.</span><span class="sxs-lookup"><span data-stu-id="70cdc-111">The integer by which the `target` is incremented by.</span></span>


### <a name="target--littleendian"></a><span data-ttu-id="70cdc-112">doel: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="70cdc-112">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="70cdc-113">Een Quantum register codeert een niet-ondertekend geheel getal door gebruik te maken van code ring van little-endian.</span><span class="sxs-lookup"><span data-stu-id="70cdc-113">A quantum register encoding an unsigned integer using little-endian encoding.</span></span>



## <a name="output--unit"></a><span data-ttu-id="70cdc-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="70cdc-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

