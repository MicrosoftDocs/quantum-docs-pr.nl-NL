---
uid: Microsoft.Quantum.Simulation.AdiabaticStateEnergyUnitary
title: Bewerking AdiabaticStateEnergyUnitary
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: AdiabaticStateEnergyUnitary
qsharp.summary: Performs state preparation by applying a `statePrepUnitary` on the input state, followed by adiabatic state preparation using a `adiabaticUnitary`, and finally phase estimation with respect to `qpeUnitary`on the resulting state using a `phaseEstAlgorithm`.
ms.openlocfilehash: d154f9f1f674dc7cf7af9807922b0897540087b4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857960"
---
# <a name="adiabaticstateenergyunitary-operation"></a><span data-ttu-id="ef67c-102">Bewerking AdiabaticStateEnergyUnitary</span><span class="sxs-lookup"><span data-stu-id="ef67c-102">AdiabaticStateEnergyUnitary operation</span></span>

<span data-ttu-id="ef67c-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="ef67c-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="ef67c-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ef67c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ef67c-105">Voert de voor bereiding van de status uit door een `statePrepUnitary` op de invoer status toe te passen, gevolgd door de Adiabatic-status voorbereiding met behulp van een `adiabaticUnitary` -en de laatste fase schatting met betrekking tot `qpeUnitary` de resulterende status met behulp van een `phaseEstAlgorithm` .</span><span class="sxs-lookup"><span data-stu-id="ef67c-105">Performs state preparation by applying a `statePrepUnitary` on the input state, followed by adiabatic state preparation using a `adiabaticUnitary`, and finally phase estimation with respect to `qpeUnitary`on the resulting state using a `phaseEstAlgorithm`.</span></span>

```qsharp
operation AdiabaticStateEnergyUnitary (statePrepUnitary : (Qubit[] => Unit), adiabaticUnitary : (Qubit[] => Unit), qpeUnitary : (Qubit[] => Unit is Adj + Ctl), phaseEstAlgorithm : ((Microsoft.Quantum.Oracles.DiscreteOracle, Qubit[]) => Double), qubits : Qubit[]) : Double
```


## <a name="input"></a><span data-ttu-id="ef67c-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="ef67c-106">Input</span></span>

### <a name="stateprepunitary--qubit--unit"></a><span data-ttu-id="ef67c-107">statePrepUnitary: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] =>- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ef67c-107">statePrepUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="ef67c-108">Een Oracle-voor bereiding van de status voor de eerste dynamische generator.</span><span class="sxs-lookup"><span data-stu-id="ef67c-108">An oracle representing state preparation for the initial dynamical generator.</span></span>


### <a name="adiabaticunitary--qubit--unit"></a><span data-ttu-id="ef67c-109">adiabaticUnitary: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] =>- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ef67c-109">adiabaticUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="ef67c-110">Een Oracle die het Adiabatic-ontwikkelings algoritme vertegenwoordigt dat moet worden gebruikt voor het implementeren van de sweeps in de eind toestand van het algoritme.</span><span class="sxs-lookup"><span data-stu-id="ef67c-110">An oracle representing the adiabatic evolution algorithm to be used to implement the sweeps to the final state of the algorithm.</span></span>


### <a name="qpeunitary--qubit--unit--is-adj--ctl"></a><span data-ttu-id="ef67c-111">qpeUnitary: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="ef67c-111">qpeUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="ef67c-112">Een Oracle vertegenwoordigt een unitary-operator $U $ die de ontwikkeling voor tijd $ \delta t $ weergeeft onder een dynamische generator met de grond staat $ \ket{\phi} $ en de grond status energie $E = \phi \\ , \delta t $.</span><span class="sxs-lookup"><span data-stu-id="ef67c-112">An oracle representing a unitary operator $U$ representing evolution for time $\delta t$ under a dynamical generator with ground state $\ket{\phi}$ and ground state energy $E = \phi\\,\delta t$.</span></span>


### <a name="phaseestalgorithm--discreteoraclequbit--double"></a><span data-ttu-id="ef67c-113">phaseEstAlgorithm: ([DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ef67c-113">phaseEstAlgorithm : ([DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Double](xref:microsoft.quantum.lang-ref.double)</span></span> 

<span data-ttu-id="ef67c-114">Een bewerking die de fase-schatting uitvoert voor een bepaalde unitary-bewerking.</span><span class="sxs-lookup"><span data-stu-id="ef67c-114">An operation that performs phase estimation on a given unitary operation.</span></span>
<span data-ttu-id="ef67c-115">Zie de schatting van de [iteratie fase](/quantum/libraries/characterization#iterative-phase-estimation) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="ef67c-115">See [iterative phase estimation](/quantum/libraries/characterization#iterative-phase-estimation) for more details.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="ef67c-116">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="ef67c-116">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="ef67c-117">Een REGI ster van qubits die moet worden gebruikt om de simulatie uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="ef67c-117">A register of qubits to be used to perform the simulation.</span></span>



## <a name="output--double"></a><span data-ttu-id="ef67c-118">Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ef67c-118">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ef67c-119">Een schatting $ \hat{\phi} $ van de bodem-energie $ \phi $ van de generator vertegenwoordigd door $U $.</span><span class="sxs-lookup"><span data-stu-id="ef67c-119">An estimate $\hat{\phi}$ of the ground state energy $\phi$ of the generator represented by $U$.</span></span>