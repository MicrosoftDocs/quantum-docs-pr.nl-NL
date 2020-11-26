---
uid: Microsoft.Quantum.Preparation.PrepareArbitraryStateD
title: Bewerking PrepareArbitraryStateD
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareArbitraryStateD
qsharp.summary: Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients.
ms.openlocfilehash: cca0ea16dca3f3da8ce76a43f1012ffa0e4a72e0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210604"
---
# <a name="preparearbitrarystated-operation"></a><span data-ttu-id="a4045-102">Bewerking PrepareArbitraryStateD</span><span class="sxs-lookup"><span data-stu-id="a4045-102">PrepareArbitraryStateD operation</span></span>

<span data-ttu-id="a4045-103">Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="a4045-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="a4045-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a4045-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a4045-105">Op basis van een set coëfficiënten en een versleuteld Quantum REGI ster van little endian, wordt een staat voor het REGI ster die wordt beschreven door de gegeven coëfficiënten voor bereid.</span><span class="sxs-lookup"><span data-stu-id="a4045-105">Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients.</span></span>

```qsharp
operation PrepareArbitraryStateD (coefficients : Double[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="a4045-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="a4045-106">Description</span></span>

<span data-ttu-id="a4045-107">Met deze bewerking wordt een wille keurige Quantum status $ \ket{\psi} $ voor bereid met complexe coëfficiënten $r _j e ^ {i t_j} $ van de $n $-Qubit reken kundige status $ \ket{0 \cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="a4045-107">This operation prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0 \cdots 0}$.</span></span>
<span data-ttu-id="a4045-108">Met name de actie van deze bewerking kan worden gesimuleerd door de unitary-trans formatie $U $ die op de status alles-nul reageert als</span><span class="sxs-lookup"><span data-stu-id="a4045-108">In particular, the action of this operation can be simulated by the a unitary transformation $U$ that acts on the all-zeros state as</span></span>

<span data-ttu-id="a4045-109">$ $ \begin{align} U\ket {0... 0} & = \ket{\psi} \\ \\ & = \frac{\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \ket{j}} {\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="a4045-109">$$ \begin{align} U\ket{0...0} & = \ket{\psi} \\\\ & = \frac{ \sum_{j=0}^{2^n-1} r_j e^{i t_j} \ket{j} }{ \sqrt{\sum_{j=0}^{2^n-1} |r_j|^2} }.</span></span>
<span data-ttu-id="a4045-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="a4045-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="a4045-111">Invoer</span><span class="sxs-lookup"><span data-stu-id="a4045-111">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="a4045-112">coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="a4045-112">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="a4045-113">Matrix van Maxi maal $2 ^ n $ reële coëfficiënten.</span><span class="sxs-lookup"><span data-stu-id="a4045-113">Array of up to $2^n$ real coefficients.</span></span> <span data-ttu-id="a4045-114">De $j $ th indexeert de nummer status $ \ket{j} $ gecodeerd in de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="a4045-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="a4045-115">qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="a4045-115">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="a4045-116">Qubit registreert coderings nummer statussen in de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="a4045-116">Qubit register encoding number states in little-endian format.</span></span> <span data-ttu-id="a4045-117">Dit wordt verwacht te worden geïnitialiseerd in de status van de berekening $ \ket{0...0} $.</span><span class="sxs-lookup"><span data-stu-id="a4045-117">This is expected to be initialized in the computational basis state $\ket{0...0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a4045-118">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a4045-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="a4045-119">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="a4045-119">Remarks</span></span>

<span data-ttu-id="a4045-120">Negatieve invoer coëfficiënten $r _j < $0 worden beschouwd als positief met waarde $ | r_j | $.</span><span class="sxs-lookup"><span data-stu-id="a4045-120">Negative input coefficients $r_j < 0$ will be treated as though positive with value $|r_j|$.</span></span> <span data-ttu-id="a4045-121">`coefficients` wordt aangevuld met elementen $ (r_j, t_j) = (0,0, 0,0) $ als er minder dan $2 ^ n $ is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="a4045-121">`coefficients` will be padded with elements $(r_j, t_j) = (0.0, 0.0)$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="a4045-122">Referenties</span><span class="sxs-lookup"><span data-stu-id="a4045-122">References</span></span>

- <span data-ttu-id="a4045-123">Synthese van Quantum Logic-circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="a4045-123">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="a4045-124">Zie ook</span><span class="sxs-lookup"><span data-stu-id="a4045-124">See Also</span></span>

- [<span data-ttu-id="a4045-125">Micro soft. Quantum. prepare. ApproximatelyPrepareArbitraryState</span><span class="sxs-lookup"><span data-stu-id="a4045-125">Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState</span></span>](xref:Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState)