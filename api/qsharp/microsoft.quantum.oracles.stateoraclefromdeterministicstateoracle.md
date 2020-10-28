---
uid: Microsoft.Quantum.Oracles.StateOracleFromDeterministicStateOracle
title: De functie StateOracleFromDeterministicStateOracle
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: StateOracleFromDeterministicStateOracle
qsharp.summary: Converts an oracle of type `DeterministicStateOracle` to `StateOracle`.
ms.openlocfilehash: ccb083dbaaec2f306ba0740ef364ebb22408ed98
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708743"
---
# <a name="stateoraclefromdeterministicstateoracle-function"></a>De functie StateOracleFromDeterministicStateOracle

Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)

Pakket [](https://nuget.org/packages/)


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