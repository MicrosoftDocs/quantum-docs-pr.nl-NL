---
uid: Microsoft.Quantum.Characterization.DiscretePhaseEstimationIteration
title: Bewerking DiscretePhaseEstimationIteration
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: DiscretePhaseEstimationIteration
qsharp.summary: Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using integer powers of a unitary oracle.
ms.openlocfilehash: 167b53d7108c64d11a4f258d17e90ba78d7dd8d8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703653"
---
# <a name="discretephaseestimationiteration-operation"></a>Bewerking DiscretePhaseEstimationIteration

Naam ruimte: [micro soft. Quantum. karakte Rise](xref:Microsoft.Quantum.Characterization) ring

Pakket [](https://nuget.org/packages/)


Voert een enkele herhaling van een iteratieve fase van een herhaald (klassiek) Phase uit met een geheel getal van een unitary Oracle.

```qsharp
operation DiscretePhaseEstimationIteration (oracle : Microsoft.Quantum.Oracles.DiscreteOracle, power : Int, theta : Double, targetState : Qubit[], controlQubit : Qubit) : Unit
```


## <a name="input"></a>Invoer

### <a name="oracle--discreteoracle"></a>Oracle: [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)

De bewerking wordt uitgevoerd op een geheel getal en een REGI ster, waardoor de $U ^ m $ wordt toegepast op het opgegeven REGI ster, waarbij $U $ de unitary is waarvan de fase wordt geschat en waarbij $m $ de gehele voeding is die aan de Oracle is gegeven


### <a name="power--int"></a>energie: [int](xref:microsoft.quantum.lang-ref.int)

Aantal keren dat de opgegeven unitary Oracle moet worden toegepast.


### <a name="theta--double"></a>Theta: [dubbel](xref:microsoft.quantum.lang-ref.double)

De hoek waarmee de fase van het besturings element Qubit wordt omgekeerd voordat de doel status wordt toegepast.


### <a name="targetstate--qubit"></a>targetState: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

REGI ster van de door de opgegeven unitary Oracle gehandelde status.


### <a name="controlqubit--qubit"></a>controlQubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Een hulp Qubit gebruikt om de toepassing van de opgegeven Oracle te beheren.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

