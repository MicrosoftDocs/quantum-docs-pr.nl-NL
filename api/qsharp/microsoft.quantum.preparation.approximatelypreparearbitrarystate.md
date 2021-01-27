---
uid: Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState
title: Bewerking ApproximatelyPrepareArbitraryState
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: ApproximatelyPrepareArbitraryState
qsharp.summary: >-
  > [!WARNING]

  > ApproximatelyPrepareArbitraryState has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryStateCP> instead.


  Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients, up to a given approximation tolerance.
ms.openlocfilehash: dab7647ab6e6a8592ab49ad7b7d398cb43b4f486
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854425"
---
# <a name="approximatelypreparearbitrarystate-operation"></a><span data-ttu-id="8dcbc-102">Bewerking ApproximatelyPrepareArbitraryState</span><span class="sxs-lookup"><span data-stu-id="8dcbc-102">ApproximatelyPrepareArbitraryState operation</span></span>

<span data-ttu-id="8dcbc-103">Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="8dcbc-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="8dcbc-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8dcbc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="8dcbc-105">ApproximatelyPrepareArbitraryState is afgeschaft.</span><span class="sxs-lookup"><span data-stu-id="8dcbc-105">ApproximatelyPrepareArbitraryState has been deprecated.</span></span> <span data-ttu-id="8dcbc-106">Gebruik <xref:Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryStateCP> in plaats daarvan.</span><span class="sxs-lookup"><span data-stu-id="8dcbc-106">Please use <xref:Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryStateCP> instead.</span></span>

<span data-ttu-id="8dcbc-107">Op basis van een set coëfficiënten en een versleuteld Quantum REGI ster van little endian, wordt een staat voor het REGI ster die is beschreven door de gegeven coëfficiënten, voor een bepaalde aanpassings tolerantie voor bereid.</span><span class="sxs-lookup"><span data-stu-id="8dcbc-107">Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients, up to a given approximation tolerance.</span></span>

```qsharp
operation ApproximatelyPrepareArbitraryState (tolerance : Double, coefficients : Microsoft.Quantum.Math.ComplexPolar[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="8dcbc-108">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="8dcbc-108">Description</span></span>

<span data-ttu-id="8dcbc-109">Met deze bewerking wordt een wille keurige Quantum status $ \ket{\psi} $ voor bereid met complexe coëfficiënten $r _j e ^ {i t_j} $ van de $n $-Qubit reken kundige status $ \ket{0 \cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="8dcbc-109">This operation prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0 \cdots 0}$.</span></span>
<span data-ttu-id="8dcbc-110">Met name de actie van deze bewerking kan worden gesimuleerd door de unitary-trans formatie $U $ die op de status alles-nullen werkt als</span><span class="sxs-lookup"><span data-stu-id="8dcbc-110">In particular, the action of this operation can be simulated by the a unitary transformation $U$ which acts on the all-zeros state as</span></span>

<span data-ttu-id="8dcbc-111">$ $ \begin{align} U\ket {0... 0} & = \ket{\psi} \\ \\ & = \frac{\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \ket{j}} {\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="8dcbc-111">$$ \begin{align} U\ket{0...0} & = \ket{\psi} \\\\ & = \frac{ \sum_{j=0}^{2^n-1} r_j e^{i t_j} \ket{j} }{ \sqrt{\sum_{j=0}^{2^n-1} |r_j|^2} }.</span></span>
<span data-ttu-id="8dcbc-112">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="8dcbc-112">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="8dcbc-113">Invoer</span><span class="sxs-lookup"><span data-stu-id="8dcbc-113">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="8dcbc-114">tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8dcbc-114">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8dcbc-115">De aanpassings tolerantie die moet worden gebruikt bij het voorbereiden van de gegeven status.</span><span class="sxs-lookup"><span data-stu-id="8dcbc-115">The approximation tolerance to be used when preparing the given state.</span></span>


### <a name="coefficients--complexpolar"></a><span data-ttu-id="8dcbc-116">coëfficiënten: [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span><span class="sxs-lookup"><span data-stu-id="8dcbc-116">coefficients : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span></span>

<span data-ttu-id="8dcbc-117">Matrix van Maxi maal $2 ^ n $ complexe coëfficiënten die worden weer gegeven door hun absolute waarde en fase $ (r_j, t_j) $.</span><span class="sxs-lookup"><span data-stu-id="8dcbc-117">Array of up to $2^n$ complex coefficients represented by their absolute value and phase $(r_j, t_j)$.</span></span> <span data-ttu-id="8dcbc-118">De $j $ th indexeert de nummer status $ \ket{j} $ gecodeerd in de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="8dcbc-118">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="8dcbc-119">qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="8dcbc-119">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="8dcbc-120">Qubit registreert coderings nummer statussen in de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="8dcbc-120">Qubit register encoding number states in little-endian format.</span></span> <span data-ttu-id="8dcbc-121">Dit wordt verwacht te worden geïnitialiseerd in de status van de berekening $ \ket{0...0} $.</span><span class="sxs-lookup"><span data-stu-id="8dcbc-121">This is expected to be initialized in the computational basis state $\ket{0...0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8dcbc-122">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8dcbc-122">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="8dcbc-123">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="8dcbc-123">Remarks</span></span>

<span data-ttu-id="8dcbc-124">Negatieve invoer coëfficiënten $r _j < $0 worden beschouwd als positief met waarde $ | r_j | $.</span><span class="sxs-lookup"><span data-stu-id="8dcbc-124">Negative input coefficients $r_j < 0$ will be treated as though positive with value $|r_j|$.</span></span> <span data-ttu-id="8dcbc-125">`coefficients` wordt aangevuld met elementen $ (r_j, t_j) = (0,0, 0,0) $ als er minder dan $2 ^ n $ is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="8dcbc-125">`coefficients` will be padded with elements $(r_j, t_j) = (0.0, 0.0)$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="8dcbc-126">Verwijzingen</span><span class="sxs-lookup"><span data-stu-id="8dcbc-126">References</span></span>

- <span data-ttu-id="8dcbc-127">Synthese van Quantum Logic-circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="8dcbc-127">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="8dcbc-128">Zie ook</span><span class="sxs-lookup"><span data-stu-id="8dcbc-128">See Also</span></span>

- [<span data-ttu-id="8dcbc-129">Micro soft. Quantum. prepare. ApproximatelyPrepareArbitraryState</span><span class="sxs-lookup"><span data-stu-id="8dcbc-129">Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState</span></span>](xref:Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState)