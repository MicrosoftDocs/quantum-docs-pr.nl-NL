---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracle
title: Door de gebruiker gedefinieerd DeterministicStateOracle-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracle
qsharp.summary: >-
  Represents an oracle for deterministic state preparation.

  The input to the oracle $O$ is:

  - The register that will store the desired quantum state $\ket{\psi}\_s$.
ms.openlocfilehash: f02267d48cf42fb5b02782dc6b667ac7b60a05dc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708778"
---
# <a name="deterministicstateoracle-user-defined-type"></a>Door de gebruiker gedefinieerd DeterministicStateOracle-type

Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)

Pakket [](https://nuget.org/packages/)


Vertegenwoordigt een Oracle voor deterministische status voorbereiding.

De invoer voor de Oracle-$O $ is:

- Het REGI ster waarin de gewenste Quantum status $ \ket{\psi} \_ s $ wordt opgeslagen.

```qsharp

newtype DeterministicStateOracle = ((Qubit[] => Unit is Adj + Ctl));
```



## <a name="remarks"></a>Opmerkingen

Deze Oracle die is gedefinieerd door $O \ket {0} = \ket{\psi} $, treedt op in de status op basis van de berekening $ \ket {0} $ om de status $ \ket{\psi} $ te maken.
De eerste para meter is het Qubit-REGI ster van $ \ket{\psi} $.