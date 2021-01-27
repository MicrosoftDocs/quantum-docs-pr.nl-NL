---
uid: Microsoft.Quantum.Characterization.QuantumPhaseEstimation
title: Bewerking QuantumPhaseEstimation
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: QuantumPhaseEstimation
qsharp.summary: Performs the quantum phase estimation algorithm for a given oracle `U` and `targetState`, reading the phase into a big-endian quantum register.
ms.openlocfilehash: 4bdf3de9dab20fa97ba47f15efec4b41a10709f3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839666"
---
# <a name="quantumphaseestimation-operation"></a>Bewerking QuantumPhaseEstimation

Naam ruimte: [micro soft. Quantum. karakte Rise](xref:Microsoft.Quantum.Characterization) ring

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Voert het geraamde algoritme van de Quantum fase uit voor een bepaalde Oracle `U` en `targetState` Lees de fase in een Quantum registratie big endian.

```qsharp
operation QuantumPhaseEstimation (oracle : Microsoft.Quantum.Oracles.DiscreteOracle, targetState : Qubit[], controlRegister : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="oracle--discreteoracle"></a>Oracle: [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)

Een bewerking die $U ^ m $ implementeert voor het opgegeven geheeltallige maatschap m.


### <a name="targetstate--qubit"></a>targetState: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Een Quantum register dat de status $ \ket{\phi} $ aanduidt op basis van $U $. Als $ \ket{\phi} $ een eigenstate is van $U $, $U \ket{\phi} = e ^ {i\phi} \ket{\phi} $ voor $ \phi \in [0, 2 \ PI) $ een onbekende fase.


### <a name="controlregister--bigendian"></a>controlRegister: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)

Een big endian-geheel getal dat kan worden gebruikt voor het beheren van de beschik bare Oracle, en bevat een representatie van $ \phi $ na de toepassing van deze bewerking. Er wordt van uitgegaan dat controlRegister wordt gestart in de oorspronkelijke status $ \ket{00\cdots 0} $, waarbij de lengte van het REGI ster de gewenste precisie aangeeft.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

