---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation
title: Bewerking ApplyPermutationUsingTransformation
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingTransformation
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using transformation-based synthesis.
ms.openlocfilehash: a05b433eae2612bbf5c87522c4ef251976184aa8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192057"
---
# <a name="applypermutationusingtransformation-operation"></a><span data-ttu-id="d3a5d-102">Bewerking ApplyPermutationUsingTransformation</span><span class="sxs-lookup"><span data-stu-id="d3a5d-102">ApplyPermutationUsingTransformation operation</span></span>

<span data-ttu-id="d3a5d-103">Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="d3a5d-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="d3a5d-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d3a5d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d3a5d-105">Permutaties de amplitudes in een Quantum status op basis van op trans formatie gebaseerde synthese.</span><span class="sxs-lookup"><span data-stu-id="d3a5d-105">Permutes the amplitudes in a quantum state given a permutation using transformation-based synthesis.</span></span>

```qsharp
operation ApplyPermutationUsingTransformation (perm : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="d3a5d-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="d3a5d-106">Description</span></span>

<span data-ttu-id="d3a5d-107">Met deze procedure implementeert u de methode voor het op één richting gebaseerde synthese van een trans formatie.</span><span class="sxs-lookup"><span data-stu-id="d3a5d-107">This procedure implements the unidirectional transformation based synthesis approach.</span></span>  <span data-ttu-id="d3a5d-108">De invoer is een permutatie $ \pi $ boven $2 ^ n $ Elements $ \{ 0, \dots, 2 ^ n-1 \} $, die een $n variabele met een onomkeerbaare Boole-functie vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="d3a5d-108">Input is a permutation $\pi$ over $2^n$ elements $\{0, \dots, 2^n-1\}$, which represents an $n$-variable reversible Boolean function.</span></span>
<span data-ttu-id="d3a5d-109">De algoritme voert iteratieve uitvoering van de volgende stappen uit:</span><span class="sxs-lookup"><span data-stu-id="d3a5d-109">The algorithm performs iteratively the following steps:</span></span>

1. <span data-ttu-id="d3a5d-110">Zoek de kleinste $x $ zodat $x \ne \pi (x) = y $.</span><span class="sxs-lookup"><span data-stu-id="d3a5d-110">Find smallest $x$ such that $x \ne \pi(x) = y$.</span></span>
2. <span data-ttu-id="d3a5d-111">Zoek met meerdere beheerde Toffoli-bewerkingen, die worden toegepast op de uitvoer, maken $ \pi (x) = x $ en wijzig $ \pi (x ') $ niet voor alle $x < x $</span><span class="sxs-lookup"><span data-stu-id="d3a5d-111">Find multiple-controlled Toffoli operations, which applied to the outputs make $\pi(x) = x$ and do not change $\pi(x')$ for all $x' < x$</span></span>

## <a name="input"></a><span data-ttu-id="d3a5d-112">Invoer</span><span class="sxs-lookup"><span data-stu-id="d3a5d-112">Input</span></span>

### <a name="perm--int"></a><span data-ttu-id="d3a5d-113">macht: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="d3a5d-113">perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="d3a5d-114">Een permutatie van $2 ^ n $ elementen vanaf 0.</span><span class="sxs-lookup"><span data-stu-id="d3a5d-114">A permutation of $2^n$ elements starting from 0.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="d3a5d-115">qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="d3a5d-115">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="d3a5d-116">Een lijst met $n $ qubits waarop de permutatie wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="d3a5d-116">A list of $n$ qubits to which the permutation is applied to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d3a5d-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d3a5d-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="d3a5d-118">Referenties</span><span class="sxs-lookup"><span data-stu-id="d3a5d-118">References</span></span>

- [<span data-ttu-id="d3a5d-119">*D. Michael Miller*, *Dmitri Maslov*, *Gerhard W. Dueck*, proc. DAC 2003, IEEE, pp. 318-323, 2003</span><span class="sxs-lookup"><span data-stu-id="d3a5d-119">*D. Michael Miller*, *Dmitri Maslov*, *Gerhard W. Dueck*, Proc. DAC 2003, IEEE, pp. 318-323, 2003</span></span>](https://doi.org/10.1145/775832.775915)
- [<span data-ttu-id="d3a5d-120">*Mathias soeken*, *Gerhard W. Dueck*, *D. Michael Miller*, proc. rc 2016, Springer, pp. 307-321, 2016</span><span class="sxs-lookup"><span data-stu-id="d3a5d-120">*Mathias Soeken*, *Gerhard W. Dueck*, *D. Michael Miller*, Proc. RC 2016, Springer, pp. 307-321, 2016</span></span>](https://doi.org/10.1007/978-3-319-40578-0_22)

## <a name="see-also"></a><span data-ttu-id="d3a5d-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d3a5d-121">See Also</span></span>

- [<span data-ttu-id="d3a5d-122">Micro soft. Quantum. synthese. ApplyPermutationUsingDecomposition</span><span class="sxs-lookup"><span data-stu-id="d3a5d-122">Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition)