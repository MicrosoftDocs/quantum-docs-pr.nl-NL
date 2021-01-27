---
uid: Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates
title: Bewerking EstimateImagOverlapBetweenStates
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateImagOverlapBetweenStates
qsharp.summary: Given two operations which each prepare copies of a state, estimates the imaginary part of the overlap between the states prepared by each operation.
ms.openlocfilehash: f18ce43f9e5ebada4c5cc0aeff1538ac640c7390
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851872"
---
# <a name="estimateimagoverlapbetweenstates-operation"></a><span data-ttu-id="759ac-102">Bewerking EstimateImagOverlapBetweenStates</span><span class="sxs-lookup"><span data-stu-id="759ac-102">EstimateImagOverlapBetweenStates operation</span></span>

<span data-ttu-id="759ac-103">Naam ruimte: [micro soft. Quantum. karakte Rise](xref:Microsoft.Quantum.Characterization) ring</span><span class="sxs-lookup"><span data-stu-id="759ac-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="759ac-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="759ac-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="759ac-105">Op basis van twee bewerkingen die elk een kopie van een staat voorbereiden, wordt het imaginaire deel van de overlap ping tussen de staten die door elke bewerking zijn voor bereid.</span><span class="sxs-lookup"><span data-stu-id="759ac-105">Given two operations which each prepare copies of a state, estimates the imaginary part of the overlap between the states prepared by each operation.</span></span>

```qsharp
operation EstimateImagOverlapBetweenStates (commonPreparation : (Qubit[] => Unit is Adj), preparation1 : (Qubit[] => Unit is Adj + Ctl), preparation2 : (Qubit[] => Unit is Adj + Ctl), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="759ac-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="759ac-106">Input</span></span>

### <a name="commonpreparation--qubit--unit--is-adj"></a><span data-ttu-id="759ac-107">commonPreparation: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="759ac-107">commonPreparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="759ac-108">Een bewerking waarbij een vaste invoer status wordt voor bereid.</span><span class="sxs-lookup"><span data-stu-id="759ac-108">An operation that prepares a fixed input state.</span></span>


### <a name="preparation1--qubit--unit--is-adj--ctl"></a><span data-ttu-id="759ac-109">preparation1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="759ac-109">preparation1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="759ac-110">De eerste van de twee status voorbereidings bewerkingen die moeten worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="759ac-110">The first of the two state preparation operations to be compared.</span></span>


### <a name="preparation2--qubit--unit--is-adj--ctl"></a><span data-ttu-id="759ac-111">preparation2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="759ac-111">preparation2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="759ac-112">De tweede van de twee status voorbereidings bewerkingen die moeten worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="759ac-112">The second of the two state preparation operations to be compared.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="759ac-113">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="759ac-113">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="759ac-114">Het aantal qubits waarvoor `commonPreparation` , `preparation1` , en `preparation2` alle Act.</span><span class="sxs-lookup"><span data-stu-id="759ac-114">The number of qubits on which `commonPreparation`, `preparation1`, and `preparation2` all act.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="759ac-115">nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="759ac-115">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="759ac-116">Het aantal metingen dat moet worden gebruikt bij het schatten van de overlap ping.</span><span class="sxs-lookup"><span data-stu-id="759ac-116">The number of measurements to use in estimating the overlap.</span></span>



## <a name="output--double"></a><span data-ttu-id="759ac-117">Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="759ac-117">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="759ac-118">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="759ac-118">Remarks</span></span>

<span data-ttu-id="759ac-119">Deze bewerking maakt gebruik van de Hadamard-test om het imaginaire deel van $ $ \begin{align} \braket{\psi | te vinden. V ^ {\dagger} U | \psi} \end{align} $ $ waarbij $ \ket{\psi} $ de status is die is voor bereid door `commonPreparation` , $U $ is de unitary weer gave van de actie van en `preparation1` waar $V $ overeenkomt met `preparation2` .</span><span class="sxs-lookup"><span data-stu-id="759ac-119">This operation uses the Hadamard test to find the imaginary part of $$ \begin{align} \braket{\psi | V^{\dagger} U | \psi} \end{align} $$ where $\ket{\psi}$ is the state prepared by `commonPreparation`, $U$ is the unitary representation of the action of `preparation1`, and where $V$ corresponds to `preparation2`.</span></span>

## <a name="references"></a><span data-ttu-id="759ac-120">Verwijzingen</span><span class="sxs-lookup"><span data-stu-id="759ac-120">References</span></span>

- <span data-ttu-id="759ac-121">Aharonov *et al.* [quantity-pH/0511096](https://arxiv.org/abs/quant-ph/0511096).</span><span class="sxs-lookup"><span data-stu-id="759ac-121">Aharonov *et al.* [quant-ph/0511096](https://arxiv.org/abs/quant-ph/0511096).</span></span>

## <a name="see-also"></a><span data-ttu-id="759ac-122">Zie ook</span><span class="sxs-lookup"><span data-stu-id="759ac-122">See Also</span></span>

- [<span data-ttu-id="759ac-123">Micro soft. Quantum. karakte Rise ring. EstimateRealOverlapBetweenStates</span><span class="sxs-lookup"><span data-stu-id="759ac-123">Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates</span></span>](xref:Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates)
- [<span data-ttu-id="759ac-124">Micro soft. Quantum. karakte Rise ring. EstimateOverlapBetweenStates</span><span class="sxs-lookup"><span data-stu-id="759ac-124">Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates</span></span>](xref:Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates)