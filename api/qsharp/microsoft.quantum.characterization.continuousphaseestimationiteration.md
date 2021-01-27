---
uid: Microsoft.Quantum.Characterization.ContinuousPhaseEstimationIteration
title: Bewerking ContinuousPhaseEstimationIteration
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: ContinuousPhaseEstimationIteration
qsharp.summary: Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using arbitrary real powers of a unitary oracle.
ms.openlocfilehash: 925b9040f6d9cda074b18a6f9079ccb653f9fa98
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851895"
---
# <a name="continuousphaseestimationiteration-operation"></a>Bewerking ContinuousPhaseEstimationIteration

Naam ruimte: [micro soft. Quantum. karakte Rise](xref:Microsoft.Quantum.Characterization) ring

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Voert een enkele herhaling van een iteratieve fase van een herhaald (klassiek) Phase uit met wille keurige echte bevoegdheden van een unitary Oracle.

```qsharp
operation ContinuousPhaseEstimationIteration (oracle : Microsoft.Quantum.Oracles.ContinuousOracle, time : Double, theta : Double, targetState : Qubit[], controlQubit : Qubit) : Unit is Adj + Ctl
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

