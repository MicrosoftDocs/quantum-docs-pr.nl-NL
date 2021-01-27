---
uid: Microsoft.Quantum.Preparation.PrepareArbitraryStateCP
title: Bewerking PrepareArbitraryStateCP
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareArbitraryStateCP
qsharp.summary: Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients.
ms.openlocfilehash: 1e293057f8b549dc57817cdce350e50e2b91682a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856911"
---
# <a name="preparearbitrarystatecp-operation"></a><span data-ttu-id="575c5-102">Bewerking PrepareArbitraryStateCP</span><span class="sxs-lookup"><span data-stu-id="575c5-102">PrepareArbitraryStateCP operation</span></span>

<span data-ttu-id="575c5-103">Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="575c5-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="575c5-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="575c5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="575c5-105">Op basis van een set coëfficiënten en een versleuteld Quantum REGI ster van little endian, wordt een staat voor het REGI ster die wordt beschreven door de gegeven coëfficiënten voor bereid.</span><span class="sxs-lookup"><span data-stu-id="575c5-105">Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients.</span></span>

```qsharp
operation PrepareArbitraryStateCP (coefficients : Microsoft.Quantum.Math.ComplexPolar[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="575c5-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="575c5-106">Description</span></span>

<span data-ttu-id="575c5-107">Met deze bewerking wordt een wille keurige Quantum status $ \ket{\psi} $ voor bereid met complexe coëfficiënten $r _j e ^ {i t_j} $ van de $n $-Qubit reken kundige status $ \ket{0 \cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="575c5-107">This operation prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0 \cdots 0}$.</span></span>
<span data-ttu-id="575c5-108">Met name de actie van deze bewerking kan worden gesimuleerd door de unitary-trans formatie $U $ die op de status alles-nullen werkt als</span><span class="sxs-lookup"><span data-stu-id="575c5-108">In particular, the action of this operation can be simulated by the a unitary transformation $U$ which acts on the all-zeros state as</span></span>

<span data-ttu-id="575c5-109">$ $ \begin{align} U\ket {0... 0} & = \ket{\psi} \\ \\ & = \frac{\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \ket{j}} {\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="575c5-109">$$ \begin{align} U\ket{0...0} & = \ket{\psi} \\\\ & = \frac{ \sum_{j=0}^{2^n-1} r_j e^{i t_j} \ket{j} }{ \sqrt{\sum_{j=0}^{2^n-1} |r_j|^2} }.</span></span>
<span data-ttu-id="575c5-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="575c5-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="575c5-111">Invoer</span><span class="sxs-lookup"><span data-stu-id="575c5-111">Input</span></span>

### <a name="coefficients--complexpolar"></a><span data-ttu-id="575c5-112">coëfficiënten: [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span><span class="sxs-lookup"><span data-stu-id="575c5-112">coefficients : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span></span>

<span data-ttu-id="575c5-113">Matrix van Maxi maal $2 ^ n $ complexe coëfficiënten die worden weer gegeven door hun absolute waarde en fase $ (r_j, t_j) $.</span><span class="sxs-lookup"><span data-stu-id="575c5-113">Array of up to $2^n$ complex coefficients represented by their absolute value and phase $(r_j, t_j)$.</span></span> <span data-ttu-id="575c5-114">De $j $ th indexeert de nummer status $ \ket{j} $ gecodeerd in de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="575c5-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="575c5-115">qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="575c5-115">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="575c5-116">Qubit registreert coderings nummer statussen in de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="575c5-116">Qubit register encoding number states in little-endian format.</span></span> <span data-ttu-id="575c5-117">Dit wordt verwacht te worden geïnitialiseerd in de status van de berekening $ \ket{0...0} $.</span><span class="sxs-lookup"><span data-stu-id="575c5-117">This is expected to be initialized in the computational basis state $\ket{0...0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="575c5-118">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="575c5-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="575c5-119">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="575c5-119">Remarks</span></span>

<span data-ttu-id="575c5-120">Negatieve invoer coëfficiënten $r _j < $0 worden beschouwd als positief met waarde $ | r_j | $.</span><span class="sxs-lookup"><span data-stu-id="575c5-120">Negative input coefficients $r_j < 0$ will be treated as though positive with value $|r_j|$.</span></span> <span data-ttu-id="575c5-121">`coefficients` wordt aangevuld met elementen $ (r_j, t_j) = (0,0, 0,0) $ als er minder dan $2 ^ n $ is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="575c5-121">`coefficients` will be padded with elements $(r_j, t_j) = (0.0, 0.0)$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="575c5-122">Verwijzingen</span><span class="sxs-lookup"><span data-stu-id="575c5-122">References</span></span>

- <span data-ttu-id="575c5-123">Synthese van Quantum Logic-circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="575c5-123">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="575c5-124">Zie ook</span><span class="sxs-lookup"><span data-stu-id="575c5-124">See Also</span></span>

- [<span data-ttu-id="575c5-125">Micro soft. Quantum. prepare. ApproximatelyPrepareArbitraryState</span><span class="sxs-lookup"><span data-stu-id="575c5-125">Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState</span></span>](xref:Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState)