---
uid: Microsoft.Quantum.Simulation.EstimateEnergy
title: Bewerking EstimateEnergy
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EstimateEnergy
qsharp.summary: Performs state preparation by applying a `statePrepUnitary` on an automatically allocated input state phase estimation with respect to `qpeUnitary`on the resulting state using a `phaseEstAlgorithm`.
ms.openlocfilehash: 0a02a8aad891c45b184b9b18d4e9383236485940
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229491"
---
# <a name="estimateenergy-operation"></a><span data-ttu-id="5b3e0-102">Bewerking EstimateEnergy</span><span class="sxs-lookup"><span data-stu-id="5b3e0-102">EstimateEnergy operation</span></span>

<span data-ttu-id="5b3e0-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="5b3e0-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="5b3e0-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5b3e0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5b3e0-105">Voert de voor bereiding van de status uit door een `statePrepUnitary` in een automatisch toegewezen schatting van de invoer status fase toe te passen met betrekking tot `qpeUnitary` de resulterende status met behulp van een `phaseEstAlgorithm` .</span><span class="sxs-lookup"><span data-stu-id="5b3e0-105">Performs state preparation by applying a `statePrepUnitary` on an automatically allocated input state phase estimation with respect to `qpeUnitary`on the resulting state using a `phaseEstAlgorithm`.</span></span>

```qsharp
operation EstimateEnergy (nQubits : Int, statePrepUnitary : (Qubit[] => Unit), qpeUnitary : (Qubit[] => Unit is Adj + Ctl), phaseEstAlgorithm : ((Microsoft.Quantum.Oracles.DiscreteOracle, Qubit[]) => Double)) : Double
```


## <a name="input"></a><span data-ttu-id="5b3e0-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="5b3e0-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="5b3e0-107">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5b3e0-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5b3e0-108">Aantal qubits dat wordt gebruikt voor het uitvoeren van simulatie.</span><span class="sxs-lookup"><span data-stu-id="5b3e0-108">Number of qubits used to perform simulation.</span></span>


### <a name="stateprepunitary--qubit--unit"></a><span data-ttu-id="5b3e0-109">statePrepUnitary: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] =>- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5b3e0-109">statePrepUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="5b3e0-110">Een Oracle-voor bereiding van de status voor de eerste dynamische generator.</span><span class="sxs-lookup"><span data-stu-id="5b3e0-110">An oracle representing state preparation for the initial dynamical generator.</span></span>


### <a name="qpeunitary--qubit--unit--is-adj--ctl"></a><span data-ttu-id="5b3e0-111">qpeUnitary: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="5b3e0-111">qpeUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="5b3e0-112">Een Oracle vertegenwoordigt een unitary-operator $U $ die de ontwikkeling voor tijd $ \delta t $ weergeeft onder een dynamische generator met de grond staat $ \ket{\phi} $ en de grond status energie $E = \phi \\ , \delta t $.</span><span class="sxs-lookup"><span data-stu-id="5b3e0-112">An oracle representing a unitary operator $U$ representing evolution for time $\delta t$ under a dynamical generator with ground state $\ket{\phi}$ and ground state energy $E = \phi\\,\delta t$.</span></span>


### <a name="phaseestalgorithm--discreteoraclequbit--double"></a><span data-ttu-id="5b3e0-113">phaseEstAlgorithm: ([DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5b3e0-113">phaseEstAlgorithm : ([DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Double](xref:microsoft.quantum.lang-ref.double)</span></span> 

<span data-ttu-id="5b3e0-114">Een bewerking die de fase-schatting uitvoert voor een bepaalde unitary-bewerking.</span><span class="sxs-lookup"><span data-stu-id="5b3e0-114">An operation that performs phase estimation on a given unitary operation.</span></span>
<span data-ttu-id="5b3e0-115">Zie de schatting van de [iteratie fase](/quantum/libraries/characterization#iterative-phase-estimation) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="5b3e0-115">See [iterative phase estimation](/quantum/libraries/characterization#iterative-phase-estimation) for more details.</span></span>



## <a name="output--double"></a><span data-ttu-id="5b3e0-116">Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5b3e0-116">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5b3e0-117">Een schatting $ \hat{\phi} $ van de bodem-energie $ \phi $ van de grond staats energie van de generator vertegenwoordigd door $U $.</span><span class="sxs-lookup"><span data-stu-id="5b3e0-117">An estimate $\hat{\phi}$ of the ground state energy $\phi$ of the ground state energy of the generator represented by $U$.</span></span>