---
uid: Microsoft.Quantum.Simulation.EstimateEnergy
title: Bewerking EstimateEnergy
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EstimateEnergy
qsharp.summary: Performs state preparation by applying a `statePrepUnitary` on an automatically allocated input state phase estimation with respect to `qpeUnitary`on the resulting state using a `phaseEstAlgorithm`.
ms.openlocfilehash: f9243557718e12d168afadbf641492291afd1704
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856767"
---
# <a name="estimateenergy-operation"></a>Bewerking EstimateEnergy

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Voert de voor bereiding van de status uit door een `statePrepUnitary` in een automatisch toegewezen schatting van de invoer status fase toe te passen met betrekking tot `qpeUnitary` de resulterende status met behulp van een `phaseEstAlgorithm` .

```qsharp
operation EstimateEnergy (nQubits : Int, statePrepUnitary : (Qubit[] => Unit), qpeUnitary : (Qubit[] => Unit is Adj + Ctl), phaseEstAlgorithm : ((Microsoft.Quantum.Oracles.DiscreteOracle, Qubit[]) => Double)) : Double
```


## <a name="input"></a>Invoer

### <a name="nqubits--int"></a>nQubits: [int](xref:microsoft.quantum.lang-ref.int)

Aantal qubits dat wordt gebruikt voor het uitvoeren van simulatie.


### <a name="stateprepunitary--qubit--unit"></a>statePrepUnitary: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] =>- [eenheid](xref:microsoft.quantum.lang-ref.unit) 

Een Oracle-voor bereiding van de status voor de eerste dynamische generator.


### <a name="qpeunitary--qubit--unit--is-adj--ctl"></a>qpeUnitary: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

Een Oracle vertegenwoordigt een unitary-operator $U $ die de ontwikkeling voor tijd $ \delta t $ weergeeft onder een dynamische generator met de grond staat $ \ket{\phi} $ en de grond status energie $E = \phi \\ , \delta t $.


### <a name="phaseestalgorithm--discreteoraclequbit--double"></a>phaseEstAlgorithm: ([DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Double](xref:microsoft.quantum.lang-ref.double) 

Een bewerking die de fase-schatting uitvoert voor een bepaalde unitary-bewerking.
Zie de schatting van de [iteratie fase](/quantum/libraries/characterization#iterative-phase-estimation) voor meer informatie.



## <a name="output--double"></a>Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)

Een schatting $ \hat{\phi} $ van de bodem-energie $ \phi $ van de grond staats energie van de generator vertegenwoordigd door $U $.