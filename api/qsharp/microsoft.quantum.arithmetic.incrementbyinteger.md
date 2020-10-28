---
uid: Microsoft.Quantum.Arithmetic.IncrementByInteger
title: Bewerking IncrementByInteger
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementByInteger
qsharp.summary: Increments an unsigned quantum register by a classical integer, using phase rotations.
ms.openlocfilehash: 363d48d697e3b2dad4d4896e6b1e701864649d9b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707269"
---
# <a name="incrementbyinteger-operation"></a><span data-ttu-id="a0b14-102">Bewerking IncrementByInteger</span><span class="sxs-lookup"><span data-stu-id="a0b14-102">IncrementByInteger operation</span></span>

<span data-ttu-id="a0b14-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="a0b14-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="a0b14-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a0b14-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a0b14-105">Verhoogt een niet-ondertekend Quantum register met een klassiek geheel getal, met behulp van fase rotaties.</span><span class="sxs-lookup"><span data-stu-id="a0b14-105">Increments an unsigned quantum register by a classical integer, using phase rotations.</span></span>

```qsharp
operation IncrementByInteger (increment : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="a0b14-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="a0b14-106">Description</span></span>

<span data-ttu-id="a0b14-107">Stel dat `target` een niet-ondertekend geheel getal $x $ in een code ring van little-endian wordt gecodeerd en `increment` gelijk is aan $a $.</span><span class="sxs-lookup"><span data-stu-id="a0b14-107">Suppose that `target` encodes an unsigned integer $x$ in a little-endian encoding and that `increment` is equal to $a$.</span></span>
<span data-ttu-id="a0b14-108">Deze bewerking implementeert vervolgens de unitary $ \ket{x} \mapsto \ket{x + a} $, waarbij de aanvulling wordt uitgevoerd modulo $2 ^ n $, waarbij $n = \texttt{Length (doel!)} $.</span><span class="sxs-lookup"><span data-stu-id="a0b14-108">Then, this operation implements the unitary $\ket{x} \mapsto \ket{x + a}$, where the addition is performed modulo $2^n$, where $n = \texttt{Length(target!)}$.</span></span>

## <a name="input"></a><span data-ttu-id="a0b14-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="a0b14-109">Input</span></span>

### <a name="increment--int"></a><span data-ttu-id="a0b14-110">interval: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a0b14-110">increment : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a0b14-111">Het gehele getal waarmee de `target` wordt verhoogd.</span><span class="sxs-lookup"><span data-stu-id="a0b14-111">The integer by which the `target` is incremented by.</span></span>


### <a name="target--littleendian"></a><span data-ttu-id="a0b14-112">doel: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="a0b14-112">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="a0b14-113">Een Quantum register codeert een niet-ondertekend geheel getal door gebruik te maken van code ring van little-endian.</span><span class="sxs-lookup"><span data-stu-id="a0b14-113">A quantum register encoding an unsigned integer using little-endian encoding.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a0b14-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a0b14-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

