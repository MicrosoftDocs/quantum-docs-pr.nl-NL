---
uid: Microsoft.Quantum.Arithmetic.IncrementPhaseByInteger
title: Bewerking IncrementPhaseByInteger
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementPhaseByInteger
qsharp.summary: Increments an unsigned quantum register by a classical integer, using phase rotations.
ms.openlocfilehash: fb67455dadbc7a2f38880581f0e413a747faa8ef
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707245"
---
# <a name="incrementphasebyinteger-operation"></a><span data-ttu-id="9821c-102">Bewerking IncrementPhaseByInteger</span><span class="sxs-lookup"><span data-stu-id="9821c-102">IncrementPhaseByInteger operation</span></span>

<span data-ttu-id="9821c-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="9821c-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="9821c-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9821c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9821c-105">Verhoogt een niet-ondertekend Quantum register met een klassiek geheel getal, met behulp van fase rotaties.</span><span class="sxs-lookup"><span data-stu-id="9821c-105">Increments an unsigned quantum register by a classical integer, using phase rotations.</span></span>

```qsharp
operation IncrementPhaseByInteger (increment : Int, target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="9821c-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="9821c-106">Description</span></span>

<span data-ttu-id="9821c-107">Stel dat `target` een niet-ondertekend geheel getal $x $ in een code ring van little-endian wordt gecodeerd en `increment` gelijk is aan $a $.</span><span class="sxs-lookup"><span data-stu-id="9821c-107">Suppose that `target` encodes an unsigned integer $x$ in a little-endian encoding and that `increment` is equal to $a$.</span></span>
<span data-ttu-id="9821c-108">Deze bewerking implementeert vervolgens de unitary $ \ket{x} \mapsto \ket{x + a} $, waarbij de aanvulling wordt uitgevoerd modulo $2 ^ n $, waarbij $n = \texttt{Length (doel!)} $.</span><span class="sxs-lookup"><span data-stu-id="9821c-108">Then, this operation implements the unitary $\ket{x} \mapsto \ket{x + a}$, where the addition is performed modulo $2^n$, where $n = \texttt{Length(target!)}$.</span></span>

## <a name="input"></a><span data-ttu-id="9821c-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="9821c-109">Input</span></span>

### <a name="increment--int"></a><span data-ttu-id="9821c-110">interval: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9821c-110">increment : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9821c-111">Het gehele getal waarmee de `target` wordt verhoogd.</span><span class="sxs-lookup"><span data-stu-id="9821c-111">The integer by which the `target` is incremented by.</span></span>


### <a name="target--phaselittleendian"></a><span data-ttu-id="9821c-112">doel: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="9821c-112">target : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="9821c-113">Een Quantum register codeert een niet-ondertekend geheel getal met behulp van code ring van Little Endian in de Dual (QFT) basis.</span><span class="sxs-lookup"><span data-stu-id="9821c-113">A quantum register encoding an unsigned integer using little-endian encoding in the dual (QFT) basis.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9821c-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9821c-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="9821c-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="9821c-115">Remarks</span></span>

<span data-ttu-id="9821c-116">Houd er rekening mee dat het circuit is vereenvoudigd omdat de verhoging een klassieke constante is, geen Quantum registratie.</span><span class="sxs-lookup"><span data-stu-id="9821c-116">Note that we have simplified the circuit because the increment is a classical constant, not a quantum register.</span></span>

<span data-ttu-id="9821c-117">Zie de afbeelding op [ pagina 6 van arXiv: Quant-pH/0008033v1 ](https://arxiv.org/pdf/quant-ph/0008033.pdf#page=6) voor het circuit diagram en de uitleg.</span><span class="sxs-lookup"><span data-stu-id="9821c-117">See the figure on [ Page 6 of arXiv:quant-ph/0008033v1 ](https://arxiv.org/pdf/quant-ph/0008033.pdf#page=6) for the circuit diagram and explanation.</span></span>

## <a name="references"></a><span data-ttu-id="9821c-118">Naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="9821c-118">References</span></span>

- [<span data-ttu-id="9821c-119">*Thomas G. Draper* , arXiv: Quant-pH/0008033</span><span class="sxs-lookup"><span data-stu-id="9821c-119"> *Thomas G. Draper* , arXiv:quant-ph/0008033</span></span>](https://arxiv.org/pdf/quant-ph/0008033v1.pdf)

## <a name="see-also"></a><span data-ttu-id="9821c-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9821c-120">See Also</span></span>

- [<span data-ttu-id="9821c-121">Micro soft. Quantum. aritmetische. IncrementByInteger</span><span class="sxs-lookup"><span data-stu-id="9821c-121">Microsoft.Quantum.Arithmetic.IncrementByInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.IncrementByInteger)