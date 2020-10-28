---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracleFromStateOracle
title: De functie DeterministicStateOracleFromStateOracle
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracleFromStateOracle
qsharp.summary: Converts an oracle of type `StateOracle` to `DeterministicStateOracle`.
ms.openlocfilehash: 539cc56e7ae4ead6654aaaae5353a771e06d2bfb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708760"
---
# <a name="deterministicstateoraclefromstateoracle-function"></a>De functie DeterministicStateOracleFromStateOracle

Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)

Pakket [](https://nuget.org/packages/)


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