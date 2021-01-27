---
uid: Microsoft.Quantum.Arithmetic.IncrementPhaseByInteger
title: Bewerking IncrementPhaseByInteger
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementPhaseByInteger
qsharp.summary: Increments an unsigned quantum register by a classical integer, using phase rotations.
ms.openlocfilehash: cc7922b2940cb979394958d5eb4e9933144eb062
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843150"
---
# <a name="incrementphasebyinteger-operation"></a><span data-ttu-id="0b6db-102">Bewerking IncrementPhaseByInteger</span><span class="sxs-lookup"><span data-stu-id="0b6db-102">IncrementPhaseByInteger operation</span></span>

<span data-ttu-id="0b6db-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="0b6db-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="0b6db-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0b6db-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0b6db-105">Verhoogt een niet-ondertekend Quantum register met een klassiek geheel getal, met behulp van fase rotaties.</span><span class="sxs-lookup"><span data-stu-id="0b6db-105">Increments an unsigned quantum register by a classical integer, using phase rotations.</span></span>

```qsharp
operation IncrementPhaseByInteger (increment : Int, target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="0b6db-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="0b6db-106">Description</span></span>

<span data-ttu-id="0b6db-107">Stel dat `target` een niet-ondertekend geheel getal $x $ in een code ring van little-endian wordt gecodeerd en `increment` gelijk is aan $a $.</span><span class="sxs-lookup"><span data-stu-id="0b6db-107">Suppose that `target` encodes an unsigned integer $x$ in a little-endian encoding and that `increment` is equal to $a$.</span></span>
<span data-ttu-id="0b6db-108">Deze bewerking implementeert vervolgens de unitary $ \ket{x} \mapsto \ket{x + a} $, waarbij de aanvulling wordt uitgevoerd modulo $2 ^ n $, waarbij $n = \texttt{Length (doel!)} $.</span><span class="sxs-lookup"><span data-stu-id="0b6db-108">Then, this operation implements the unitary $\ket{x} \mapsto \ket{x + a}$, where the addition is performed modulo $2^n$, where $n = \texttt{Length(target!)}$.</span></span>

## <a name="input"></a><span data-ttu-id="0b6db-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="0b6db-109">Input</span></span>

### <a name="increment--int"></a><span data-ttu-id="0b6db-110">interval: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0b6db-110">increment : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0b6db-111">Het gehele getal waarmee de `target` wordt verhoogd.</span><span class="sxs-lookup"><span data-stu-id="0b6db-111">The integer by which the `target` is incremented by.</span></span>


### <a name="target--phaselittleendian"></a><span data-ttu-id="0b6db-112">doel: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="0b6db-112">target : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="0b6db-113">Een Quantum register codeert een niet-ondertekend geheel getal met behulp van code ring van Little Endian in de Dual (QFT) basis.</span><span class="sxs-lookup"><span data-stu-id="0b6db-113">A quantum register encoding an unsigned integer using little-endian encoding in the dual (QFT) basis.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0b6db-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0b6db-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="0b6db-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="0b6db-115">Remarks</span></span>

<span data-ttu-id="0b6db-116">Houd er rekening mee dat het circuit is vereenvoudigd omdat de verhoging een klassieke constante is, geen Quantum registratie.</span><span class="sxs-lookup"><span data-stu-id="0b6db-116">Note that we have simplified the circuit because the increment is a classical constant, not a quantum register.</span></span>

<span data-ttu-id="0b6db-117">Zie de afbeelding op [ pagina 6 van arXiv: Quant-pH/0008033v1 ](https://arxiv.org/pdf/quant-ph/0008033.pdf#page=6) voor het circuit diagram en de uitleg.</span><span class="sxs-lookup"><span data-stu-id="0b6db-117">See the figure on [ Page 6 of arXiv:quant-ph/0008033v1 ](https://arxiv.org/pdf/quant-ph/0008033.pdf#page=6) for the circuit diagram and explanation.</span></span>

## <a name="references"></a><span data-ttu-id="0b6db-118">Verwijzingen</span><span class="sxs-lookup"><span data-stu-id="0b6db-118">References</span></span>

- [<span data-ttu-id="0b6db-119">*Thomas G. Draper*, arXiv: Quant-pH/0008033</span><span class="sxs-lookup"><span data-stu-id="0b6db-119"> *Thomas G. Draper*, arXiv:quant-ph/0008033</span></span>](https://arxiv.org/pdf/quant-ph/0008033v1.pdf)

## <a name="see-also"></a><span data-ttu-id="0b6db-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="0b6db-120">See Also</span></span>

- [<span data-ttu-id="0b6db-121">Micro soft. Quantum. aritmetische. IncrementByInteger</span><span class="sxs-lookup"><span data-stu-id="0b6db-121">Microsoft.Quantum.Arithmetic.IncrementByInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.IncrementByInteger)