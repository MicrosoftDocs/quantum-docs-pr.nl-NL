---
uid: Microsoft.Quantum.Oracles.StateOracleFromDeterministicStateOracle
title: De functie StateOracleFromDeterministicStateOracle
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: StateOracleFromDeterministicStateOracle
qsharp.summary: Converts an oracle of type `DeterministicStateOracle` to `StateOracle`.
ms.openlocfilehash: 4eed29072cab9e8c106509a6a114c8a071441079
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842509"
---
# <a name="stateoraclefromdeterministicstateoracle-function"></a>De functie StateOracleFromDeterministicStateOracle

Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Converteert een Oracle van het type `DeterministicStateOracle` naar `StateOracle` .

```qsharp
function StateOracleFromDeterministicStateOracle (deterministicStateOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle) : Microsoft.Quantum.Oracles.StateOracle
```


## <a name="input"></a>Invoer

### <a name="deterministicstateoracle--deterministicstateoracle"></a>deterministicStateOracle: [deterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)

Een status voorbereiding Oracle $A $ van type `DeterministicStateOracle` .



## <a name="output--stateoracle"></a>Uitvoer: [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)

Dezelfde status voorbereiding Oracle $A $, maar nu van type `StateOracle` . Houd er rekening mee dat de vlag index in dit `StateOracle` een dummy variabele is en geen effect heeft.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Oracles. DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [Micro soft. Quantum. Oracles. StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)