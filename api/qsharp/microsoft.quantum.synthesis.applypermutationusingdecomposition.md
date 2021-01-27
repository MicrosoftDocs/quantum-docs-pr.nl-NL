---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition
title: Bewerking ApplyPermutationUsingDecomposition
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingDecomposition
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.
ms.openlocfilehash: 765b6d301363021f5b57a22f90e2ada38c9c09ec
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857397"
---
# <a name="applypermutationusingdecomposition-operation"></a><span data-ttu-id="887f2-102">Bewerking ApplyPermutationUsingDecomposition</span><span class="sxs-lookup"><span data-stu-id="887f2-102">ApplyPermutationUsingDecomposition operation</span></span>

<span data-ttu-id="887f2-103">Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="887f2-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="887f2-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="887f2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="887f2-105">Permutaties de amplitudes in een Quantum status op basis van een permutatie met behulp van op ontleding gebaseerde synthese.</span><span class="sxs-lookup"><span data-stu-id="887f2-105">Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.</span></span>

```qsharp
operation ApplyPermutationUsingDecomposition (perm : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="887f2-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="887f2-106">Description</span></span>

<span data-ttu-id="887f2-107">Met deze procedure wordt de methode voor het samen stellen op basis van een synthese geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="887f2-107">This procedure implements the decomposition based synthesis approach.</span></span>  <span data-ttu-id="887f2-108">De invoer is een permutatie $ \pi $ boven $2 ^ n $ Elements $ \{ 0, \dots, 2 ^ n-1 \} $, waarmee een $n variabele van $-variable omkeerbaar Booleaanse waarde wordt aangeduid.</span><span class="sxs-lookup"><span data-stu-id="887f2-108">The input is a permutation $\pi$ over $2^n$ elements $\{0, \dots, 2^n-1\}$, which represents an $n$-variable reversible Boolean function.</span></span>
<span data-ttu-id="887f2-109">Het algoritme voert iteraties de volgende stappen uit voor elke variabele index $i $:</span><span class="sxs-lookup"><span data-stu-id="887f2-109">The algorithm iteratively performs the following steps for each variable index $i$:</span></span>

1. <span data-ttu-id="887f2-110">Compute $ ((\ pi_l, \ pi_r), \pi ') $ zo is dat de installatie kopieën van $ \ pi_l $ en $ \ pi_r $ geen bits in hun eigen elementen wijzigen op andere indexen dan $i $ en installatie kopieën van $ \pi $ in hun eigen elementen.</span><span class="sxs-lookup"><span data-stu-id="887f2-110">Compute $((\pi_l, \pi_r), \pi')$ such that the images of $\pi_l$ and $\pi_r$ do not change bits in their elements at indexes other than $i$ and images of $\pi'$ do not change bit $i$ in their elements.</span></span>
2. <span data-ttu-id="887f2-111">Stel $ \pi \leftarrow \pi $ in en pas waarheids tabellen af van $ \ pi_l $ en $ \ pi_r $ op basis van elementen die geen vaste punten zijn.</span><span class="sxs-lookup"><span data-stu-id="887f2-111">Set $\pi \leftarrow \pi'$, and derive truth tables from $\pi_l$ and $\pi_r$ based on elements that are not fixed-points.</span></span>

<span data-ttu-id="887f2-112">Nadat u deze stappen voor alle variabelen indexen hebt toegepast, is de resterende permutatie $ \pi $ de identiteit en op basis van de verzamelde waarheids tabellen en-indexen, een @"microsoft.quantum.intrinsic.x" met behulp van de @"microsoft.quantum.synthesis.applyxcontrolledontruthtable" bewerking.</span><span class="sxs-lookup"><span data-stu-id="887f2-112">After applying these steps for all variable indexes, the remaining permutation $\pi$ will be the identity, and based on the collected truth tables and indexes, one can apply truth-table controlled @"microsoft.quantum.intrinsic.x" operations using the @"microsoft.quantum.synthesis.applyxcontrolledontruthtable" operation.</span></span>

<span data-ttu-id="887f2-113">De variabele bestelling is $0, \dots, n-$1.</span><span class="sxs-lookup"><span data-stu-id="887f2-113">The variable order is $0, \dots, n - 1$.</span></span>  <span data-ttu-id="887f2-114">U kunt een aangepaste variabele volgorde opgeven in de bewerking @"microsoft.quantum.synthesis.applypermutationusingdecompositionwithvariableorder" .</span><span class="sxs-lookup"><span data-stu-id="887f2-114">A custom variable order can be specified in the operation @"microsoft.quantum.synthesis.applypermutationusingdecompositionwithvariableorder".</span></span>

## <a name="input"></a><span data-ttu-id="887f2-115">Invoer</span><span class="sxs-lookup"><span data-stu-id="887f2-115">Input</span></span>

### <a name="perm--int"></a><span data-ttu-id="887f2-116">macht: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="887f2-116">perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="887f2-117">Een permutatie van $2 ^ n $ elementen vanaf 0.</span><span class="sxs-lookup"><span data-stu-id="887f2-117">A permutation of $2^n$ elements starting from 0.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="887f2-118">qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="887f2-118">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="887f2-119">Een lijst met $n $ qubits waarop de permutatie wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="887f2-119">A list of $n$ qubits to which the permutation is applied to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="887f2-120">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="887f2-120">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="887f2-121">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="887f2-121">Example</span></span>

<span data-ttu-id="887f2-122">Een `SWAP` bewerking verwerken:</span><span class="sxs-lookup"><span data-stu-id="887f2-122">To synthesize a `SWAP` operation:</span></span>

```qsharp
using (qubits = Qubit[2]) {
  ApplyPermutationUsingDecomposition([0, 2, 1, 3], LittleEndian(qubits));
}
```

## <a name="references"></a><span data-ttu-id="887f2-123">Verwijzingen</span><span class="sxs-lookup"><span data-stu-id="887f2-123">References</span></span>

- [<span data-ttu-id="887f2-124">*Alexis de Vos*, *Yvan van Rentergem*, adv. in math. van comm. 2 (2), 2008, pp. 183--200</span><span class="sxs-lookup"><span data-stu-id="887f2-124">*Alexis De Vos*, *Yvan Van Rentergem*, Adv. in Math. of Comm. 2(2), 2008, pp. 183--200</span></span>](http://www.aimsciences.org/article/doi/10.3934/amc.2008.2.183)
- [<span data-ttu-id="887f2-125">*Mathias soeken*, *Laura Tague*, *Gerhard W. Dueck*, *Rolf Drechsler*, Journal of symbolische berekening 73 (2016), pp. 1--26</span><span class="sxs-lookup"><span data-stu-id="887f2-125">*Mathias Soeken*, *Laura Tague*, *Gerhard W. Dueck*, *Rolf Drechsler*, Journal of Symbolic Computation 73 (2016), pp. 1--26</span></span>](https://www.sciencedirect.com/science/article/pii/S0747717115000188?via%3Dihub)

## <a name="see-also"></a><span data-ttu-id="887f2-126">Zie ook</span><span class="sxs-lookup"><span data-stu-id="887f2-126">See Also</span></span>

- [<span data-ttu-id="887f2-127">Micro soft. Quantum. synthese. ApplyPermutationUsingDecompositionWithVariableOrder</span><span class="sxs-lookup"><span data-stu-id="887f2-127">Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecompositionWithVariableOrder</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecompositionWithVariableOrder)
- [<span data-ttu-id="887f2-128">Micro soft. Quantum. synthese. ApplyPermutationUsingTransformation</span><span class="sxs-lookup"><span data-stu-id="887f2-128">Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation)