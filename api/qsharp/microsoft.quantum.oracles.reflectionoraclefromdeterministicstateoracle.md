---
uid: Microsoft.Quantum.Oracles.ReflectionOracleFromDeterministicStateOracle
title: De functie ReflectionOracleFromDeterministicStateOracle
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracleFromDeterministicStateOracle
qsharp.summary: Constructs reflection about a given state from an oracle.
ms.openlocfilehash: c260bdbcdb2ce53ad602bf84e0d31ef4fec24a79
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842515"
---
# <a name="reflectionoraclefromdeterministicstateoracle-function"></a>De functie ReflectionOracleFromDeterministicStateOracle

Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Maakt reflectie over een bepaalde status vanuit een Oracle.

```qsharp
function ReflectionOracleFromDeterministicStateOracle (oracle : Microsoft.Quantum.Oracles.DeterministicStateOracle) : Microsoft.Quantum.Oracles.ReflectionOracle
```


## <a name="description"></a>Beschrijving

Op basis van een deterministische status voorbereiding Oracle die wordt vertegenwoordigd door een unitary-matrix $O $, is het resultaat van deze functie een Oracle die een reflectie rond de status $ \ket{\psi} $ die is voor bereid door de Oracle-$O $; dat wil zeggen de status $ \ket{\psi} $, $O \ket {0} = \ket{\psi} $.

## <a name="input"></a>Invoer

### <a name="oracle--deterministicstateoracle"></a>Oracle: [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)

Een Oracle die kopieën van de status $ \ket{\psi} $ voorbereidt.



## <a name="output--reflectionoracle"></a>Uitvoer: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

Een Oracle die overeenkomt met de status $ \ket{\psi} $.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Oracles. DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [Micro soft. Quantum. Oracles. ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)