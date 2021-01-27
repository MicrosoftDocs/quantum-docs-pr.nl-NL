---
uid: Microsoft.Quantum.Characterization.RobustPhaseEstimation
title: Bewerking RobustPhaseEstimation
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: RobustPhaseEstimation
qsharp.summary: Performs the robust non-iterative quantum phase estimation algorithm for a given oracle `U` and eigenstate, and provides a single real-valued estimate of the phase with variance scaling at the Heisenberg limit.
ms.openlocfilehash: 4b37c8275a5b2aee8534bacc5831281aa498b57d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851804"
---
# <a name="robustphaseestimation-operation"></a>Bewerking RobustPhaseEstimation

Naam ruimte: [micro soft. Quantum. karakte Rise](xref:Microsoft.Quantum.Characterization) ring

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Voert het robuuste algoritme voor het schatten van de niet-iteratieve Quantum fase voor een bepaalde Oracle `U` -en eigenstate en biedt een enkele geschatte schatting van de fase met variantie schaaling bij de Heisenberg-limiet.

```qsharp
operation RobustPhaseEstimation (bitsPrecision : Int, oracle : Microsoft.Quantum.Oracles.DiscreteOracle, targetState : Qubit[]) : Double
```


## <a name="input"></a>Invoer

### <a name="bitsprecision--int"></a>bitsPrecision: [int](xref:microsoft.quantum.lang-ref.int)

Dit biedt een schatting van $ \phi $ met de standaard afwijking $ \sigma \le 2 \ pi/2 ^ \text{bitsPrecision} $ met behulp van een aantal query's dat kan worden geschaald zoals $ \sigma \le 10,7 \pi/\Text{# van query's} $.


### <a name="oracle--discreteoracle"></a>Oracle: [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)

Een bewerking die $U ^ m $ implementeert voor gegeven geheeltallige maat regelen, $m $.


### <a name="targetstate--qubit"></a>targetState: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Een Quantum registratie waarmee $ wordt $U. Als er een eigenstate $ \ket{\phi} $ van $U $ wordt opgeslagen, wordt $U \ket{\phi} = e ^ {i\phi} \ket{\phi} $ voor $ \phi\in (-\pi, \pi] $ een onbekende fase.



## <a name="output--double"></a>Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)



## <a name="remarks"></a>Opmerkingen

In de limiet van een groot aantal query's Cramer-Rao lagere grenzen voor de standaard afwijking van de schatting van $ \phi $ voldoen aan $ \sigma \ge 2 \pi/\Text{# van query's} $.

## <a name="references"></a>Verwijzingen

- Robuuste kalibratie van een universele Single-Qubit Gate-Set via een robuuste fase schatting Shelby Kimmel, Guang Hao low, Theodore J. Yoder https://arxiv.org/abs/1502.02677