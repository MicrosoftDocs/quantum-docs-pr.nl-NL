---
uid: Microsoft.Quantum.Oracles.ObliviousOracleFromDeterministicStateOracle
title: De functie ObliviousOracleFromDeterministicStateOracle
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ObliviousOracleFromDeterministicStateOracle
qsharp.summary: Combines the oracles `DeterministicStateOracle` and `ObliviousOracle`.
ms.openlocfilehash: 8f1fe34e38edefba228fb9d01e1712e4c0916970
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226686"
---
# <a name="obliviousoraclefromdeterministicstateoracle-function"></a>De functie ObliviousOracleFromDeterministicStateOracle

Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Combineert de Oracle- `DeterministicStateOracle` en `ObliviousOracle` .

```qsharp
function ObliviousOracleFromDeterministicStateOracle (ancillaOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle) : Microsoft.Quantum.Oracles.ObliviousOracle
```


## <a name="input"></a>Invoer

### <a name="ancillaoracle--deterministicstateoracle"></a>ancillaOracle: [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)

Een status voorbereiding Oracle $A $ van het type dat wordt toegepast `DeterministicStateOracle` op REGI ster $a $.


### <a name="signaloracle--obliviousoracle"></a>signalOracle: [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)

Een Oracle-$U $ van het type dat `ObliviousOracle` gezamenlijk in het REGI ster $a, s $ wordt ingezet.



## <a name="output--obliviousoracle"></a>Uitvoer: [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)

Een Oracle-$O = UA $ van type `ObliviousOracle` .

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Oracles. DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [Micro soft. Quantum. Oracles. ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)