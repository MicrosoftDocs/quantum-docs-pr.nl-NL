---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracleFromStateOracle
title: De functie DeterministicStateOracleFromStateOracle
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracleFromStateOracle
qsharp.summary: Converts an oracle of type `StateOracle` to `DeterministicStateOracle`.
ms.openlocfilehash: af545a7d6e82e654ee36ab3ba77c8f8be3384b96
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854560"
---
# <a name="deterministicstateoraclefromstateoracle-function"></a>De functie DeterministicStateOracleFromStateOracle

Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Converteert een Oracle van het type `StateOracle` naar `DeterministicStateOracle` .

```qsharp
function DeterministicStateOracleFromStateOracle (idxFlagQubit : Int, stateOracle : Microsoft.Quantum.Oracles.StateOracle) : Microsoft.Quantum.Oracles.DeterministicStateOracle
```


## <a name="input"></a>Invoer

### <a name="idxflagqubit--int"></a>idxFlagQubit: [int](xref:microsoft.quantum.lang-ref.int)

De index voor de vlag Qubit van de `stateOracle` $A $, die expliciet op twee registers reageert: de vlag $f $ en het systeem $s $, bijvoorbeeld $A \ket {0} \_ f\ket {\ psi} \_ s $.


### <a name="stateoracle--stateoracle"></a>stateOracle: [stateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)

Een status voorbereiding Oracle $A $ van type `StateOracle` .



## <a name="output--deterministicstateoracle"></a>Uitvoer: [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)

Voor de voor bereiding van de Oracle-$A $, maar nu van het type `DeterministicStateOracle` , wordt deze toegepast op een REGI ster waarbij $a, s $ niet langer expliciet gescheiden is, bijvoorbeeld  $A \ket{0\psi} \_ {as} $.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Oracles. StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)
- [Micro soft. Quantum. Oracles. DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)