---
uid: Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates
title: Bewerking EstimateOverlapBetweenStates
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateOverlapBetweenStates
qsharp.summary: Given two operations which each prepare copies of a state, estimates the squared overlap between the states prepared by each operation.
ms.openlocfilehash: e083d6da13b0780905bf365c7a428ebc9666ce9e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839718"
---
# <a name="estimateoverlapbetweenstates-operation"></a><span data-ttu-id="23eb0-102">Bewerking EstimateOverlapBetweenStates</span><span class="sxs-lookup"><span data-stu-id="23eb0-102">EstimateOverlapBetweenStates operation</span></span>

<span data-ttu-id="23eb0-103">Naam ruimte: [micro soft. Quantum. karakte Rise](xref:Microsoft.Quantum.Characterization) ring</span><span class="sxs-lookup"><span data-stu-id="23eb0-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="23eb0-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="23eb0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="23eb0-105">Op basis van twee bewerkingen waarbij elke bewerking een kopie van een staat voorbereidt, wordt een schatting gemaakt van de gekwadrateerde overlap ping tussen de staten die zijn voor bereid.</span><span class="sxs-lookup"><span data-stu-id="23eb0-105">Given two operations which each prepare copies of a state, estimates the squared overlap between the states prepared by each operation.</span></span>

```qsharp
operation EstimateOverlapBetweenStates (preparation1 : (Qubit[] => Unit is Adj), preparation2 : (Qubit[] => Unit is Adj), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="23eb0-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="23eb0-106">Input</span></span>

### <a name="preparation1--qubit--unit--is-adj"></a><span data-ttu-id="23eb0-107">preparation1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="23eb0-107">preparation1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="23eb0-108">De eerste van de twee status voorbereidings bewerkingen die moeten worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="23eb0-108">The first of the two state preparation operations to be compared.</span></span>


### <a name="preparation2--qubit--unit--is-adj"></a><span data-ttu-id="23eb0-109">preparation2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="23eb0-109">preparation2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="23eb0-110">De tweede van de twee status voorbereidings bewerkingen die moeten worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="23eb0-110">The second of the two state preparation operations to be compared.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="23eb0-111">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="23eb0-111">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="23eb0-112">Het aantal qubits waarvoor `commonPreparation` , `preparation1` , en `preparation2` alle Act.</span><span class="sxs-lookup"><span data-stu-id="23eb0-112">The number of qubits on which `commonPreparation`, `preparation1`, and `preparation2` all act.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="23eb0-113">nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="23eb0-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="23eb0-114">Het aantal metingen dat moet worden gebruikt bij het schatten van de overlap ping.</span><span class="sxs-lookup"><span data-stu-id="23eb0-114">The number of measurements to use in estimating the overlap.</span></span>



## <a name="output--double"></a><span data-ttu-id="23eb0-115">Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="23eb0-115">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="23eb0-116">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="23eb0-116">Remarks</span></span>

<span data-ttu-id="23eb0-117">Met deze bewerking wordt de SWAP test gebruikt voor het zoeken naar $ $ \begin{align} \left | \braket{00\cdots 0 | V ^ {\dagger} U | 00 \ cdots 0} \right | ^ 2 \end{align} $ $ waarbij $U $ de unitary weer gave van de actie van is `preparation1` en waarbij $V $ overeenkomt met `preparation2` .</span><span class="sxs-lookup"><span data-stu-id="23eb0-117">This operation uses the SWAP test to find $$ \begin{align} \left| \braket{00\cdots 0 | V^{\dagger} U | 00\cdots 0} \right|^2 \end{align} $$ where $U$ is the unitary representation of the action of `preparation1`, and where $V$ corresponds to `preparation2`.</span></span>

## <a name="see-also"></a><span data-ttu-id="23eb0-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="23eb0-118">See Also</span></span>

- [<span data-ttu-id="23eb0-119">Micro soft. Quantum. karakte Rise ring. EstimateRealOverlapBetweenStates</span><span class="sxs-lookup"><span data-stu-id="23eb0-119">Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates</span></span>](xref:Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates)
- [<span data-ttu-id="23eb0-120">Micro soft. Quantum. karakte Rise ring. EstimateImagOverlapBetweenStates</span><span class="sxs-lookup"><span data-stu-id="23eb0-120">Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates</span></span>](xref:Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates)