---
uid: Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates
title: Bewerking EstimateRealOverlapBetweenStates
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateRealOverlapBetweenStates
qsharp.summary: Given two operations which each prepare copies of a state, estimates the real part of the overlap between the states prepared by each operation.
ms.openlocfilehash: 01631bcbff2bff26ddc1db4e42d90ac4f8380bd4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703611"
---
# <a name="estimaterealoverlapbetweenstates-operation"></a><span data-ttu-id="ae0e0-102">Bewerking EstimateRealOverlapBetweenStates</span><span class="sxs-lookup"><span data-stu-id="ae0e0-102">EstimateRealOverlapBetweenStates operation</span></span>

<span data-ttu-id="ae0e0-103">Naam ruimte: [micro soft. Quantum. karakte Rise](xref:Microsoft.Quantum.Characterization) ring</span><span class="sxs-lookup"><span data-stu-id="ae0e0-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="ae0e0-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ae0e0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ae0e0-105">Op basis van twee bewerkingen die elk een kopie van een staat voorbereiden, wordt het werkelijke deel van de overlap ping tussen de staten die door elke bewerking zijn voor bereid, geschat.</span><span class="sxs-lookup"><span data-stu-id="ae0e0-105">Given two operations which each prepare copies of a state, estimates the real part of the overlap between the states prepared by each operation.</span></span>

```qsharp
operation EstimateRealOverlapBetweenStates (commonPreparation : (Qubit[] => Unit is Adj), preparation1 : (Qubit[] => Unit is Adj + Ctl), preparation2 : (Qubit[] => Unit is Adj + Ctl), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="ae0e0-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="ae0e0-106">Input</span></span>

### <a name="commonpreparation--qubit--unit-adj"></a><span data-ttu-id="ae0e0-107">commonPreparation: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="ae0e0-107">commonPreparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="ae0e0-108">Een bewerking waarbij een vaste invoer status wordt voor bereid.</span><span class="sxs-lookup"><span data-stu-id="ae0e0-108">An operation that prepares a fixed input state.</span></span>


### <a name="preparation1--qubit--unit-adj--ctl"></a><span data-ttu-id="ae0e0-109">preparation1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="ae0e0-109">preparation1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="ae0e0-110">De eerste van de twee status voorbereidings bewerkingen die moeten worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="ae0e0-110">The first of the two state preparation operations to be compared.</span></span>


### <a name="preparation2--qubit--unit-adj--ctl"></a><span data-ttu-id="ae0e0-111">preparation2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="ae0e0-111">preparation2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="ae0e0-112">De tweede van de twee status voorbereidings bewerkingen die moeten worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="ae0e0-112">The second of the two state preparation operations to be compared.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="ae0e0-113">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ae0e0-113">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ae0e0-114">Het aantal qubits waarvoor `commonPreparation` , `preparation1` , en `preparation2` alle Act.</span><span class="sxs-lookup"><span data-stu-id="ae0e0-114">The number of qubits on which `commonPreparation`, `preparation1`, and `preparation2` all act.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="ae0e0-115">nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ae0e0-115">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ae0e0-116">Het aantal metingen dat moet worden gebruikt bij het schatten van de overlap ping.</span><span class="sxs-lookup"><span data-stu-id="ae0e0-116">The number of measurements to use in estimating the overlap.</span></span>



## <a name="output--double"></a><span data-ttu-id="ae0e0-117">Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ae0e0-117">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="ae0e0-118">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="ae0e0-118">Remarks</span></span>

<span data-ttu-id="ae0e0-119">Deze bewerking maakt gebruik van de Hadamard-test om het echte deel van $ $ \begin{align} \braket{\psi te vinden. V ^ {\dagger} U | \psi} \end{align} $ $ waarbij $ \ket{\psi} $ de status is die is voor bereid door `commonPreparation` , $U $ is de unitary weer gave van de actie van en `preparation1` waar $V $ overeenkomt met `preparation2` .</span><span class="sxs-lookup"><span data-stu-id="ae0e0-119">This operation uses the Hadamard test to find the real part of $$ \begin{align} \braket{\psi | V^{\dagger} U | \psi} \end{align} $$ where $\ket{\psi}$ is the state prepared by `commonPreparation`, $U$ is the unitary representation of the action of `preparation1`, and where $V$ corresponds to `preparation2`.</span></span>

## <a name="references"></a><span data-ttu-id="ae0e0-120">Naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="ae0e0-120">References</span></span>

- <span data-ttu-id="ae0e0-121">Aharonov *et al.* [quantity-pH/0511096](https://arxiv.org/abs/quant-ph/0511096).</span><span class="sxs-lookup"><span data-stu-id="ae0e0-121">Aharonov *et al.* [quant-ph/0511096](https://arxiv.org/abs/quant-ph/0511096).</span></span>

## <a name="see-also"></a><span data-ttu-id="ae0e0-122">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ae0e0-122">See Also</span></span>

- [<span data-ttu-id="ae0e0-123">Micro soft. Quantum. karakte Rise ring. EstimateImagOverlapBetweenStates</span><span class="sxs-lookup"><span data-stu-id="ae0e0-123">Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates</span></span>](xref:Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates)
- [<span data-ttu-id="ae0e0-124">Micro soft. Quantum. karakte Rise ring. EstimateOverlapBetweenStates</span><span class="sxs-lookup"><span data-stu-id="ae0e0-124">Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates</span></span>](xref:Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates)