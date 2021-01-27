---
uid: Microsoft.Quantum.Preparation.PrepareArbitraryState
title: Bewerking PrepareArbitraryState
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareArbitraryState
qsharp.summary: >-
  > [!WARNING]

  > PrepareArbitraryState has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateCP> instead.


  Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients.
ms.openlocfilehash: e2e4818e5d30b17dd1984c36da92d76b84403e1c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842388"
---
# <a name="preparearbitrarystate-operation"></a><span data-ttu-id="5d055-102">Bewerking PrepareArbitraryState</span><span class="sxs-lookup"><span data-stu-id="5d055-102">PrepareArbitraryState operation</span></span>

<span data-ttu-id="5d055-103">Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="5d055-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="5d055-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5d055-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="5d055-105">PrepareArbitraryState is afgeschaft.</span><span class="sxs-lookup"><span data-stu-id="5d055-105">PrepareArbitraryState has been deprecated.</span></span> <span data-ttu-id="5d055-106">Gebruik <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateCP> in plaats daarvan.</span><span class="sxs-lookup"><span data-stu-id="5d055-106">Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateCP> instead.</span></span>

<span data-ttu-id="5d055-107">Op basis van een set coëfficiënten en een versleuteld Quantum REGI ster van little endian, wordt een staat voor het REGI ster die wordt beschreven door de gegeven coëfficiënten voor bereid.</span><span class="sxs-lookup"><span data-stu-id="5d055-107">Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients.</span></span>

```qsharp
operation PrepareArbitraryState (coefficients : Microsoft.Quantum.Math.ComplexPolar[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="5d055-108">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="5d055-108">Description</span></span>

<span data-ttu-id="5d055-109">Met deze bewerking wordt een wille keurige Quantum status $ \ket{\psi} $ voor bereid met complexe coëfficiënten $r _j e ^ {i t_j} $ van de $n $-Qubit reken kundige status $ \ket{0 \cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="5d055-109">This operation prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0 \cdots 0}$.</span></span>
<span data-ttu-id="5d055-110">Met name de actie van deze bewerking kan worden gesimuleerd door de unitary-trans formatie $U $ die op de status alles-nullen werkt als</span><span class="sxs-lookup"><span data-stu-id="5d055-110">In particular, the action of this operation can be simulated by the a unitary transformation $U$ which acts on the all-zeros state as</span></span>

<span data-ttu-id="5d055-111">$ $ \begin{align} U\ket {0... 0} & = \ket{\psi} \\ \\ & = \frac{\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \ket{j}} {\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="5d055-111">$$ \begin{align} U\ket{0...0} & = \ket{\psi} \\\\ & = \frac{ \sum_{j=0}^{2^n-1} r_j e^{i t_j} \ket{j} }{ \sqrt{\sum_{j=0}^{2^n-1} |r_j|^2} }.</span></span>
<span data-ttu-id="5d055-112">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="5d055-112">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="5d055-113">Invoer</span><span class="sxs-lookup"><span data-stu-id="5d055-113">Input</span></span>

### <a name="coefficients--complexpolar"></a><span data-ttu-id="5d055-114">coëfficiënten: [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span><span class="sxs-lookup"><span data-stu-id="5d055-114">coefficients : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span></span>

<span data-ttu-id="5d055-115">Matrix van Maxi maal $2 ^ n $ complexe coëfficiënten die worden weer gegeven door hun absolute waarde en fase $ (r_j, t_j) $.</span><span class="sxs-lookup"><span data-stu-id="5d055-115">Array of up to $2^n$ complex coefficients represented by their absolute value and phase $(r_j, t_j)$.</span></span> <span data-ttu-id="5d055-116">De $j $ th indexeert de nummer status $ \ket{j} $ gecodeerd in de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="5d055-116">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="5d055-117">qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="5d055-117">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="5d055-118">Qubit registreert coderings nummer statussen in de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="5d055-118">Qubit register encoding number states in little-endian format.</span></span> <span data-ttu-id="5d055-119">Dit wordt verwacht te worden geïnitialiseerd in de status van de berekening $ \ket{0...0} $.</span><span class="sxs-lookup"><span data-stu-id="5d055-119">This is expected to be initialized in the computational basis state $\ket{0...0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5d055-120">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5d055-120">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="5d055-121">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="5d055-121">Remarks</span></span>

<span data-ttu-id="5d055-122">Negatieve invoer coëfficiënten $r _j < $0 worden beschouwd als positief met waarde $ | r_j | $.</span><span class="sxs-lookup"><span data-stu-id="5d055-122">Negative input coefficients $r_j < 0$ will be treated as though positive with value $|r_j|$.</span></span> <span data-ttu-id="5d055-123">`coefficients` wordt aangevuld met elementen $ (r_j, t_j) = (0,0, 0,0) $ als er minder dan $2 ^ n $ is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="5d055-123">`coefficients` will be padded with elements $(r_j, t_j) = (0.0, 0.0)$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="5d055-124">Verwijzingen</span><span class="sxs-lookup"><span data-stu-id="5d055-124">References</span></span>

- <span data-ttu-id="5d055-125">Synthese van Quantum Logic-circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="5d055-125">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="5d055-126">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5d055-126">See Also</span></span>

- [<span data-ttu-id="5d055-127">Micro soft. Quantum. prepare. ApproximatelyPrepareArbitraryState</span><span class="sxs-lookup"><span data-stu-id="5d055-127">Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState</span></span>](xref:Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState)