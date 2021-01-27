---
uid: Microsoft.Quantum.Canon.DecomposedIntoTimeStepsCA
title: De functie DecomposedIntoTimeStepsCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DecomposedIntoTimeStepsCA
qsharp.summary: Returns an operation implementing the Trotter–Suzuki integrator for a given operation.
ms.openlocfilehash: e82df36d2e4f3767a152d5c92d7b1897c744a2ca
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840690"
---
# <a name="decomposedintotimestepsca-function"></a><span data-ttu-id="63f00-102">De functie DecomposedIntoTimeStepsCA</span><span class="sxs-lookup"><span data-stu-id="63f00-102">DecomposedIntoTimeStepsCA function</span></span>

<span data-ttu-id="63f00-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="63f00-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="63f00-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="63f00-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="63f00-105">Retourneert een bewerking die de Trotter – Suzuki integrator implementeert voor een bepaalde bewerking.</span><span class="sxs-lookup"><span data-stu-id="63f00-105">Returns an operation implementing the Trotter–Suzuki integrator for a given operation.</span></span>

```qsharp
function DecomposedIntoTimeStepsCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), trotterOrder : Int) : ((Double, 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="63f00-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="63f00-106">Input</span></span>

### <a name="nsteps--int"></a><span data-ttu-id="63f00-107">nSteps: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="63f00-107">nSteps : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="63f00-108">Het aantal bewerkingen dat moet worden uitgesplitst in tijd stappen.</span><span class="sxs-lookup"><span data-stu-id="63f00-108">The number of operations to be decomposed into time steps.</span></span>


### <a name="op--intdoublet--unit--is-adj--ctl"></a><span data-ttu-id="63f00-109">op: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), 't) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="63f00-109">op : ([Int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="63f00-110">Een bewerking die een index-invoer (type `Int` ) en een tijd invoer (type `Double` ) voor de ontleding accepteert.</span><span class="sxs-lookup"><span data-stu-id="63f00-110">An operation which accepts an index input (type `Int`) and a time input (type `Double`) for decomposition.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="63f00-111">trotterOrder: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="63f00-111">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="63f00-112">Hiermee selecteert u de volg orde van de Trotter – Suzuki integrator die moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="63f00-112">Selects the order of the Trotter–Suzuki integrator to be used.</span></span>
<span data-ttu-id="63f00-113">Order 1 en zelfs orders 2, 4, 6,... worden momenteel ondersteund.</span><span class="sxs-lookup"><span data-stu-id="63f00-113">Order 1 and even orders 2, 4, 6,... are currently supported.</span></span>



## <a name="output--doublet--unit--is-adj--ctl"></a><span data-ttu-id="63f00-114">Output: ([Double](xref:microsoft.quantum.lang-ref.double), 't) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="63f00-114">Output : ([Double](xref:microsoft.quantum.lang-ref.double),'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="63f00-115">Retourneert een unitary-implementatie van de Trotter – Suzuki integrator, waarbij de eerste para meter `Double` de grootte van de integratie stap is en de tweede para meter is gericht op het doel.</span><span class="sxs-lookup"><span data-stu-id="63f00-115">Returns a unitary implementing the Trotter–Suzuki integrator, where the first parameter `Double` is the integration step size, and the second parameter is the target acted upon.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="63f00-116">Type parameters</span><span class="sxs-lookup"><span data-stu-id="63f00-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="63f00-117">T</span><span class="sxs-lookup"><span data-stu-id="63f00-117">'T</span></span>

<span data-ttu-id="63f00-118">Het type waarvoor elke stap moet worden uitgevoerd; normaal gesp roken, ofwel `Qubit[]` of `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="63f00-118">The type which each time step should act upon; typically, either `Qubit[]` or `Qubit`.</span></span>

## <a name="remarks"></a><span data-ttu-id="63f00-119">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="63f00-119">Remarks</span></span>

<span data-ttu-id="63f00-120">Als `order` deze functie wordt aangeroepen met gelijk aan `1` , wordt een bewerking geretourneerd die kan worden gesimuleerd door de laagste Trotter – Suzuki integrator $ $ \begin{align} S_1 (\lambda) = \ prod_ {j = 1} ^ {m} e ^ {H_j \lambda}, \end{align} $ $ waar we de notatie van [Quant-pH/0508139](https://arxiv.org/abs/quant-ph/0508139) hebben gevolgd en $ \lambda $ de ontwikkelings tijd zijn (vertegenwoordigd door de eerste invoer van de geretourneerde bewerking), en laat $ \{ H_j \} _ {j = 1} ^ {m} $ zijn de set van (schuine Hermitian) dynamische generators die worden `op(j, lambda, _)` gesimuleerd door de unitary-operator $e ^ {H_j \lambda} $.</span><span class="sxs-lookup"><span data-stu-id="63f00-120">When called with `order` equal to `1`, this function returns an operation that can be simulated by the lowest-order Trotter–Suzuki integrator $$ \begin{align} S_1(\lambda) = \prod_{j = 1}^{m} e^{H_j \lambda}, \end{align} $$ where we have followed the notation of [quant-ph/0508139](https://arxiv.org/abs/quant-ph/0508139) and let $\lambda$ be the evolution time (represented by the first input of the returned operation), and have let $\{H_j\}_{j = 1}^{m}$ be the set of (skew-Hermitian) dynamical generators being integrated such that `op(j, lambda, _)` is simulated by the unitary operator $e^{H_j \lambda}$.</span></span>

<span data-ttu-id="63f00-121">Op dezelfde manier `order` retourneert een van `2` de tweede volg orde symmetrisch Trotter – Suzuki integrator $ $ \begin{align} S_2 (\lambda) = \ prod_ {j = 1} ^ {m} e ^ {H_k \lambda/2} \ prod_ {j ' = m} ^ {1} e ^ {H_ {j '} \lambda/2}.</span><span class="sxs-lookup"><span data-stu-id="63f00-121">Similarly, an `order` of `2` returns the second-order symmetric Trotter–Suzuki integrator $$ \begin{align} S_2(\lambda) = \prod_{j = 1}^{m} e^{H_k \lambda / 2} \prod_{j' = m}^{1} e^{H_{j'} \lambda / 2}.</span></span>
<span data-ttu-id="63f00-122">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="63f00-122">\end{align} $$</span></span>

<span data-ttu-id="63f00-123">Hogere even waarden van `order` worden geïmplementeerd met de recursieve constructie van [Quant-pH/0508139](https://arxiv.org/abs/quant-ph/0508139).</span><span class="sxs-lookup"><span data-stu-id="63f00-123">Higher even values of `order` are implemented using the recursive construction of [quant-ph/0508139](https://arxiv.org/abs/quant-ph/0508139).</span></span>

## <a name="references"></a><span data-ttu-id="63f00-124">Verwijzingen</span><span class="sxs-lookup"><span data-stu-id="63f00-124">References</span></span>

- [<span data-ttu-id="63f00-125">*D. W. Berry, G. Ahokas, R. Cleve, B. C. Sanders*</span><span class="sxs-lookup"><span data-stu-id="63f00-125"> *D. W. Berry, G. Ahokas, R. Cleve, B. C. Sanders* </span></span>](https://arxiv.org/abs/quant-ph/0508139)