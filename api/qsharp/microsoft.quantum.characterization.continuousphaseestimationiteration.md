---
uid: Microsoft.Quantum.Characterization.ContinuousPhaseEstimationIteration
title: Bewerking ContinuousPhaseEstimationIteration
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: ContinuousPhaseEstimationIteration
qsharp.summary: Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using arbitrary real powers of a unitary oracle.
ms.openlocfilehash: a3914a4b19e3b898b6de8808699da09d386f487a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703658"
---
# <a name="continuousphaseestimationiteration-operation"></a>Bewerking ContinuousPhaseEstimationIteration

Naam ruimte: [micro soft. Quantum. karakte Rise](xref:Microsoft.Quantum.Characterization) ring

Pakket [](https://nuget.org/packages/)


Voert een enkele herhaling van een iteratieve fase van een herhaald (klassiek) Phase uit met wille keurige echte bevoegdheden van een unitary Oracle.

```qsharp
operation ContinuousPhaseEstimationIteration (oracle : Microsoft.Quantum.Oracles.ContinuousOracle, time : Double, theta : Double, targetState : Qubit[], controlQubit : Qubit) : Unit
```


## <a name="input"></a>Invoer

### <a name="oracle--continuousoracle"></a>Oracle: [ContinuousOracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)

De bewerking wordt uitgevoerd op een dubbel $t $ en een REGI ster, waardoor $U ^ t $ wordt toegepast op het betreffende REGI ster, waarbij $U $ de unitary is waarvan de fase moet worden geschat, waarbij $t $ de gehele kracht is die aan de Oracle is gegeven


### <a name="time--double"></a>tijd: [dubbel](xref:microsoft.quantum.lang-ref.double)

Aantal keren dat de opgegeven unitary Oracle moet worden toegepast.


### <a name="theta--double"></a>Theta: [dubbel](xref:microsoft.quantum.lang-ref.double)

De hoek waarmee de fase van het besturings element Qubit wordt omgekeerd voordat de doel status wordt toegepast.


### <a name="targetstate--qubit"></a>targetState: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

REGI ster van de door de opgegeven unitary Oracle gehandelde status.


### <a name="controlqubit--qubit"></a>controlQubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)





## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

