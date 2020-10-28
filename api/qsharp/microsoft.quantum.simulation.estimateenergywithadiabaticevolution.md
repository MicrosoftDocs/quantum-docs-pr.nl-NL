---
uid: Microsoft.Quantum.Simulation.EstimateEnergyWithAdiabaticEvolution
title: Bewerking EstimateEnergyWithAdiabaticEvolution
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EstimateEnergyWithAdiabaticEvolution
qsharp.summary: Performs state preparation by applying a `statePrepUnitary` on an automatically allocated input state, followed by adiabatic state preparation using a `adiabaticUnitary`, and finally phase estimation with respect to `qpeUnitary`on the resulting state using a `phaseEstAlgorithm`.
ms.openlocfilehash: 3fdbdd83b784cdc560e3160151fdf4ba4e7115e6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707819"
---
# <a name="estimateenergywithadiabaticevolution-operation"></a><span data-ttu-id="5cb9b-102">Bewerking EstimateEnergyWithAdiabaticEvolution</span><span class="sxs-lookup"><span data-stu-id="5cb9b-102">EstimateEnergyWithAdiabaticEvolution operation</span></span>

<span data-ttu-id="5cb9b-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="5cb9b-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="5cb9b-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5cb9b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5cb9b-105">Voert de voor bereiding van de status uit door een ' `statePrepUnitary` automatisch toegewezen invoer status ' toe te passen, gevolgd door de Adiabatic-status voorbereiding met behulp van een `adiabaticUnitary` -en de laatste fase schatting met betrekking tot `qpeUnitary` de resulterende status met behulp van een `phaseEstAlgorithm` .</span><span class="sxs-lookup"><span data-stu-id="5cb9b-105">Performs state preparation by applying a `statePrepUnitary` on an automatically allocated input state, followed by adiabatic state preparation using a `adiabaticUnitary`, and finally phase estimation with respect to `qpeUnitary`on the resulting state using a `phaseEstAlgorithm`.</span></span>

```qsharp
operation EstimateEnergyWithAdiabaticEvolution (nQubits : Int, statePrepUnitary : (Qubit[] => Unit), adiabaticUnitary : (Qubit[] => Unit), qpeUnitary : (Qubit[] => Unit is Adj + Ctl), phaseEstAlgorithm : ((Microsoft.Quantum.Oracles.DiscreteOracle, Qubit[]) => Double)) : Double
```


## <a name="input"></a><span data-ttu-id="5cb9b-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="5cb9b-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="5cb9b-107">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5cb9b-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5cb9b-108">Aantal qubits dat wordt gebruikt voor de simulatie.</span><span class="sxs-lookup"><span data-stu-id="5cb9b-108">Number of qubits used for the simulation.</span></span>


### <a name="stateprepunitary--qubit--unit"></a><span data-ttu-id="5cb9b-109">statePrepUnitary: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] =>- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5cb9b-109">statePrepUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="5cb9b-110">Een Oracle-voor bereiding van de status voor de eerste dynamische generator.</span><span class="sxs-lookup"><span data-stu-id="5cb9b-110">An oracle representing state preparation for the initial dynamical generator.</span></span>


### <a name="adiabaticunitary--qubit--unit"></a><span data-ttu-id="5cb9b-111">adiabaticUnitary: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] =>- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5cb9b-111">adiabaticUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="5cb9b-112">Een Oracle die het Adiabatic-ontwikkelings algoritme vertegenwoordigt dat moet worden gebruikt voor het implementeren van de sweeps in de eind toestand van het algoritme.</span><span class="sxs-lookup"><span data-stu-id="5cb9b-112">An oracle representing the adiabatic evolution algorithm to be used to implement the sweeps to the final state of the algorithm.</span></span>


### <a name="qpeunitary--qubit--unit-adj--ctl"></a><span data-ttu-id="5cb9b-113">qpeUnitary: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="5cb9b-113">qpeUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="5cb9b-114">Een Oracle vertegenwoordigt een unitary-operator $U $ die de ontwikkeling voor tijd $ \delta t $ weergeeft onder een dynamische generator met de grond staat $ \ket{\phi} $ en de grond status energie $E = \phi \\ , \delta t $.</span><span class="sxs-lookup"><span data-stu-id="5cb9b-114">An oracle representing a unitary operator $U$ representing evolution for time $\delta t$ under a dynamical generator with ground state $\ket{\phi}$ and ground state energy $E = \phi\\,\delta t$.</span></span>


### <a name="phaseestalgorithm--discreteoraclequbit--double"></a><span data-ttu-id="5cb9b-115">phaseEstAlgorithm: ([DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5cb9b-115">phaseEstAlgorithm : ([DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Double](xref:microsoft.quantum.lang-ref.double)</span></span> 

<span data-ttu-id="5cb9b-116">Een bewerking die de fase-schatting uitvoert voor een bepaalde unitary-bewerking.</span><span class="sxs-lookup"><span data-stu-id="5cb9b-116">An operation that performs phase estimation on a given unitary operation.</span></span>
<span data-ttu-id="5cb9b-117">Zie de schatting van de [iteratie fase](/quantum/libraries/characterization#iterative-phase-estimation) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="5cb9b-117">See [iterative phase estimation](/quantum/libraries/characterization#iterative-phase-estimation) for more details.</span></span>



## <a name="output--double"></a><span data-ttu-id="5cb9b-118">Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5cb9b-118">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5cb9b-119">Een schatting $ \hat{\phi} $ van de bodem-energie $ \phi $ van de generator vertegenwoordigd door $U $.</span><span class="sxs-lookup"><span data-stu-id="5cb9b-119">An estimate $\hat{\phi}$ of the ground state energy $\phi$ of the generator represented by $U$.</span></span>